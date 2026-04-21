# CDF Project Proposal: CI/CD Cybersecurity Guide

## Project Name
CI/CD Cybersecurity Guide

## Project Proposal

The CI/CD Cybersecurity Guide is an open-source reference framework that maps security controls and open-source security tooling across the Continuous Integration and Continuous Delivery lifecycle. The guide helps organizations implement secure-by-design CI/CD pipelines aligned with recognized frameworks such as NIST SSDF, Executive Order 14028, SLSA, Cybersecurity Resiliency Act (CRA), and emerging software supply-chain assurance expectations.

The project provides:
- a structured mapping of security practices across pipeline stages
- alignment guidance between open-source tooling and security frameworks
- implementation pathways for platform engineering teams
- vendor-neutral recommendations
- practitioner-focused adoption guidance

The CI/CD Cybersecurity Guide addresses a major industry gap: while many organizations deploy CI/CD pipelines, few have a clear framework for securing them end-to-end. The project is intended to become the authoritative security reference architecture for CI/CD pipelines within the Continuous Delivery Foundation ecosystem.

## Project Description
(What it does, why it is valuable, origin and history)

The CI/CD Cybersecurity Guide provides a lifecycle-based security reference model for modern CI/CD environments. It organizes security controls across pipeline phases, including:

- source control protection
- build integrity
- artifact provenance
- deployment governance
- runtime visibility
- vulnerability response workflows
- SBOM lifecycle usage
- identity and access management within pipelines
- policy enforcement automation

The guide maps open-source tools—including CDF-hosted projects, to security control objectives aligned with:

- NIST Secure Software Development Framework (SSDF v1.1)
- SLSA
- Cybersecurity Resiliency Act 
- Emerging AI Security
- Continuous Threat Exposure Management (CTEM) practices


## Background and Context

Over the past year, the CDF CI/CD Cybersecurity SIG has operated as an active working group focused on improving the security posture of modern continuous delivery pipelines. The SIG was formed in response to growing industry concern around software supply chain attacks, increasing regulatory pressure, and the expanding responsibilities placed on DevOps and platform engineering teams.

During its first year, the SIG successfully delivered the **CI/CD Cybersecurity Guide**  
https://cybersecurity.cd.foundation/

The guide is a vendor-neutral, practitioner-focused resource that documents how open-source security tooling integrates directly into CI/CD workflows based on industry-standard frameworks. It reflects the use of open-source tooling that can be adopted in CI/CD pipelines used by organizations running Jenkins, Tekton, Shipwright, Spinnaker and internal developer platforms. The guide focuses on new OS tooling from the OpenSSF, Apache, and other OS foundations.  

With the guide published and in active community use, the SIG believes the initiative has reached sufficient maturity, scope, and sustainability to progress into an official CDF project.

The CI/CD Cybersecurity Guide originated within the Continuous Delivery Foundation CI/CD Cybersecurity SIG as a collaborative effort to:

- document pipeline security requirements
- align CDF ecosystem tooling with SSDF requirements
- improve adoption of secure pipeline architectures
- reduce confusion around software supply-chain security implementation

The guide has evolved into a living reference architecture used by:

- platform engineering teams
- DevSecOps practitioners
- public-sector security programs
- regulated industry adopters
- open-source contributors

## Problem Statement

Why this Guide Now: 
This guide helps DevOps engineers build security-compliant CI/CD pipelines by mapping new open-source automation tools to evolving security frameworks. As security standards evolve, pipeline updates are essential to ensure safer software development. This guide examines the intersection of security tooling and the CI/CD pipeline, highlighting key security practices, tools, and strategies that align with established frameworks, including the Secure Software Development Framework and the NIST Cybersecurity Framework. This guide aligns framework-defined tasks with open-source tools to facilitate their accomplishment, providing a shared orientation model for practitioners as CI/CD systems become more automated and interconnected.

As CI/CD pipelines increasingly incorporate AI - and LLM-assisted workflows, delivery velocity and automation continue to accelerate, placing new pressure on verification, provenance, and control points within the pipeline. This guide treats AI as an accelerator of existing CI/CD patterns—not a separate domain—reinforcing the need for clear, framework-aligned security practices that help practitioners reason about risk as complexity increases.

Modern software delivery environments face several challenges:

- CI/CD pipelines have become a primary attack surface.
- Security guidance is often fragmented, tool-specific, or disconnected from delivery workflows.
- Platform engineering teams are increasingly responsible for embedding security guardrails into internal developer platforms.
- Organizations struggle to translate high-level security requirements into actionable CI/CD implementation patterns.

There is a clear need for a foundation-owned, continuously maintained reference guide that aligns CI/CD security practices with open-source security tooling as delivery models continue to evolve.

## Project Scope

The CI/CD Cybersecurity Guide project will:

- Maintain and evolve the existing cybersecurity.cd.foundation content
- Provide practical guidance for securing CI/CD systems and internal developer platforms
- Map security practices and tooling to pipeline stages and operational workflows
- Reference and integrate CDF-hosted projects where applicable
- Offer architecture diagrams, workflow patterns, and implementation examples
- Support education, adoption, and community contribution


## Non-Goals

This project will not:

- Create or maintain security tooling
- Provide compliance certification or auditing services
- Replace individual project documentation
- Define new frameworks or guidelines


