# CDF Events SIG

## Overview
Today’s CI/CD systems do not talk to each other in a standardized way. This leads to problems related to interoperability, notification of failure issues, and poor automation.

This group is looking at how events can help to create CI/CD systems with a decoupled architecture that is easy to scale and makes it resilient to failures. Using events could also increase automation when connecting workflows from different systems to each other, and as a result empowering tracing/visualizing/auditing of the connected workflows through these events.

### Purpose
The group focuses on the use of events to provide interoperability through topics like:
- When are events suited? For triggers, audits, monitoring, management
  - Common guidelines for at-least-once, at-most-once, exactly once, ordering… When to apply what strategy?
- Best practices for event-driven CI/CD systems
- Events to be used by tools for orchestration/workflows
- Pipeline to pipeline communication via events
- Tracing/auditing/graphing/visualizing of the entire process, e.g., through events. What truly occurs?
- Metrics, e.g., how many versions have been deployed, how many PRs (Pull Requests) have been raised, how many events have been issued?  
- How are events related and how are they ordered (links vs trace context)?

### Outcome
The group is working on a standardized event protocol that caters for technology agnostic machine-to-machine communication in CI/CD systems. This specification will be published, reviewed and agreed upon between relevant Linux Foundation projects/members.

The group aims to provide reference implementations such as event listeners and event senders on top of CloudEvents.

## Members
*In alphabetical order, except for the chairs*
* Andrea Fritolli (IBM) - Co-chair
* Emil Bäckmark (Ericsson) - Co-chair
* Andreas Grimmer (Dynatrace)
* Cameron Motevasselani (Armory)
* Erik Sternerson (doWhile)
* Mattias Linnér (Ericsson)
* Mauricio Salatino (Camunda / LearnK8s)
* Ravi Lachhman (Harness)
* Steve Taylor (DeployHub)
* Tracy Ragan (DeployHub)

TOC Sponsor: \<TBD\>

## Communication
Communication in this SIG is primarily done through its [Slack channel](https://cdeliveryfdn.slack.com/archives/C0151BTKEJX)

## Meetings
The SIG meets every second Monday, at 4 PM CET. Meeting notes can be seen [here](https://github.com/cdfoundation/sig-interoperability/blob/master/workstreams/events_in_cicd/meetings.md)
