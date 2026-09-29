# Project Proposal for Conduit

*Submitted by Dadisi Sanyika, Founder & CEO, Sol Duara, Inc. — project creator and lead.*

## Project Description

### What does the project do?

Conduit is an intent-aware event orchestration platform for software delivery toolchains, built natively on the CDEvents specification. It gives every tool in a delivery pipeline a single integration surface: each tool connects once to Conduit, and Conduit carries, correlates, and verifies the events that move between all of them.

Air traffic control is the clearest picture of the architecture. Aircraft do not negotiate with each other pairwise; they file flight plans and coordinate through a tower that knows not only where every aircraft *is*, but where each one *intends to go*. Conduit is that tower for software delivery. CDEvents is the shared radio vocabulary. CDrus Expressions are the filed flight plans, machine-readable declarations of workflow intent. Conduit is the controller that checks each movement against declared intent before clearing the next.

Concretely, Conduit is three layers:

1. **Universal transport.** A CDEvents-native hub. Each tool integrates once with Conduit rather than pairwise with every other tool, reducing the integration surface from O(N²) to O(N). Conduit is broker-agnostic: it orchestrates on top of existing message brokers rather than replacing them.

2. **Workflow topology and memory.** Every CDEvent that flows through Conduit is persisted to an event store, producing an immutable, queryable audit trail across the entire toolchain, "what happened in the last deployment?" and "why did this pipeline fail?" become one query instead of an archaeology expedition across N tools. Causal chains survive tool boundaries and anonymous restarts through Conduit's `chainId` construction: a UUID v7 base combined with an HMAC-keyed hash of remote pipeline identifiers, keeping chains both tamper-resistant and efficiently queryable by time range. Because Conduit also holds the declared workflow topology upstream of execution, it can reason about paths, deviation, and optimization before a run collapses into a single trace — it holds the map, not just the footprints.

3. **Intent verification, via CDrus Expressions.** CDrus Expressions encode the *causal intent* of a workflow separately from its execution path. Before routing proceeds, Conduit verifies that a downstream tool's interpretation of an upstream event matches the sender's declared intent. The failure class this prevents has a name in this project, *confliguration*: Tool A emits "build succeeded," Tool B silently reads "compilation complete, tests pending," and the divergence propagates downstream undetected. Conduit converts that silent failure into a detectable, blockable condition at the boundary where it occurs.

**CDrus Expressions are part of this proposal and are retained locally to the project.** The expression language specification, its JSON Schemas, and the reference expression library are contributed together with Conduit, versioned with Conduit releases, and governed by the Conduit project's own processes, not maintained as an external or vendor-controlled dependency. Every published schema and expression carries a URI that dereferences to the exact document it names (serving today from `schemas.cdrus.dev` and `expressions.cdrus.dev`). The project will keep that guarantee under project-controlled infrastructure and intends to contribute the dereferenceable-schema publishing pattern upstream to CDEvents.

### Why it is valuable?

The integration problem in software delivery is structural, and it is expressible in formal terms. With N tools, pairwise integration requires N(N−1)/2 connections — O(N²) growth. At the 20–50 tools common in enterprise pipelines, that is hundreds of integration points, each carrying its own translation mapping, routing rules, and maintenance contract. Traditional event buses centralized the routing but preserved the semantic chaos underneath: every producer still emits in its own dialect, every consumer still expects its own, and the bus moves messages it cannot interpret. The N×N translation matrix survives — invisible, ungoverned, and exponentially expensive.

CDEvents resolved the vocabulary. What remains unresolved is enforcement: nothing in the stack yet guarantees that the meaning a tool sends is the meaning the next tool acts on. Conduit closes that gap. The distinction is grounded in speech-act theory: a message has a locution (what it says), an illocution (what it intends), and a perlocution (what its receiver does with it). Today's toolchains transmit locutions fluently and lose the rest. Conduit's contribution is verifying that intent survives the trip — its operating principle is test-test-store: test the sender's declared intent, test the receiver's interpretation, and commit the event to the chain only after the two are normalized.

For end users, the value lands as four things: one integration per tool instead of one per pair; tools that can be swapped without rewriting the pipeline's nervous system; a single queryable audit trail spanning every tool in the chain; and semantic failures caught at the boundary instead of discovered in production.