## Statement on Alignment with Foundation Charter’s Mission

The Continuous Delivery Foundation’s mission includes improving software delivery practices through open collaboration, interoperability, and education.

The CI/CD Cybersecurity Guide directly supports this mission by:

- improving trust in CI/CD pipelines
- accelerating adoption of secure continuous delivery practices
- enabling interoperability between CDF ecosystem projects
- providing implementation guidance aligned with government security expectations
- supporting emerging compliance-driven delivery models such as Continuous ATO (cATO)

The guide strengthens the position of CDF as a leader in secure software delivery infrastructure

## Proposed Maturity Level
Incubating (with intent to graduate)

## Link to project's website

- [Homepage](https://cybersecurity.cd.foundation/)
- [SIG Page](https://cd.foundation/cybersecurity/)

## Proposing Group
CDF CI/CD Cybersecurity Special Interest Group (SIG)

## Proposed TOC Sponsor
Tracy Ragan and Steve Taylor

## Proposed Governance
CI/CD Technical Oversight Committee (TOC)

## Link to Current Code of Conduct

The project adopts the Continuous Delivery Foundation Code of Conduct:

https://github.com/cdfoundation/community/blob/main/CODE_OF_CONDUCT.md

## CI/CD Cyberseucrity Guide License

[Apache](https://github.com/cdfoundation/CICD-Cybersecurity/blob/main/LICENSE)

## Project Governance

https://github.com/cdfoundation/CICD-Cybersecurity#governance

## Contributing Guidelines 

- [Contributing Guidelines](https://github.com/cdfoundation/CICD-Cybersecurity/blob/main/CONTRIBUTING.md)

## List of Project's official communication channels 

- [Slack](https://cdeliveryfdn.slack.com/archives/C082V7WN9K4)
- Mailing List: CICD-Cybersecurity@lists.cd.foundation

## Source Control

https://github.com/cdfoundation/CICD-Cybersecurity/

## Issue Tracker

https://github.com/cdfoundation/CICD-Cybersecurity/

## Infrastructure Needs
Netlify for hosting the Guide's webpage. (estimated cost $10 monthly)

## External Dependencies

- Hugo / Golang
- GitHub

## Initial Committers

- Tracy Ragan @Tracyragan
- Steve Taylor @sbtaylor15
- Ann Marie Fred @amfred
- Kate Scarcella @k8scarcella
- Kris Stern @krisstern

## Leadership Team and Decision-Making Process

Chairperson: Kate Scarcella (https://www.linkedin.com/in/k8scarcellaexodus/)

The CI/CD Cybersecurity Guide operates under the governance of the Continuous Delivery Foundation (CDF) CI/CD Cybersecurity SIG, using a consensus-driven open governance model to guide its evolution and direction. Major updates to the guide are proposed and refined through SIG discussions, implemented through pull requests, and validated via contributor review cycles, with Technical Oversight Committee (TOC) involvement where appropriate. This collaborative process ensures transparency in decision-making, maintains vendor neutrality, and reinforces strong community ownership of the project as it grows within the CDF ecosystem.

## Project Deliverables

- Versioned releases of the CI/CD Cybersecurity Guide
- Maintained website and documentation repository
- Roadmap-driven content updates
- Community contribution framework
- Reference architectures and diagrams
  
## Initial Roadmap (High-Level)

### Phase 1
- Transition guide to CDF project governance
- Establish maintainers and a contribution model
- Stabilize structure and terminology
- Define release cadence

### Phase 2
- Map tooling to the Cybersecurity Resiliency Act (CRA)
- Add AI lifecycle patterns
- Deepen references to CDF ecosystem projects

### Phase 3
- Ongoing community-driven updates
- Regular content refresh aligned to industry changes
- Build more features into the site.
  - Advance searching / Tag/Filter System
  - Seach History and Bookmarking
  - Breadcrumbs
  - Phase Dashboard Cards

## Community and Sustainability

The project will:

- Operate under open governance
- Welcome contributors across the CDF ecosystem
- Maintain a transparent roadmap planning
- Encourage participation from practitioners, platform engineers, and project maintainers
- Provide continuity beyond the original SIG membership


## Success Metrics

- Active maintainers and contributors
- Regular content releases
- Adoption and references across CDF events and materials
- Community engagement and feedback
- Alignment with evolving CI/CD and platform engineering practices


## CI/CD Cybersecurity Community
The CI/CD Cybersecurity community meets bi-weekly for an overall project status meeting.  Guide content, format, and expansion are the topics of these meetings. 

- [General Meeting Minutes](https://docs.google.com/document/d/1DXgvzQzMRqvvryB_W0Te4foA0Loh5WvwKojEEa7W0ak/edit?usp=sharing)
- [Meeting Recordings Youtube](https://www.youtube.com/watch?v=Q8m067Z35uE&list=PL2KXbZ9-EY9TIHn457fyjjrUcM5fSszy8)


## Guide Disclaimer - On first page of guide: 

Disclaimer
This CI/CD Cybersecurity Guide is meant to serve as a reference point. Users are strongly encouraged to review these recommendations to fit their specific project security requirements and organizational standards. By using this guide, you agree to do so at your own risk and discretion. The Continuous Delivery Foundation and the Linux Foundation shall not be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this guide, even if advised of the possibility of such damage.



