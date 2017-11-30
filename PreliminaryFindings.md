# Data Federation - Preliminary Findings

## TL;DR
After interviewing many teams and experts who perform data aggregation across complex organizational boundaries,
it is clear there is a demand for better resources and tooling for these efforts. We recommend
exploring the space further.

## What is a "data federation"?
We use the term data federation to refer to data aggregation efforts that cross organizational
or institutional boundaries, such as when the federal government collects data from states, where states collect from municipalities, OMB collects data from agencies, etc. This type of data collection, in which the aggregator has limited authority over the owners of the data, is very common in government due to it's decentralized structure, and poses special challenges relative
to the more common corporate authority structure.

## Our Process
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
through compliance or cooperation, they may not have the capital (in time, money or expertise) to do so. This is a more
salient problem when the organization is smaller and unlikely to already maintain technical staff, for example
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

## Recommendations
We recommend continuing to explore two principle questions to promote expertise at these efforts
across government. First, Where should resources for these efforts come from?
One thing that is clear from our exploration so far is that there is great need and benefit to 3rd party
coordinators to promote the data standardization, consensus building, and tooling, but that generally the
parties that most benefit from this coordination are unwilling or unable to invest in it. So, what is the best
home for these efforts- is it with a corporation, non-profit, standards body, or some part of the federal government?
The answer will likely vary by the type of effort, but since these efforts are for the public good and
rely on cooperation rather than competition, normal market dynamics cannot provide the support required.

Second, given that these efforts require a capital investment to succeed, what is the best path forward to globally
reduce the capital required through improved tooling or other resources? For example, I could easily imagine building
out a data federation toolkit with standards for generating schemas, validating, submission / aggregation, etc..
Such a toolkit could follow a similar model as the U.S. Web Design Standards - being open source, but supporting itself
through consulting engagements that enable enhanced customization.

## Why this matters
Federated datasets are a critical part of government operation, yet there has never been a serious, systemic study
of how to do it better. Government is in the data business, and much of that data gets transferred across
organizational boundaries and assembling it requires careful coordination of many parties, yet there is very little
note sharing about what works, what doesn't, who plays what roles, what resources are required, and how resources are best spent.

We believe a thorough systemic study of this problem could yield solutions in the form of a playbook, technical toolkit, and recommendations for what sort of role the Federal government could play in supporting these efforts.
