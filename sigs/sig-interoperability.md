# CDF Interoperability SIG

## Overview

The emergence of new open technologies and methodologies such as cloud native and
microservices has resulted in tremendous advances in various industries and enabled
the rapid development and delivery of new features and services to the end-users
faster than before. Continuous Integration (CI) and Continuous Delivery (CD) are
prerequisites and enablers for organizations to use these technologies and achieve
true agility in response to these changes.

The organizations that embrace CI/CD employ various tools and technologies depending
on their needs and where they are in their CI/CD transformation. Organizations often
employ more than one tool in various stages of their CI/CD pipelines due to different
capabilities provided by the tools. This is perhaps one of the biggest benefits the
users get by using open technologies for their CI/CD needs.

However, one of the challenges users face is the lack of interoperability across the
CI/CD tools and technologies, resulting in various issues while constructing and
running pipelines such as passing metadata and artifacts between the tools or achieving
traceability from commit to deployment. Often users end up building "own glue code" to
address what is a common problem, further complicating moving from one tool to another
and adopting new technologies and methodologies.

These "glue code solutions" are generally specific to users needs and the tools rather
than being loosely coupled and agnostic to tooling and technology. Additionally these
solutions are not visible to other users and the communities, making them vulnerable to
the risks of outage in their CI/CD pipelines due to the potential changes (ie non-backward
changes to the APIs, changes in data models) that happens to the tools in respective
projects.

The interoperability SIG will focus on addressing these challenges and further work with
projects to achieve a common set of solutions.

CDF Interoperability SIG aims to enable a dialog in the interoperability area by bringing
CI/CD users together with the open source projects in order to

* clarify what interoperability means for the CI/CD ecosystem
* promote the need to collaborate on interoperability challenges in a neutral forum
* highlight and promote the needs of the users who face challenges constructing complex
end-to-end CI/CD flows and pipelines by employing different tools and technologies
* explore synergies between, and enable collaboration across, the CI/CD projects with
regards to interoperability
* pursue solutions which are; loosely coupled, scalable, flexible, and tool and
technology agnostic
* reduce the need for users to implement in-house solutions by promoting native
interoperability between tools
* attract and assist projects that work on interoperability

## Members

Members of this SIG can be viewed [here](https://github.com/cdfoundation/sig-interoperability#members)

## Governance

SIG Interoperability is a [CDF Special Interest Group](https://github.com/cdfoundation/toc/tree/master/sigs).

Governance details for this SIG can be found [here](https://github.com/cdfoundation/sig-interoperability#governance)

## Communication

Communication details for this SIG can be found [here](https://github.com/cdfoundation/sig-interoperability#communication)

## Meetings

Meeting details and minutes are here: [here](https://github.com/cdfoundation/sig-interoperability#meetings)
