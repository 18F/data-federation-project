# Data Federation - Preliminary Findings

## Overview
Federated data efforts — those in which a certain type of data is aggregated from many entities across organizational boundaries — have a long history and increasingly important role in critical missions across government. Due to government's decentralized nature, government leaders seeking to collect data frequently do so from organizations they have limited authority over — for example, OMB collecting data from agencies, federal government from states, states from municipalities, etc.. Special problems arise in these situations, since resources, capabilities, and incentives may vary wildly, yet there has been very little systemic support for these efforts. After speaking with leaders of nine such projects, and three additional experts, it is clear that such support is needed and would be welcomed by all levels of government.

We recommend continuing on to a discovery phase, focusing on making capital investments in reusable tooling and processes that will benefit future federated data efforts. We also seek to clarify the federal governments role in these efforts moving forward.

## Why this matters
Federated data efforts play an increasingly important role in laws, policies, and operations across many levels of government. When lawmakers on both sides of the aisles passed the DATA Act in 2014, it wasn't just innovative in its mission (to provide unprecedented transparency in government spending), but also in its methods, which required the creation of a machine-readable data standard and buy-in from every federal agency. The effort required coordination across federal agencies which varied wildly in technical capabilities, and was completed on time and well under budget in 2017. The federal open data policy, along with data.gov, provides a mechanism to streamline the cataloging and discovery of both open and closed data sets across the government. And Open311, a standard API for local government, has enabled an ecosystem of apps to develop around reporting problems such as potholes, streamlining the experience for citizens and cities alike.

Federated data efforts are increasingly seen as an engine for transparency, economic growth, and accountability, yet collecting that data remains a challenge. Despite the fact that efforts of this sort are increasing in frequency, each new effort is still improvising solutions in terms of processes, tooling, and compliance infrastructure. It's time to take this problem seriously and invest in reusable tools and approaches that will streamline federated data efforts in the years to come.  

## How we arrived at this conclusion
We have performed 12 interviews so far with experts in these types of efforts, and will likely do a few more in the next couple weeks. We've spoken with:

### Projects
- **Data.gov**: A catalog of metadata for most Federal datasets
- **Code.gov**: A catalog of metadata for Federal open source code
- **Open Referral**: An effort to provide data exchange formats for social services
- **Open Data Institute**: A non-profit promoting open data that just launched a data standardization research project
- **National Information Exchange Model (NIEM)**: A repository of schemas and governing structure to support cross-domain data sharing.
- **Open311**: An API standard for cities to support common citizen interactions such as pothole reporting.
- **DATA Act**: A statute ordering the creation of a data standard and new publishing process to provide unprecedented auditability of Federal spending data.
- **Data Coalition**: An organization which advocates for open data standards such as the DATA Act.
- **Federal Geographic Data Committee (FGDC)**: A committee which maintains a standard for geographic data.

### Experts
- **Mark Headd**: Current 18F Acquisitions Specialist, former CDO of Philadelphia
- **Tyler Kleykamp**: CDO of Connecticut
- **Andrew Nicklin**: Maintains datastandards.directory, involved with open311, openReferral, many city-level efforts.

For each project interview, we asked:
1. What is ____, in your own words?
2. What was the impetus or driving force for this effort: policy, user needs, etc?
3. In building ____, what were the biggest challenges, and what went smoothly?
4. What tools and technologies do you use for this effort?
5. Why did you choose this architecture or process. Were others tried, etc?
6. What are the political and organizational dynamics of getting ____ setup?
7. Who were the relevant stakeholders for this project, how were they identified and convened?
8. Is there anyone else I should speak with to better understand ____?

Expert interviews varied slightly by person, but we generally discussed what experience they have with similar efforts, what in their view went well, and what didn't go well.

### What potential users are saying

In speaking with these individuals and reviewing open source repositories, a few things became clear. Although there is a lot of variety in these efforts, there is a lot of commonality as well, and everyone we spoke with was very supportive of trying to get more support for efforts like these moving forward. For example, every effort needs to develop some sort of schema for the data, provide a mechanism to validate against that schema, have it publicly documented, and provide a mechanism for data ingest. The more that can be done to support the infrastructure of these projects, at both the technical and procedural levels, the more it will enable federated data efforts in the future. Essentially every effort so far is starting from scratch in terms of doing user research, developing a schema, validating data, aggregating the data, getting approvals, building UIs, and developing processes to support the aggregation. The domain is ripe for investment into reusable tools and frameworks of thinking.

One thing we learned is that several resources are undertaking research in this domain — namely, Andrew Nicklin is compiling data standards in datastandards.directory, and the Open Data Institute is undergoing a multi-year research effort into building and maintaining open data standards. Although there is a difference between data standards and federated data efforts (since efforts may be federated without adopting an open standard), it's encouraging that the domain is getting more attention.

Another common theme is the confusion around ownership around these efforts. Several leaders interviewed see this work as public infrastructure for the 21st century, but it's not always clear who should be owning and maintaining these efforts. Although specific policies and laws can make roles clear in specific instances, overall the policies around data standards are confusing and ambiguous, leaving gaps that need to be filled in an ad-hoc manner.