### Background origin and history

Conduit is not arriving at the CDF from outside. It is SIG-originated work returning for project status.

SIG Events — the CDEvents SIG — chartered a scope that was always wider than a vocabulary. The SIG's own charter names events used by tools for orchestration and workflows; pipeline-to-pipeline communication via events; how events are related and ordered (links versus trace context); and tracing and auditing of the entire delivery process, the charter literally asks "What truly occurs?" The SIG defined the event vocabulary, built the proof of concept demonstrating tools interoperating through it, and committed to reference implementations on top of CloudEvents. When the vocabulary moved into project status as CDEvents, the specification half of that charter found its home. The other half, the layer that consumes, correlates, orders, audits, and orchestrates those events across a toolchain, had no successor.

Sol Duara, Inc. picked that work up because no one else was doing it, and the continuity is personal before it is corporate. Dadisi Sanyika's participation in the [CDEvents Working Group](https://hackmd.io/@cdfoundation/HJ0mM5d4_) dates to November 2022, the project's first year, where his first recorded meeting was spent on event links, context propagation, and end-to-end traceability, the precise problem space Conduit's chain-continuity design answers. That participation predates and spans the founding of Sol Duara; the company was formed as the vehicle for work already underway. Today he is a sustained working-group participant, and contributes directly to the specification, including subject proposals for DataOps (migration, reconciliation) and scheduling (scheduledExecution, changeWindow) events now working through the group's review process. He designed Conduit to carry the chartered scope from proof of concept to platform, CDEvents-native from the first commit rather than adapted to the standard after the fact, and the work kept confirming the conclusion the SIG's charter implies: an open standardized vocabulary only becomes load-bearing when something enforces it end to end. CDrus Expressions are Sol Duara's original contribution to that lineage, the declaration layer the SIG scope never reached, without which intent cannot be checked at all, first demonstrated to the CDEvents Working Group in June 2026 and under its review since.

This proposal is therefore a return, not a donation. Work chartered inside a CDF SIG, matured under one company's stewardship, comes back for project status and community governance.

## Scope

### Goals

1. Provide the universal O(N) integration surface for CDEvents-speaking tools: transport, correlation, audit, and chain continuity.
2. Maintain the CDrus Expressions specification, schemas, and reference expression library inside the project, with specification changes made through project governance.
3. Guarantee that every published schema and expression URI dereferences to the exact versioned document it names.
4. Deliver SDKs that lower the cost of emitting and consuming conformant events: TypeScript and Go as the reference implementation, followed by Python, Java, PHP, and C++.
5. Contribute improvements upstream to CDEvents, including the dereferenceable-schema publishing pattern and SDK-surface findings from production integration work.

### Non-Goals

1. Conduit is not a CI/CD engine. It does not compete with Jenkins, Jenkins X, Ortelius, Spinnaker, Screwdriver, or any execution tool; it is the connective tissue between them.
2. Conduit does not define a proprietary event format. It is CDEvents-native and will not fork or shadow the open specification.
3. Conduit is not a message broker. It is an proleptic event orchestrator; a closed system that is not open to brokers organizations already run.

## Alignment with CDF Charter Mission

Driving the adoption of continuous delivery is the CD Foundation's stated strategic goal, and interoperability is its most consistently named blocker; the reason the Foundation chartered SIG Interoperability and SIG Events, and the reason CDEvents exists. Conduit is the other half of that same chartered scope: the specification standardized what tools say; Conduit ensures the toolchain acts on what was meant. A standard's value is realized at the moment something depends on it end to end. Conduit makes CDEvents load-bearing.

The alignment runs in both directions. Existing CDF projects, Jenkins, Jenkins X, Spinnaker, Screwdriver, Ortelius, gain interconnection through a single hub without pairwise plugin maintenance between them. CDEvents gains a reference orchestrator that exercises the specification under production pressure, a working pattern for dereferenceable schema hosting, and a multi-language SDK contribution pipeline, a flow that is already running, with Sol Duara's event-subject proposals and CDrus reviews moving through the working group today. And the Foundation gains the piece of the interoperability story it has not yet had: proof that the standard composes into a working system.

