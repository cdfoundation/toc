# Project Proposal for CDEvents

## Project Description

### What does the project do?

CD Events are Cloud Events with events specific extensions and payload structure, which is based on the CD Event vocabulary.  The goal of CD Events is to define a specification to enable a common communication between tools in the CI/CD chain. Companies no longer have single CI/CD tools and need tools to talk with each other.  Also, they need the ability to swap tools as new needs arise.

### Why it is valuable?

The CD Event project will provide visibility and ability for users to contribute to the specification. These contributions we enable to communication between tools to be standardized and adopted providing a single view into the CI/CD pipeline.  

### Background origin and history

The CD Events started as a SIG under the CDF.  The members of the SIG have defined an initial event vocabulary and implemented a Proof of Concept around that vocabulary.  The POC has been we received when presented at multiple conferences and online talks.  The SIG is a diverse group that includes contributors, CDF member companies, CDF projects and CNCF projects.

## Alignment with CDF Charter Mission

### Describe alignment with the charter

The CD Foundation’s strategic goals include driving the adoption of continuous delivery. CD Events fits into this strategy by providing a standard which tools in the CD pipeline can communicate.  CD Events is CI/CD tool agnostic, supports any type of development language, and interacts with any cloud provider.  CD Events will enable existing CI/CD tools to communicate without writing a specific "plugin" into every tool, instead write once and communicate with may.

## Code of Conduct

### Link to Code of Conduct (if one is adopted)

The CD Events SIG is currently working under the CDF Code of Conduct.  The CD Events project will adopt the CDF Code of Conduct or Linux Foundation Code of Conduct as part of the acceptance as a project.

## TOC Sponsors

- Andrea Frittoli
- Steve Taylor

## Project License

- Link to Project License
[Apache 2.0](https://github.com/cdfoundation/sig-events/blob/main/LICENSE)

## Source Code Control

- Link to Source Code Control (GitHub by default)

[Current repo](https://github.com/cdfoundation/sig-events) is under the CDF which is moving to [CDEvents GitHub Org](https://github.com/cdevents)

## Issue Tracker

- Link to Issue Tracker (GitHub by default)
[Current Issues](https://github.com/cdfoundation/sig-events/issues)

## External Dependencies

- List of dependencies with license

[GoLang](https://golang.org/LICENSE) - for the CD Events GoLang SDK

## Release Methodology and Mechanics

### Describe the release methodology and mechanics

CD Events will follow the typical Git Flow process using GitHub Pull Requests for handling changes to the repos.  Releases of the deliverables such as the SDK will be made available on the GitHub repo and will follow the schematic versioning schema, i.e. v1.0.0.0.

## Initial Committers

## Members

Current members:

- Ravi Lachhman, [@ravilach](https://github.com/ravilach), Harness
- Andreas Grimmer, [@agrimmer](https://github.com/agrimmer), Dynatrace
- Emil Bäckmark, [@e-backmark-ericsson](https://github.com/e-backmark-ericsson), Ericsson
- Ramin Akhbari, ([@rakhbari](https://github.com/rakhbari)), eBay
- Mattias Linnér, [@m-linner-ericsson](https://github.com/m-linner-ericsson), Ericsson
- Andrea Frittoli, [@afrittoli](https://github.com/afrittoli), IBM
- Mauricio Salatino [@salaboy](https://github.com/salaboy), [VMware](https://vmware.com) [Knative Project](http://knative.dev)
- Steve Taylor [@sbtaylor15](https://github.com/sbtaylor15), [DeployHub](https://www.deployhub.com) / [Ortelius OS](https://ortelius.io)
- Tracy Ragan [@tracyragan](https://github.com/tracyragan), [DeployHub](https://www.deployhub.com) / [Ortelius OS](https://ortelius.io)
- Brad McCoy [@bradmccooydev](https://github.com/bradmccoydev), [Ortelius OS](https://ortelius.io)
- Erik Sternerson [@erkist](https://github.com/erkist), doWhile
- Cameron Motevasselani ([@link108](https://github.com/link108)), [Armory](https://www.armory.io/)
- Alois Reitbauer ([@aloisreitbauer](https://github.com/aloisreitbauer)), [Dynatrace](https://www.dynatrace.com/)
- Fredrik Fristedt [@fredjn](https://github.com/fredjn), Axis Communications
- Oleg Nenashev [@oleg-nenashev](https://github.com/oleg-nenashev), Jenkins

## Governance

- Describe the project leadership team and decision-making process

[SIG Governance](https://github.com/cdfoundation/sig-events#governance) which will be used as the starting point for the "project" governance.

- Link to any documented governance practices

[CDF SIG Governance](https://github.com/cdfoundation/toc/blob/master/GROUPS.md#sigs)

## Preferred Maturity Level

We are requesting to be added as an *Incubating* project.

## Project Website

- Link to projects website
[Project Site](https://github.com/cdevents) - The GitHub pages will be starting point for the project website.  Waiting on the LFX to obtain the events.cd domain name.

## Communication Channels

- List Slack, Discord, IRC channels
cdeliveryfdn.slack.com - sig-events channel

- List Email list
- List Facebook handle
- Twitter
[@_cdevents](https://twitter.com/_cdevents)
- List other social media accounts

## Existing financial sponsorship

- List existing financial sponsorships
None at this time

## Infrastructure

- List existing infrastructure
- List new infrastructure needs
Domain Name - events.cd
Website - Hugo Server or GitHub Pages