## What we found so far
The impetus for these types of efforts ranges from top-down policies (e.g., data.gov, code.gov, DATA Act), to
private sector incentives (e.g., Google Transit Feed Specification), and passionate non-profits (e.g., OpenReferral, Open311). Regardless of the initial reasons for starting an initiative, it's important to realize that ultimately adoption is driven by cost / benefit analysis at the organizational level. In the case of mandates, legal or policy requirements are easily ignored or watered down if the cost is too high or benefit too low. It's also important to note that even if the organization stands to benefit significantly through compliance or cooperation, they may not have the capital (in time, money or expertise) to do so. This is a more salient problem when the organization is smaller and unlikely to already maintain technical staff, for example in local government or social services.

In terms of incentives, it's critical that data aggregation efforts either (1) support a new "killer app" that supports organizations in their mission, or (2) supports the organization's existing workflow. In many interviews, the Google Transit Feed Specification, which allows governments to publish public transit data so that it can be consumed by Google Maps among others, was held up as the perfect example of the "killer app." Publishing in the spec seamlessly integrates the data into the apps that citizens are already using. Municipalities in Connecticut also embrace open data standards, not necessarily for it's value to the public, but because by publishing to a data portal, their own data can be more easily consumed within their own working processes.

Once incentives are aligned, it's critical to get a few early adopters, and work with them to get something working end-to-end. The benefits of shipping early and iterating were salient in several projects, particularly code.gov, data.gov, and DATA Act. One thing that became clear (by both doing it right and doing it wrong), is that the distinction between policy and technology is extremely difficult to draw. In situations where the technology and policy were owned by different organizations, for example with the DATA Act, tensions arose and there was high communication overhead. In situations where the policies and technologies coevolved, such as with data.gov and code.gov, having both the technology and the policy able to nimbly react to user needs and implementation constraints proved extremely valuable.

After early adopters prove success with the effort, there is generally a gold rush as organizations clamor to adopt & comply. In this stage, it's generally been fairly easy to keep momentum going, keep interest and funding, etc..

Then after a few years, the honeymoon ends, and organizations stare at years and years of effort to maintain compliance and evolve the schema in order to keep it relevant in a changing world. Organizations really struggle with maintaining standards, schemas, and tooling over the long term. For many of these efforts, it is still too soon to tell how the maintenance burden will be handled, but in other cases the loss of a single passionate person or 3rd party could spell doom for the effort.


## Proposal for Next Steps

We believe the discovery work done so far, which has revealed a long history of, and growing demand for federated data efforts, is sufficient to establish a clear appetite for improved tooling for these efforts across many levels of government. There is also appetite for further research and exploration, however that important work is being actively pursued by non-profits and academia. TTS is in a unique position to invest in the technical infrastructure behind these efforts, and we believe that should be the focus of the next phase of feasibility testing. Work TTS has done so far, in particular work by DATA Act for data validation and ingest, and data.gov for JSON validation and harvesting, could form the basis of an ecosystem of tooling that could greatly accelerate future federated data efforts. Although previous work is open source, it is not engineered for public reuse.

Building reusable tools is difficult because of a catch-22: it is difficult to build reusable tools without a forgiving first adopter, but in any new effort it will rarely be in budget or scope to extract reusable elements from existing solutions. We believe investment from 10x could help break that cycle: the next step should be to identify a new, upcoming federated data effort, and use it as a test case to generalize the work done by previous efforts. The work done in the past needs to be broken into smaller modules, published to package managers, and documented. It will likely also need to be supplemented with new tools or wrappers to provide a compelling product to potential adopters. It should also be noted that a previous 10x phase 1 project, the Generic Data Validation Platform, supported these same conclusions, and could be subsumed by this effort.

One such upcoming federated data effort is the data standards policy itself. In a blissfully ironic twist, the federal standards policy (A-119), specifies that agencies should provide an inventory of the standards they use and justifications for government-unique standards, but it does not define a data standard or method of ingest for that inventory. We should work with OMB to define a standard, and work with the relevant stakeholder within GSA to be the first adopters of that standard, while building a set of tools to accept, document, and validate the new technology. If there are problems in getting buy-in from OMB on this particular issue, we can work with them to identify another one or, in the worst case scenario, proceed independently to refactor previous tooling based around scenarios from our case studies.

Another goal of the next phase would be to help identify ways to clarify roles & responsibilities for data standards efforts at the federal level, to clarify authorities in this domain.

## Questions to be answered in the next phase

There are a few key questions the next phase will seek to answer:

1. Is the work done to date in this area possible to make reusable (at the technical level)?

Oftentimes, things may seem very similar at the procedural or process level, but have subtle differences which make it difficult to share actual code. It is still an outstanding question on whether it is possible to make code reusable for these efforts moving forward.

2. Can a new process / tool built with reusable components meet demands for usability and compliance?

It's one thing to force a new domain to use a certain set of tools, it's another to use those tools and still be able to meet high standards for usability and compliance.

3. What role does the Federal government play in these efforts?

Although specific laws and policies can make the roles clear in specific cases, does policy exist which delegates authority to any agency to pioneer or support these efforts in a more general way?
