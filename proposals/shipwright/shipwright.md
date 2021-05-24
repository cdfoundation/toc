# CD Foundation Proposal for Shipwright

## Name of Project

Shipwright

## Summary

### Proposal

[Shipwright](https://shipwright.io) is a framework for building container images on Kubernetes.
Shipwright is based on years of experience developing and operating [OpenShift Builds](https://docs.openshift.com/container-platform/4.7/cicd/builds/understanding-image-builds.html) as part of the OpenShift platform, with contributions from the [IBM Cloud Code Engine](https://www.ibm.com/cloud/code-engine) team.
Shipwright powers IBM Cloud Code Engine container image builds, and is expected to form the foundation of the OpenShift Builds v2 product to be released in Tech Preview later this year.

Building container images reliably, securely, and efficiently is increasingly becoming a core function of a modern cloud native delivery pipeline, and Shipwright intends to be a flexible and powerful tool to meet the needs of developers, operators, security auditors, and more.

### Rationale

We believe the CD Foundation is the correct home for Shipwright.

1. Shipwright is built on Tekton, a CDF project since its founding. Sharing foundation ownership seems natural.
1. The Shipwright project has so far been a joint venture between teams in Red Hat OpenShift and IBM Cloud Code Engine, but we heartily welcome contributions from others, and we expect neutral ownership to help toward that goal.

## Statement on Alignment with Foundation Charter's Mission

Building container images is a common task in modern continuous delivery pipelines, and Shipwright makes building container images on Kubernetes easy, flexible, and secure.

## Link to *current* Code of Conduct (if one is adopted already)

[Code of Conduct](https://github.com/shipwright-io/community/blob/main/code-of-conduct.md)

## Sponsor from TOC, if identified (a sponsor helps mentor projects)

None yet identified

## Project license

Apache 2.0

## Source control (GitHub by default)

[Shipwirhgt GitHub Repo](https://github.com/shipwright-io)

## Issue tracker (GitHub by default)

[Shipwright Build Issue Tracker](https://github.com/shipwright-io/build/issues)

## External dependencies (including licenses)

Tekton, Kubernetes (Apache 2.0)

Code dependencies: https://github.com/shipwright-io/build/blob/main/go.mod

## Release methodology and mechanics

We have adopted a six-week release cadence over the last two releases.
Releases are largely automated using GitHub Actions at this time.
Released images are available on [Quay.io](https://quay.io/shipwright/build-operator), and installable release YAMLs are available in [GitHub Releases](https://github.com/shipwright-io/build/releases).

## Names of initial committers, if different from those submitting proposal

Initial committers are same as ones submitting proposal.

## Briefly describe the project's leadership team and decision-making process

Leadership team:
- [Shoubhik Bose](https://github.com/sbose78) (Red Hat)
- [Enrique Encalada](https://github.com/qu1queee) (IBM)
- [Adam Kaplan](https://github.com/adambkaplan) (Red Hat)

The Shipwright community holds public weekly meetings to discuss relevant topics.

Decisions are made by rough consensus, without any formal governance structure at this time.
We intend to formalize project governance over time, with CD Foundation's help and guidance.

## Link to any documented governance practices

- [Contributing Guidelines](https://github.com/shipwright-io/build/blob/main/CONTRIBUTING.md)

## Preferred maturity level (see stages below)

Incubation

## List of project's official communication channels (slack, irc, mailing lists)

- `#shipwright` in the Kubernetes Slack (https://slack.k8s.io)
- [@shipwrightio](https://twitter.com/shipwrightio) on Twitter
- Mailing lists for [users](https://lists.shipwright.io/archives/list/shipwright-users@lists.shipwright.io/) and [developers](https://lists.shipwright.io/archives/list/shipwright-dev@lists.shipwright.io/)

## Link to project's website

- [Homepage](https://shipwright.io)

## Existing financial sponsorship

Project infrastructure is sponsored by Red Hat using Netlify.
Current core contributors are Red Hat and IBM employees.

## Infrastructure needs or requests

None at this time.
