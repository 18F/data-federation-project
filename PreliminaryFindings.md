# Data Federation - Preliminary Findings

## Overview
After interviewing many teams and experts who perform data aggregation across complex organizational boundaries,
it is clear there is a demand for better resources and tooling for these efforts. We recommend
exploring the space further.

## What is a "data federation"?
We use the term data federation to refer to data aggregation efforts that cross organizational
or institutional boundaries, such as when the federal government collects data from states, where states collect from municipalities, OMB collects data from agencies, etc. This type of data collection, in which the aggregator has limited authority over the owners of the data, is very common in government due to it's decentralized structure, and poses special challenges relative
to the more common corporate authority structure.

## Why this matters
Federated datasets are a critical part of government operation, yet there has never been a serious, systemic study
of how to do it better. Government is in the data business, and much of that data gets transferred across
organizational boundaries and assembling it requires careful coordination of many parties, yet there is very little
note sharing about what works, what doesn't, who plays what roles, what resources are required, and how resources are best spent.

We believe a thorough systemic study of this problem could yield solutions in the form of a playbook, technical toolkit, and recommendations for what sort of role the Federal government could play in supporting these efforts.


## How we arrived at this conclusion
We have performed 12 interviews so far with experts in these types of efforts, and will likely do a few more in the next
couple weeks. We've spoken with:

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
2. What was impetus or driving force for this effort: policy, user needs, etc?
3. In building ____, what were the biggest challenges, and what went smoothly?
4. What tools and technologies do you use for this effort?
5. Why did you choose this architecture or process. Were others tried, etc?
6. What are the political and organizational dynamics of getting NIEM setup?
7. Who were the relevant stakeholders for this project, how were they identified and convened?
8. Is there anyone else I should speak with to better understand X?

Expert interviews varied slightly by person, but we generally discussed what experience they have with similar efforts, what in their view went well, and what didn't go well.

## What we found so far
The impetus for these types of efforts ranges from top-down policies (e.g., data.gov, code.gov, DATA Act), to
private sector incentives (e.g., Google Transit Feed Specification), and even occasionally passionate
individuals (e.g., OpenReferral). Regardless of the initial reasons for starting an initiative, it's important
to realize that ultimately adoption is driven by cost / benefit analysis at the organizational level.
In the case of mandates, legal or policy requirements are easily ignored or watered down if the cost is
too high or benefit too low. It's also important to note that even if the organization stands to benefit significantly
through compliance or cooperation, they may not have the capital (in time, money or expertise) to do so. This is a more salient problem when the organization is smaller and unlikely to already maintain technical staff, for example
in local government or social services.

In terms of incentives, it's critical that data aggregation efforts either (1) support an new "killer app" that
supports organizations in their mission, or (2) supports the organization's existing workflow. In many interviews,
the Google Transit Feed Specification, which allows governments to publish public transit data so that it can be
consumed by Google Maps among others, was help up as the perfect example of the "killer app." Publishing in the spec
instantly broadcasts the data to the apps that citizens are already using. Municipalities in Connecticut also embrace open data standards, not necessarily for it's value to the public, but because by publishing to a data portal,
their own data can be more easily consumed within their own working processes.

Once incentives are aligned, it's critical to get a few early adopters, and work with them to get something
working end-to-end. The benefits of shipping early and iterating were salient in several projects, particularly
code.gov, data.gov, and DATA Act. One thing that became clear (by both doing it right and doing it wrong), is that
the distinction between policy and technology is extremely difficult to draw. In situations where the
technology and policy were owned by different organizations, for example for DATA Act, tensions arose and there
was high communication overhead. In situations where the policies and technologies coevolved, such as with data.gov
and code.gov, being able to nimbly react both the technology and the policy to user needs and implementation
constraints proved extremely valuable.

After early adopters prove success with the effort, there is generally a gold rush as organizations clamor to
adopt & comply. In this stage, it's generally been fairly easy to keep momentum going, keep interest and funding, etc..

Then after a few years, the honeymoon ends, and organizations stare at years and years of effort to maintain compliance and evolve the schema in order to keep it relevant in a changing world. Organizations really struggle with
maintaining standards, schemas, and tooling over the long term. For many of these efforts, it is still too soon to
tell how the maintenance burden will be handled, but in other cases the loss of a single passionate person
or 3rd party could spell doom for the effort.

## Proposal for Next Steps

We believe the discovery work done so far, which has revealed a long history of, and growing demand for federated data efforts, is sufficient to establish a clear appetite for improved tooling for these efforts across many levels of government. There is also appetite for further research and exploration, however that important work is being actively pursued by non-profits and academia. TTS is in a unique position to invest in the technical infrastructure behind these efforts, and we believe that should be the focus of the next phase of feasibility testing. Work TTS has done so far, in particular work by DATA Act for data validation and ingest, and data.gov for JSON validation and harvesting, could form the basis of an ecosystem of tooling that could greatly accelerate future federated data efforts. Although previous work is open source, it is not engineered for public reuse.

Building reusable tools is difficult because of a catch-22: it is difficult to build reusable tools without a forgiving first adopter, but in any new effort it will rarely be in budget or scope to extract reusable elements from existing solutions. We believe investment from 10x could help break that cycle: the next step should be to identify a new, upcoming federated data effort, and use it as a test case to generalize the work done by previous efforts. The work done in the past needs to be broken into smaller modules, published to package managers, and documented. It will likely also need to be supplemented with new tools or wrappers to provide a compelling product to potential adopters.

One such upcoming federated data effort is the data standards policy itself. In a blissfully ironic twist, the federal data standards policy (A-119), specifies that agencies should provide data on the standards they maintain, but does not define a data standard or method of ingest for that data. We should work with OMB to define a standard, and work with the relevant stakeholder within GSA to be the first adopters of that standard, while building a set of tools to accept, document, and validate the new technology.

## Questions to be answered in the next phase

There are a few key questions the next phase will seek to answer:

1. Is the work done to date in this area possible to make reusable (at the technical level)?
2. Will a brand new use case have enough overlap with previous efforts to take advantage of not just processes, but actual code? 
3. Can a new process / tool built with reusable components meet demands for usability, security, and compliance?