Finally, neutrality is not governance hygiene for this project, it is a functional requirement. A hub that every vendor's tool connects through cannot credibly be owned by any single vendor. The CD Foundation is not merely a good home for Conduit; it is where this work began, and the only kind of home under which the architecture keeps its promise.

## Code of Conduct

The project operates under the [CDF Code of Conduct](https://github.com/cdfoundation/.github/blob/main/CODE_OF_CONDUCT.md) and will formally adopt the CDF/Linux Foundation Code of Conduct as part of acceptance.

## TOC Sponsors

- [To be identified — the project is actively requesting two TOC sponsors and welcomes mentorship per the project lifecycle process.]

## Project License

- [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) for all Conduit and CDrus Expressions repositories.

## Source Code Control

- Conduit: `https://github.com/Sol-Duara-Inc/conduit` *(confirm final path at submission)*
- CDrus Expressions: `https://github.com/Sol-Duara-Inc/cdrus`
- Upon acceptance, repositories transfer to a neutral project GitHub organization (following the CDEvents precedent), with CDrus Expressions housed inside that same organization as a project component.

## Issue Tracker

- GitHub Issues on the repositories above.

## External Dependencies

- [CDEvents specification](https://github.com/cdevents/spec) — Apache-2.0
- [CloudEvents](https://github.com/cloudevents/spec) — Apache-2.0
- PostgreSQL (event store and orchestration state) — PostgreSQL License
- Valkey (Redis-API-compatible working-state cache and event deduplication) — BSD-3-Clause
- RabbitMQ (default broker binding; broker layer is pluggable) — MPL-2.0
- Go and TypeScript toolchains — BSD-3-Clause / Apache-2.0

CDrus Expressions is intentionally absent from this list: it is a component of the project, not an external dependency. That is the point of retaining it locally.

## Release Methodology and Mechanics

Conduit follows Git flow with pull-request review on all changes and [semantic versioning](https://semver.org/) for releases. Releases are signed (Sigstore cosign) and ship with DSSE attestations, aligning with the practices championed by SIG Software Supply Chain. Each release publishes its CDrus Expressions schemas and reference expressions to versioned, dereferenceable URIs, so the specification, the schemas, and the platform that enforces them move in lockstep and can never drift apart silently.

## Initial Committers

- Dadisi Sanyika ([@sol-duara](https://github.com/sol-duara), Sol Duara, Inc. — project creator and lead; CDEvents Working Group participant since November 2022, named maintainer May 2026
- An open invitation stands to SIG Events and SIG Interoperability contributors to rejoin, as early committers, the work their groups chartered; broadening the committer base across organizations is an explicit first-year growth objective, not an afterthought.

## Governance

The project launches under a documented maintainer model: decisions by lazy consensus, escalating to maintainer vote; maintainership earned through sustained contribution; an explicit, dated commitment to multi-organization maintainership on the growth-plan timeline. Changes to the CDrus Expressions specification follow the same public process as changes to Conduit itself, which is precisely what "retained locally to the project" guarantees: the intent language is governed by the community that depends on it.

## Preferred Maturity Level

Incubating.

## Project Website

- Project site: to be established under a neutral project domain post-acceptance *(interim: Sol Duara-hosted project pages)*, built on the Docsy/Hugo pattern used by CDEvents.
- Live today: `schemas.cdrus.dev` and `expressions.cdrus.dev`, serving dereferenceable schemas and expressions.

## Communication Channel

- CDF Slack: `#conduit` channel (requested on acceptance)
- Mailing list: `cdf-conduit@list.cd.foundation` (per CDF groups.io convention, requested on acceptance)
- Social handles: to be registered under the project name at acceptance.

## Existing financial sponsorship

Sol Duara, Inc. funds and staffs Conduit's development and commits to continuing that investment through incubation.

## Infrastructure

Existing:

- GitHub repositories under Sol-Duara-Inc (transferring to a neutral org on acceptance)
- Schema and expression hosting on Cloudflare Pages under `cdrus.dev`, with correct content types and versioned paths

Requested:

- CDF Slack channel and mailing list as above
- Guidance on neutral control of the schema-hosting domains consistent with the Foundation's IP policy, so the dereferenceability guarantee is held by the project rather than by any company
- Project website hosting per CDF norms

