# Data Federation Project

The U.S. Data Federation is a project focused on making it easier to collect, combine, and exchange _federated data_ - data from disparate sources. The project is an initiative of the GSA Technology Transformation Services (TTS) [10x](10x.gsa.gov) program, which funds technology-focused ideas from federal employees with an aim to improve the experience all people have with our government. 

## Overview

U.S. government policies, initiatives, and public-facing products and services depend on aggregating and harmonizing data from disparate government sources. The goal of the U.S. Data Federation project is to document repeatable processes, develop reusable tooling, and curate resources to support federated data projects. 

We define a federated data project as an effort in which a common type of data is collected or exchanged across complex, disparate organizational boundaries. For example, federal agencies often need to collect data from state and local governments, other federal agencies, and other data providers. These federated data may be used to support policy or budget decisions, operational efficiencies, or published in aggregate form for other data users. 

Federated data efforts are increasingly seen as an engine for transparency, economic growth, and accountability, yet collecting this kind of data remains a challenge. While this type of data management effort is growing increasingly common in our distributed style of government, each new effort is still improvising solutions in terms of processes, tooling, and compliance infrastructure. Many of these federated data efforts face common requirements and common challenges, but lack common resources. 

The United States Data Federation project was conceived in 2016 to address this gap. The project aims to identify common challenges and pain points in federated data efforts and address these needs by curating best practices and resources and developing reusable tooling. The best practices and resources are intended to include guides and repeatable processes around data governance, organizational coordination, and standards development in federated environments. The reusable tools are intended to include capabilities around data validation, automated aggregation, and the development and documentation of data specifications.   

## Milestones

**Phase 1** (Fall 2017)

Team: Phil Ashlock, Anthony Garvan

-   Interviewed a variety of distributed data management projects and synthesized findings in a [Data Federation Framework](<https://github.com/18F/data-federation-report/blob/master/DataFederationFramework.md>). 

-   Created a placeholder for future web content at federation.data.gov

-   Pitched for Phase 2 funding based on finding that reusable tooling and processes would benefit future federated data efforts

**Phase 2** (Spring 2018)

Team: Phil Ashlock, Catherine Devlin, Anthony Garvan, Chris Goranson, Joe Krzystan

-   Prototyped a reusable data validation tool that allows users to submit data via a web interface or API to be validated against a set of customizable rules in real time

-   Partnered with the USDA Food & Nutrition Service (FNS) to adapt this tool for the FNS-742, a form that collects verification data for the National School Lunch Program 

-   Pitched for Phase 3 funding to further develop the tool, implement it with FNS, and conduct outreach to identify other partners and other opportunities for reusable tools  (Phase 2 Final Presentation)

**Phase 3** (December 2018-June 2019)

Team: Phil Ashlock, Mike Gintz, Mark Headd, Ethan Heppner, Julia Lindpaintner, Amy Mok

-   Developed Phase 2 prototype into Reusable Validation and Aggregation Library ([ReVAL](https://github.com/18F/ReVAL)) with a focus on API-based usage

-   Worked with FNS to develop ReVAL's first custom manifestation for FNS-742 as the [FNS Data Validation Service](https://github.com/18F/usda-fns-ingest)

-   Validated demand for ReVAL and identified future partners 

-   Continued to identify common needs and useful reusable resources for data efforts through outreach and presentations to the Data Exchange Community of Practice, Interagency Working Group on Open Data, VA Open Data Working Group, and others

-   Began building a community around a shared need for knowledge-sharing across data efforts in government

-   Protect against redundancy by aligning the efforts of the U.S. Data Federation with other efforts across government, such as the work of the Federal Data Strategy and the mandates of the Evidence Act and Open Government Data Act 

-   Pitched for Phase 4 funding to leverage the completion of ReVAL and the momentum of the U.S. Data Federation work to support a long-term vision and strategic plan for a user-centered, maximally-effective resources.data.gov

## Recommendations

The recommendation in the pitch for Phase 4 funding was to take advantage of a unique opportunity: government-wide efforts to support open data and federated data efforts are converging at GSA and within data.gov in particular. Rather than limiting Phase 4 to the completion of ReVAL, we recommended also using Phase 4 to unite the efforts behind the U.S. Data Federation and resources.data.gov. The vision for Phase 4 is to use the learnings, resource development model, momentum, and network of the U.S. Data Federation to build a user-centered resources.data.gov that helps data practitioners navigate the landscape of data standards, tools, and other resources. 

## Next steps

Phase 4 work has commenced as of October 2019. Staffed with a full-time UX designer (and project lead) and part-time strategist, the initial weeks of the project will focus on understanding the stakeholder landscape and external mandates for resources.data.gov, re-establishing contact with project partners, and identifying key deliverables for Phase 4.

## References and deliverables

**Phase 1**

- [Interview notes](https://github.com/18F/data-federation-report/issues?utf8=%E2%9C%93&q=is%3Aissue+interview)

- [Preliminary Findings](https://github.com/18F/data-federation-report/blob/master/PreliminaryFindings.md)

- [US Data Federation Framework](https://github.com/18F/data-federation-report/blob/master/DataFederationFramework.md) (includes [Data Federation Maturity Model](https://github.com/18F/data-federation-report/blob/master/DataFederationFramework.md#the-data-federation-maturity-model) and [Data Federation Playbook](https://github.com/18F/data-federation-report/blob/master/DataFederationFramework.md#the-data-federation-playbook))

**Phase 2**

- [Final presentation (PDF)](assets/US-Data-Federation-Phase-II-Final.pdf)

- Prototype [Django Data Ingest Tool](https://github.com/18F/ReVAL) 

**Phase 3**

- [Project overview (PDF)](assets/Project-Overview-for-Partners-Stakeholders.pdf)

- [Project overview with FNS case study (PDF)](assets/Project-Overview-with-FNS-Case-Study.pdf)

- [Project overview presentation (PDF)](assets/US-Data-Federation-Project-Intro.pdf)

- [Webinar via Digital.gov on April 17, 2019](https://youtu.be/r4XUu2MLrDo) // [Slides (PDF)](assets/Digital.gov%20Presentation%20%E2%80%94%20US%20Data%20Federation.pdf)

- [Phase 4 pitch presentation (PDF)](https://github.com/18F/data-federation-project/blob/master/assets/10x%20Data%20Federation%20Phase%204%20pitch.pdf) 

### Related repositories

There are several repositories that contain code that is a part of this project.

* Github repo for the US Data Federation website: https://github.com/GSA/us-data-federation

* Github repo for ReVAL, the US Data Federation's first reusable tool for data validation and aggregation: https://github.com/18F/ReVAL

* Github repo for the FNS Data Validation Service, which uses ReVAL to check submitted FNS-742 data against a set of centralized validation rules via API: https://github.com/18F/usda-fns-ingest

* Github repo for the Workzone Data Exchange (WZDx) Validator, which uses ReVAL to perform JSON Schema validation against the WZDx v1.1 specification: https://github.com/18F/usdot-jpo-ode-workzone-data-exchange

*Other repos referenced:*

* https://github.com/18F/couch-rules-engine

* https://github.com/18F/goodtables-gov

* https://github.com/18F/usdot-jpo-ode-workzone-data-exchange

* https://github.com/18F/cx-cap-goal
