# CDF Software Supply Chain SIG

## Overview

Recent attacks highlighted the importance of and the need to collaborate on addressing challenges with the Software Supply Chain.
Governments, standards developing organizations, and communities have started focusing on this topic to improve the situation and publishing new announcements, guidelines, and directives.
It is imperative to take actions to ensure security, integrity, and compliance of the Software Supply Chain which includes all source code which is incorporated into an artifact, irrespective of whether it is open source or proprietary software.
Additionally, the systems involved in getting software from developers’ IDEs into the hands of end-users, such as SCM and CI/CD systems, must also be subject to the same level of scrutiny.

One key consideration to take into account while working with Software Supply Chain is CI/CD.
There are many parts of the software lifecycle that need attention and the focus of this SIG is the CI/CD in order to avoid overlaps and contribute to other initiatives aiming to improve the security posture for the products and production systems from CI/CD perspective.

The reasons for this is that the practices employed and the technologies used by organizations while establishing software flows heavily depend on CI/CD.
The activities that start, once code contributions leave developer's workstations and land in the production environments serving end users’ needs, are orchestrated by CI/CD systems.
Various industry best practices such as policy driven CD and SBOMs are all important aspects to take into consideration to ensure security, integrity, and compliance for the products that are deployed to production.

Another critical aspect to highlight is the importance of securing the CI/CD systems themselves as these systems are essentially production systems.
CI/CD systems are also constructed using open source and/or commercial software and any issues with security, integrity, and compliance within these systems could have great impacts on the products produced using them.
In addition to this, CI/CD systems interact with or operate against various environments such as staging and production.
Such environments could be hosted on-premise, private and public clouds which increases the complexity and importance of securing CI/CD systems themselves.
The Software Supply Chain SIG aims to study different aspects of CI/CD systems, securing it to prevent bad actors from exploiting these systems and the products produced and deployed by them for malicious intentions.

In addition to identifying and working with relevant topics, the SIG will take a practice oriented approach by implementing proof of concepts and sample pipelines using various CI/CD technologies and tools to highlight how such tools could be used in a Software Supply Chain, how good practices could be employed and what kind of opportunities there are.
A critical requirement for success is collaboration between DevOps practitioners and [CDF hosted projects](https://cd.foundation/projects/) such as Tekton and Jenkins.
Additionally, collaborating with the existing CDF SIGs including but not limited to [Interoperability](https://github.com/cdfoundation/sig-interoperability), [Events](https://github.com/cdfoundation/sig-events), and [Best Practices](https://github.com/cdfoundation/sig-best-practices) is critical for the SIG since some of the topics driven by these SIGs such as metadata standardization and events are relevant for the topics this SIG will work on, such as SBOMs and notification of vulnerabilities.
The Software Supply Chain SIG will also look for synergies between CDF and other communities such as [OpenSSF](https://openssf.org/) and projects and working groups hosted by it such as [Sigstore](https://www.sigstore.dev/), [SLSA](https://slsa.dev/), [Security Tooling WG](https://github.com/ossf/wg-security-tooling), and [Supply Chain Integrity WG](https://github.com/ossf/wg-supply-chain-integrity) to ensure CI/CD aspects are not overlooked.


## Members

* Liora Milbaum ([@lmilbaum](https://github.com/lmilbaum)), Red Hat
* Fatih Degirmenci ([@fdegir](https://github.com/fdegir)), Ericsson Software Technology
* Kara de la Marck ([@MarckK](https://github.com/MarckK)), CDF
* Georg Kunz ([@gkunz](https://github.com/gkunz)), Ericsson
* Erhan Vikyol ([@vikyol](https://github.com/vikyol)), Storebrand
* Tracy Miranda ([@tracymiranda](https://github.com/tracymiranda)), Chainguard
* Melissa McKay ([@mjmckay](https://github.com/mjmckay)), JFrog
* Maxime Gréau ([@mgreau](https://github.com/mgreau)), Elastic
* Majinghe ([@majinghe](https://github.com/majinghe))
* Dan Garfield ([@todaywasawesome](https://github.com/todaywasawesome)), Codefresh 

## New Members

Membership to the CDF SIG Software Supply Chain is open to the public and self-declared.

New members are advised to:

* Join the SIG and CDF TOC maillists.
* Join the SIG Slack Channel and introduce yourself.
* Go through the README.md document.
* Regularly join the SIG Meetings.
* Submit a PR to add yourself to the members list.
* Here are various ways to get involved:
  * Share your thoughts by joining the meetings or by posting to maillist and Slack channel.
  * Present a project the community you are part of is working on.
  * Add a topic you would like to discuss to the agenda.
  * Create a new issue to start gathering feedback and collaborating.
  * Choose an issue where help is needed and comment on it expressing interest.
  * Propose a proof of concept.

## Governance

SIG Software Supply Chain is a [CDF Special Interest Group](https://github.com/cdfoundation/toc/tree/master/sigs).

The process SIG Software Supply Chain follows can be seen from [here](https://github.com/cdfoundation/toc/blob/master/GROUPS.md#sigs).

Chairs and the TOC Sponsor of the SIG are

* Liora Milbaum ([@lmilbaum](https://github.com/lmilbaum)), Red Hat - Co-chair
* Fatih Degirmenci ([@fdegir](https://github.com/fdegir)), Ericsson Software Technology - Co-chair
* Melissa McKay ([@mjmckay](https://github.com/mjmckay)), JFrog - TOC Sponsor

### SIG Workstreams

SIG Software Supply Chain welcomes contributors who take part in the SIG to form workstreams to work on specific areas of interest in a more focused and structured way.

Workstream governance is TBD.

## Communication

SIG Software Supply Chain communication happens via a public mailing list and everyone is
welcome to join our open discussions.

SIG Software Supply Chain also uses Slack for additional collaboration opportunities.

* Maillist: TBD
* Slack Channel: TBD

## Meetings

SIG Software Supply Chain meets TBD.

* Meeting agenda and minutes: TBD
* Meeting recordings: TBD
* Zoom Bridge: TBD
* Zoom International dial-in numbers: [here](https://zoom.us/zoomconference)
* CDF Public Calendar (UTC): [here](https://calendar.google.com/calendar/u/0/embed?src=linuxfoundation.org_mhf0kmgedn67ihni8r129avp24@group.calendar.google.com&ctz=UTC)
