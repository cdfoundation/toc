# Project Graduation Proposal for Tekton

## Introduction

Tekton is a powerful and flexible open-source framework for creating CI/CD
systems, allowing developers to build, test, and deploy across cloud providers
and on-premise systems. Get started with Tekton.

Since 2018, Tekton has matured considerably, while remaining true to its nature
of having a small footprint and giving users full flexibility in how they setup
their CI/CD system through Tekton.

This very flexibility has enabled Tekton to become the base for the
implementation of more opinionated services on top, ranging from open source
projects, cloud services as well as end-user platforms for DevOps services.

The Tekton community benefits from a large and diverse community, with
contributors from many different companies. The community features an open
governance model, with documented policies about different aspects of the
community life:

- code of conduct
- the governing bodies, their elections and responsibilities
- the contributor ladder with rights and responsibilities
- design principles and development standards
- security policies

Tekton cares a lot about security, both for the project as well as for its
users:

- Tekton has undergone a [security audit][security-audit]
- Tekton has a vulnerability team and [security policy][security-policy]
- Tekton features a project, [Tekton Chains][chains], fully dedicated to
  providing security features for Tekton users, including integration with
  [Sigstore][sigstore]
- The core Tekton projects have all achieved the [OpenSSF Best Practices
  badge][openssf-badge].

Tekton uses Tekton for it's own build and release process, which also means that
Tekton releases are signed through Sigstore, with attestation stored publicly,
so that users may verify both the container images signatures as well as monitor
the attestations. 

Tekton follows documented release cycles, with a community wide [support
policy][support-policy] which aligns with that of the Kubernetes and other
projects in the ecosystem.

