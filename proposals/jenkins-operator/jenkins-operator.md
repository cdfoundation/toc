# CD Foundation Proposal for Jenkins Operator

## Name of project

Jenkins Operator

## Summary

### Proposal

### Rationale

The main reason why we decided to implement the Jenkins Operator is the fact that we faced a lot of problems with standard Jenkins deployment. We want to make Jenkins more robust, suitable for dynamic and multi-tenant environments.

With Jenkins Operator project we want to enable our community to run Jenkins in cloud-native environments. Also, support most of the public cloud providers (AWS, Azure, GCP) in terms of additional capabilities like backups, observability and cloud security.
With declarative configuration and full lifecycle management based on Operator Framework this can become the de facto standard for running Jenkins on top of Kubernetes.

### Project Description

The Jenkins Operator is a Kubernetes Native Operator which manages operations for Jenkins on Kubernetes. It has been built with immutability and declarative configuration as code in mind.

## Origin and History

Back in 2016 when Kubernetes was getting more traction, dev teams used to deploy Jenkins to leverage autoscaling and self-healing capabilities in a new Cloud-Native world. It was usually done via Helm 2 which was full of promise and official Helm Charts were far from production-ready.

It often led to maintaining your own private fork with a bunch of additional Groovy scripts to install plugins and configure Jenkins which became unmaintainable as it grew to a large scale.

The number of issues and support activities related to managing Jenkins at scale forced us to rethink our initial approach. We made a decision to adopt the CoreOS Operator Pattern and automate the full lifecycle of Jenkins.

As a result of hard work, we released the initial version of Jenkins Kubernetes Operator which quickly became adopted by the community and hosted under the official Jenkins GitHub organization.

## Statement on Alignment with Foundation Charter's Mission

The CD Foundation’s strategic goals include driving the adoption of continuous delivery and open source. Jenkins itself covers a significant market share when it comes to CI/CD. With the Jenkins Operator project we want to enable community to use it in cloud-native fashion.
There is a great potential to grow open source community around Jenkins and Kubernetes. Eventually, understand how Kubernetes operators ecosystem might help in area software delivery.   

## Growth Plan

### Today

As for now, the project has been widely adopted by the Jenkins community (400+ stargazers on GitHub) and officially became Jenkins organization sub-project.

## Tomorrow

We aim to make Jenkins Operator a standard when it comes to running Jenkins on top of Kubernetes in a cloud-native environments.

## Long-Term

Enhance Jenkins ecosystem and stay on top of cloud-native technology landscape.

## Link to *current* Code of Conduct (if one is adopted already)

https://github.com/jenkinsci/kubernetes-operator/blob/master/CODE_OF_CONDUCT.md

## Sponsor from TOC, if identified (a sponsor helps mentor projects)

N/A

## Project license

Apache License Version 2.0

## Source control (GitHub by default)

https://github.com/jenkinsci/kubernetes-operator

## Issue tracker (GitHub by default)

https://github.com/jenkinsci/kubernetes-operator/issues

## External dependencies (including licenses)

https://github.com/jenkinsci/kubernetes-operator/blob/master/go.mod

## Release methodology and mechanics

* End to end testing phase - ensure all changes, bug fixes and improvements.
* Using semantic release package to handle versioning - https://github.com/semantic-release/semantic-release
* Publish Docker containers e.g. virtuslab/jenkins-operator:v0.6.0
* Publish release notes, migration guide, description of major features, etc. https://github.com/jenkinsci/kubernetes-operator/releases

Release process is automated using the following [Makefile](https://github.com/jenkinsci/kubernetes-operator/blob/master/Makefile).

## Names of initial committers, if different from those submitting proposal

* https://github.com/tomaszsek
* https://github.com/jakalkhalili
* https://github.com/SylwiaBrant
* https://github.com/Sig00rd
* https://github.com/KorusMateusz
* https://github.com/prryb
* https://github.com/MKajzik

More at https://github.com/jenkinsci/kubernetes-operator/graphs/contributors

## Briefly describe the project's leadership team and decision-making process

[Bartek Antoniak](https://github.com/antoniaklja) is Cloud Engineering Manager at VirtusLab and leading the Jenkins Operator initiative together with the team of five people. 
When it comes to the decision making process, we mostly rely on architecture proposals (RFC documents) and brainstorming sessions.

## Link to any documented governance practices

https://github.com/jenkinsci/kubernetes-operator/blob/master/CONTRIBUTING.md

## Preferred maturity level (see stages below)

Incubation

## List of project's official communication channels (slack, irc, mailing lists)

* Slack: dedicated channel #jenkins-operator on virtuslab-oss.slack.com
* Stack Overflow: https://community.jenkins.io/c/contributing/jenkins-operator/20

## Link to project's website 

* Homepage and documentation - https://jenkinsci.github.io/kubernetes-operator/

## Links to social media accounts

* Meetup: https://www.jenkins.io/events/online-meetup/

## Existing financial sponsorship

Project development and infrastructure is sponsored by [VirtusLab](https://virtuslab.com/). The core committers are [VirtusLab](https://virtuslab.com/) employees.

## Infrastructure needs or requests

We want to be associated with and have a presence in CD foundation events that enable developers around the world to leverage, contribute, and take advantage of our open source offering.
Also, we'd like to have dedicated compute, storage and networking in a public cloud space necessary for continuous development and continuous testing the project.