The Tekton project is thriving within the Continuous Delivery Foundation,
it has grown to [fullfil](#criteria) all [required criteria]
[tekton-graduation-criteria] and it would like to formally apply for graduation. 

## Criteria

The following twelve graduation criteria have been derived from the
definition of [graduated stage][graduated-stage] as defined by the TOC, and
they have been [agreed] as [Tekton specific graduation criteria]
[tekton-graduation-criteria]. They are tracked in the [Tekton graduation
project][graduation-project] on Tekton side as well.

### C1 Governing Board ✔

Criteria: 
- Have a defined governing body which consists of members from at least 2
  different companies

Evidence:
- [Current Governing Board members](https://github.com/tektoncd/community/blob/main/governance.md#current-members)
- [Principle of maximum representation](https://github.com/tektoncd/community/blob/main/governance.md#maximum-representation)

| Full Name                                  |  Company   | GitHub                                        | Slack                                                         | Elected On | Until    |
|-------------------                         |:----------:|-----------------------------------------------|---------------------------------------------------------------|------------|----------|
| Priya Wadhwa                               | ChainGuard | [priyawadhwa](https://github.com/priyawadhwa) | [@Priya Wadhwa](https://tektoncd.slack.com/team/U02T0CS9PN0)  | Feb 2022   | Feb 2024 |
| Vincent Deemester                          |  Red Hat   | [vdemeester](https://github.com/vdemeester)   | [@vdemeester](https://tektoncd.slack.com/team/UHSQGV1L3)      | Feb 2021   | Feb 2023 |
| Jerop Kipruto (while Christie is on leave) |   Google   | [jerop](https://github.com/jerop)             | [@Jerop Kipruto](https://tektoncd.slack.com/team/U011DPQSP0V) | Apr 2022   | Oct 2022 |
| Andrea Frittoli                            |    IBM     | [afrittoli](https://github.com/afrittoli)     | [@Andrea Frittoli](https://tektoncd.slack.com/team/UJ411P2CC) | Feb 2022   | Feb 2024 |
| Dibyo Mukherjee                            |   Google   | [dibyom](https://github.com/dibyom)           | [@Dibyo Mukherjee](https://tektoncd.slack.com/team/UJ73HM7PZ) | Feb 2021   | Feb 2023 |

### C2 Governance, Decision-Making and Release 🚧

Criteria: 
- Have a documented and publicly accessible description of the project's
  governance, decision-making, and release processes.

Evidence:

- [Project Governance](https://github.com/tektoncd/community/blob/main/governance.md)
- [Decision Making](https://github.com/tektoncd/community/blob/main/governance.md#governance-meetings-and-decision-making-process)
- [Tekton Enhancement Proposals](https://github.com/tektoncd/community/tree/main/teps)
- [Community Wide Release Process](https://github.com/tektoncd/community/blob/main/releases.md)

- [Pipeline Release Cadence and Process](https://github.com/tektoncd/pipeline/blob/main/releases.md)
- [Triggers Release Cadence and Process]() - coming soon
- [Chains Release Cadence and Process]() - coming soon
- [Dashboard Release Cadence and Process](https://github.com/tektoncd/dashboard/blob/main/releases.md)
- [Operator Release Cadence and Process]() - [coming soon](https://github.com/tektoncd/operator/pull/1104)
- [CLI Release Cadence and Process]() - coming soon

### C3 Committers from 2+ Orgs ✔

Criteria: 
- Have a healthy number of committers from at least two organizations. A
  committer is defined as someone with the commit bit; i.e., someone who can
  accept contributions to some or all of the project.

Evidence:

- 24 Companies with 100+ contributions
- 100+ companies who contributed
- Source: [devstat](https://tekton.devstats.cd.foundation/d/5/companies-table?orgId=1)

### C4 Governance and Contributing ✔

Criteria:
- Explicitly define a project governance and committer process. This is
  preferably laid out in a GOVERNANCE.md file and references a CONTRIBUTING.md
  and OWNERS.md file showing the current and emeritus committers.

Evidence:

- [Governance.md](https://github.com/tektoncd/community/blob/main/governance.md)
- [processes.md](https://github.com/tektoncd/community/blob/main/process.md#contributions)
- Contributing.md: [community](https://github.com/tektoncd/community/blob/main/CONTRIBUTING.md), [pipeline](https://github.com/tektoncd/pipeline/blob/main/CONTRIBUTING.md), [triggers](https://github.com/tektoncd/triggers/blob/main/CONTRIBUTING.md), 
[cli](https://github.com/tektoncd/cli/blob/main/CONTRIBUTING.md), [dashboard](https://github.com/tektoncd/dashboard/blob/main/CONTRIBUTING.md), [operator](https://github.com/tektoncd/operator/blob/main/CONTRIBUTING.md), [chains](https://github.com/tektoncd/chains/blob/main/CONTRIBUTING.md)
- OWNERS files: [pipeline](https://github.com/tektoncd/pipeline/blob/main/OWNERS_ALIASES), [triggers](https://github.com/tektoncd/triggers/blob/main/OWNERS), [cli](https://github.com/tektoncd/cli/blob/main/OWNERS), [dashboard](https://github.com/tektoncd/dashboard/blob/main/OWNERS), [operator](https://github.com/tektoncd/operator/blob/main/OWNERS), [chains](https://github.com/tektoncd/chains/blob/main/OWNERS), [catalog](https://github.com/tektoncd/catalog/blob/main/OWNERS).

### C5 Adopters ✔

Criteria:
- Have a public list of project adopters for at least the primary repo (e.g.,
  ADOPTERS.md or logos on the project website).

Evidence:
- [Solarwind][solarwind-trebuchet]
- [adopters.md][adopters]

### C6 OpenSSF Best Practices Badge 🚧 

Criteria:
- Have achieved and maintained an OpenSSF Best Practices Badge.

Badges:

| Project | Badge |
|---------|-------|
| Pipeline | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/4020/badge)](https://bestpractices.coreinfrastructure.org/projects/4020) |
| Triggers | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/6527/badge)](https://bestpractices.coreinfrastructure.org/projects/6527) |
| Chains | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/6408/badge)](https://bestpractices.coreinfrastructure.org/projects/6408) |
| Dashboard | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/6543/badge)](https://bestpractices.coreinfrastructure.org/projects/6543) |
| CLI | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/6510/badge)](https://bestpractices.coreinfrastructure.org/projects/6510) |
| Operator | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/6548/badge)](https://bestpractices.coreinfrastructure.org/projects/6548) |


### C7 Release Cycles and LTS ✔ 

Criteria:
- Projects that have publicly documented release cycles and plans for Long Term
  Support ("LTS").

Evidence:

- [Community Wide Release and LTS Policy][release-lts-policy]

### C8 Platform for other projects ✔

Criteria:
- Projects that have themselves become platforms for other projects.

Evidence:
- Some major OpenSource projects built on top of Tekton are listed
  in the [adopters.md][adopters] list
- Project [FRSCA](https://github.com/buildsec/frsca) is built on top of Tekton

### C9 Attract Committers ✔

Criteria:
- Projects that are able to attract a healthy number of committers on the basis
  of its production usefulness (not simply 'developer popularity').

Evidence:
- Some contributing companies that use Tekton as users and/or vendors:
  - IBM: [Tekton on IBMCloud](https://www.ibm.com/uk-en/cloud/tekton)
  - RedHat: [RedHat OpenShift](https://docs.openshift.com/container-platform/4.8/cicd/pipelines/understanding-openshift-pipelines.html)
  - Relay: [How Relay Works](https://relay.sh/docs/how-it-works/)
  - SolarWind: [Project Trebuchet Keynote](https://www.youtube.com/watch?v=1-tMRxqMwTQ)

### C10 End-user Implementations ✔

Criteria:
- Projects that have several, high-profile or well known end-user
  implementations.

Evidence:
- SolarWind: [Project Trebuchet Keynote](https://www.youtube.com/watch?v=1-tMRxqMwTQ)
- IBM (WIP)

### C11 Security Audit ✔

Criteria:
- Project has undergone a security audit

Evidence:
- [Tekton Security Audit][security-audit]

### C12 TOC Vote 

Criteria:
- Receive a 2/3 supermajority vote from the TOC to move to Graduated stage.

Process:
- Voting on this PR and on the mailing-list thread (link TBD)

## References

- [Graduated Stage Definition][graduated-stage]
- [Tekton specific Graduation Criteria][tekton-graduation-criteria]
- [Tekton Website](https://tekton.dev)
- [Tekton Community](https://github.com/tektoncd/community)
- [Tekton Graduation Criteria tracking project][graduation-project]
- [TOC Graduation Criteria Presentation 04 Oct 2022](https://docs.google.com/presentation/d/1iA26v5y-eTAJhkHrL3jVztxDsUtdeP23fTNn-sW1bu8/edit?usp=sharing)

[pipeline]: https://github.com/tektoncd/pipeline
[triggers]: https://github.com/tektoncd/triggers
[chains]: https://github.com/tektoncd/chains
[dashboard]: https://github.com/tektoncd/dashboard
[cli]: https://github.com/tektoncd/cli
[operator]: https://github.com/tektoncd/operator
[security-audit]: https://cd.foundation/blog/2022/08/26/tekton-security-review-completed/
[security-policy]: https://github.com/tektoncd/community/security
[tekton-graduation-criteria]: https://github.com/cdfoundation/toc/issues/157
[graduated-stage]: https://github.com/cdfoundation/toc/blob/main/PROJECT_LIFECYCLE.md#graduated-stage
[graduation-project]: https://github.com/orgs/tektoncd/projects/24/views/1
[sigstore]: https://sigstore.dev
[openssf-badge]: https://bestpractices.coreinfrastructure.org/en
[support-policy]: https://github.com/tektoncd/community/blob/main/releases.md#support-policy
[release-lts-policy]: https://github.com/tektoncd/community/blob/main/releases.md
[adopters]: https://github.com/tektoncd/community/blob/main/adopters.md
[solarwind-trebuchet]: https://www.youtube.com/watch?v=1-tMRxqMwTQ