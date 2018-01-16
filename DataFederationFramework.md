# The Data Federation Framework (alpha)

## Summary
We define a data federation as an effort where a certain type of specifiable data is collected across complex many organizational boundaries. This could be, for example, when the federal government collects data from states, or states from municipalities, or even when the Office of Management and Budget collects data systematically from many federal agencies. This type of data sharing effort is common in our distributed style of government, but we believe it has not been given the systemic investigation and infrastructural support it deserves- currently each such effort is treated as an isolated instance, with little sharing of tools or lessons from one effort to the next. The goal of the U.S. Data Federation project is to fill that gap, providing a common language and framework for understanding these efforts, and (in the future) a toolkit for accelerating the implementation of these efforts.

We interviewed twelve leaders of federated data projects, and seven additional experts from government, academia, and the private sector who have been influential in shaping or understanding these efforts. We developed a framework for understanding the spectrum of these efforts in along four axes: Community, Specification, Application, and Mandate. We found that the most successful efforts are those in which all four of these axes are developed iteratively and simultaneously.

## What We Did
Projects We Interviewed:
- [DATA ACT](https://en.wikipedia.org/wiki/Digital_Accountability_and_Transparency_Act_of_2014), a 2014 law mandating expanded and standardized reporting of financial data for federal agencies.
- [data.gov.ie](https://data.gov.ie/data), the open data port for Ireland.
- [data.gov](https://www.data.gov), the open data portal for the United States.
- [code.gov](https://code.gov/), a searchable directory of open source code made public by the federal government.
- [Voting Information Project](https://www.votinginfoproject.org/) helps voters find information about their elections with collaborative, open-source tools.
- [Open Civic Data](http://opencivicdata.readthedocs.io/en/latest/index.html), an effort to define common schemas and provide tools for gathering information on government organizations, people, legislation, and events.
- [opendataphilly.org](https://www.opendataphilly.org/), the open data portal for Philadelphia.
- [OpenReferral](https://openreferral.org/), dedicated to developing open standards and platforms for making it easy to share and find information related to community resources.
- [Open311](http://www.open311.org/), A collaborative model and open standard for civic issue tracking.
- [National Information Exchange Model (NIEM)](https://www.niem.gov/), a common vocabulary that enables efficient information exchange across diverse public and private organizations. NIEM can save time and money by providing consistent, reusable data terms and definitions, and repeatable processes.
- [Federal Geographic Data Committee](https://www.fgdc.gov/)

We also researched the Google Transit Feed Specification.

Other Experts we Spoke With
- Rachel Bloom, who researched open data standard adoption for her thesis. Currently at [GeoThink](http://geothink.ca/).
- [Andrew Nicklin](https://govex.jhu.edu/author/anicklin/), Director of Data Practices at Johns Hopkins Center for Government Excellence
- [James McKinney](http://www.jamespetermckinney.com/), Senior Data Standard Specialist at Open Contracting Partnership
- [Data Coalition](https://www.datacoalition.org/), who advocates on behalf of the private sector and the public interest for the publication of government information as standardized, machine-readable data.
- [Open Data Institute](https://theodi.org/), which connects, equips and inspires people around the world to innovate with data.
- [Mark Headd](https://www.linkedin.com/in/markheadd), current 18F acquisitions specialist and former Philadelphia CDO.
- [Wo Chang](https://www.nist.gov/people/wo-l-chang), Co-chair of the NIST Big Data Working Group.
- Tyler Kleykamp, Chief Data Officer of Connecticut, who runs the [Connecticut Open Data Portal](https://data.ct.gov/) and maintains this [list](https://github.com/OpenDataCT/state-federal-datasets)
of datasets states must report to the Federal government.

## Our Takeaway: The Data Federation Framework

Successful execution of a federated data effort is largely a question of incentives and resources. Developing, and complying with, a new standard for data submission takes considerable time, effort, and expertise, and will only be possible to sustain with a large number of motivated individuals who have both the ability and the capacity to execute on a long term vision. However, it is difficult, and unwise, to immediately allocate vast resources to a new federated data effort- the effort may be easier than anticipated, or harder, or impossible, for a variety of reasons. We have observed that the most successful of these efforts simultaneously and iteratively develop the maturity of the effort along four axes: Community, Specification, Application, and Mandate. If done properly, these four dimensions work in concert to create a virtuous cycle of more participation, enthusiasm, and resources allocated to the project over time.


|:----------------:|:--------------:|:----------------:|:-------------:|
| **Impetus**      | Grassroots     | Policy           | Law           |
| **Community**    | First Adopters | Trending         | Maintenance   |
| **Specification**| Dictionary     | Machine Readable | Standardized  |
| **Application**  | Alpha          | Beta             | Production    |

**Mandate**: The first spark behind any federated data effort is some sort of impetus. This might be a shared understanding of a problem, where a grassroots community comes together and decides to act (for example, with the law enforcement community creating NIEM). Or it could be a policy, where a central authority (e.g., OMB, or a state government) decides to require compliance of a certain sort through an official policy (for example, with the data.gov). Or, it could be as formal as a law, such as in the case of the DATA Act. The more formal the mechanism, the greater force permanence it has, and thus the harder it is to adapt during implementation. For both policies and laws, it is critical to leave all technical decision making to the implementation team. Never specify a technical standard in policy or law. For example, it can be very helpful to dictate that a standard must be machine readable, but specifying that the standard must be written in XML can have complex and unforeseen consequences. In extreme cases you can specify data elements to provide, but it is best to avoid doing so. In writing a policy or law, focus on processes and outcomes, not on implementation details. Never attempt to fully dictate a data standard in policy or law. For example, you can say that the standard must be machine readable, extensible, and developed alongside a web application with user feedback, but it would not be helpful to say that the standard should be in XML, that states can modify as needed, and that it must be showcased in a user-friendly web application. It's also important to recognize that data standards need maintenance and adaptation over time: it's wise to specify an annual or biannual review of the standard itself to make sure the data is still providing value.

**Community**: For a federated data effort, you have two communities you need to keep happy: the data owners, or those who need to do the work to adopt the standard, and the community of users, or consumers of the aggregated data. It is the job of the project team (a small team dedicated to driving adoption) to keep this community excited and encouraged.

When executing on a federated data effort, it's important to not expect or plan for immediate compliance of the entire community of data owners. Instead, select 2-3 early adopters: good-faith partners who are excited about helping. One partner is not enough to generalize on, and over 3 partners would begin to overburden the project team. Once those early adopters have been identified, help them implement a draft of the standard in a high touch fashion. This means working with them side by side to implement it, or even have the project team implement it themselves in order to demonstrate feasibility and be able to show them how it works. The project's team relationship with the early adopters is critical and bidirectional: the implementation details and the standard itself needs to be adapted to be user friendly for data owners, and those owners must also learn about why the standard is helpful to a broader audience. Typically data that is being collected is already in use by the communities most relevant to the data owners, and it requires a shift in mindset to invest in making it more broadly available. For example, for the Voting Information Project, counties typically already publish their polling locations and ballot information on their website. Without a standard reporting format, however, it was nearly impossible for citizens to find. Thus, the project team was responsible for conveying to the owners that problem of scale, and helping them understand the standard. And for the DATA Act, for example, the project team quickly realized that agencies were most comfortable working with CSV (comma separated value) format. Rather than try to teach them all to adhere to an XML-style format the machine readable specification was written in, they developed a parallel standard for the CSV format. Once the early adopters have had success, it's time to roll out the larger standard. Since the first-mover risk has been absorbed, typically the effort will start trending in the larger community, who now has use cases to point to, people to talk with, and code to look at to help them comply. Once adoption is complete or plateaus, the standard enters the maintenance phase, where ownership problems begin to be salient. Often the trending phase is accompanied by influxes of excitement, talent, press, and funding. After a few years all of those may lessen, and it becomes important to establish long term mechanisms for maintaining the standard itself and the processes around compliance. If the standard has become a normal part of operations, the maintenance phase can be part of the normal budget. If it continues to be "tacked on" to normal operations, the effort is at risk of fizzling out.

It is also important to be in touch with the community of data consumers from the very beginning. This could be journalists, scientists, citizens, decision makers in the org, etc.. The reason for this is two-fold: first, as the ultimate users of the data, it is important that their feedback be integrated early and often. Second, their positive feedback and involvement will help incentivize the data owners, who are embarking on a long an uncertain journey.

**Specification**: The specification itself is responsible for communicating to data owners what data needs to be provided and how it should be formatted. At the lowest level of formality, project teams can start with a description of fields (a data dictionary). These should be detailed, should not use acronyms, should include exact field / column names, and include examples of compliant data. If you have a simple data standard, for example a single CSV or sets of CSVs, this level of detail may be sufficient. For example, the Google Transit Feed Specification, which is among the most successful federated data efforts, does not publish a machine readable standard, but rather has thorough documentation detailing the requirements and fields in language the domain experts in local government would understand. A more formal specification should be machine readable: in this case, not only is the data dictionary well documented as detailed above, but the standard itself can be used to automatically perform simple validations against the data. This level of specificity can help reduce compliance burden by increasing clarity. For example, a data dictionary might have a field called "start_date" and describe that it's the starting date of an election, but a machine readable version would be forced to clarify that the format of the date should look like 2018-01-15, which reduces potential for wasteful back & forth or downstream data integrity problems. For specifications that must map to many-to-one or many-to-many relationships, a machine readable format (e.g., JSON Schema or XML Schema) is strongly preferred, even as a first iteration. That machine readable schema can be versioned as well. Over many years of stability and adoption, it may make sense to promote the machine readable schema into a full standard, adopted by ISO, for example. This level of maturity is rare, but can be helpful to promote stability. Working with standards bodies is generally a complex endeavor, and thus not recommended until the standard has a proven user base and community.

**Application**: It is only very rare cases where raw data published online will be compelling enough to drive adoption of the user community. Generally that community will have richer requirements beyond and supporting the data itself. For example, they may want to be able to search it or visualize it easily, or access it programmatically through an Application Programming Interface (API). Since that user community is ultimately driving value for the entire effort, it's important to be developing an application in concert with the standard to demonstrate the value of the data. For example, with code.gov, the project team developed an alpha version of code.gov in just a few months, showcasing the work of some of the early adopters. They quickly earned over 100,000 viewers, which helped ignite excitement for the effort across government, and provide countless valuable perspectives on how the data would be used and what, exactly, the value was they should be targeting. Often for federated data efforts, the value proposition itself is not fully known, but rather hypothesized: developing a "killer app" that showcases that value directly is a critical part of the effort. Similarly, the application helps inform the specification itself: perhaps some fields are found to be unnecessary, or incorrectly formatted, or missing. This application provides important fuel for incentivizing adoption. For example, for the Google Transit Feed Specification, having local citizens be able to search through their city's public transit routes on Google Maps provided clear and tremendous value to potential adopters. As is industry best-practice, it's important to develop this application iteratively, starting with a small subset of features, releasing publicly to early adopters in a alpha phase, performing more extensive testing in a beta phase, and adding increased stability in the production phase.

## Discussion

### What Works Well
- Killer App (Google Transit)
- General Policy (Code.gov), with specifications to make a machine readable standard (but not to specify the standard)
- Single empowered project team (code.gov)
- Dogfooding (municipalities, geo)
- Demonstrated demand (google search results- VIP)
- Financial Incentives ()
- Data reporting as part of normal workflow, not "tacked on"
- Start with simple tech (don't assume big data / complex architecture like microservices). If a CSV will
work, don't do json or XML. If a static app will do, don't use a database.
- Early adopters / "shining examples" to drive adoption. Both peer pressure and practical - can point to repos, discuss challenges, etc.
- tooling to aid in reporting (e.g., inventory.data.gov, validators, human readable documentation)

### What Causes Issues
- conveying scale (VIP)
- Resources (OpenReferral)
- expertise (States / Municipalities)
- authority (for large orgs)
- policies / laws that recommend general guidelines, but leave authority up to states / districts for details, miss a huge opportunity. Should dictate machine readable. restaurant inspections / FDA (Andrew Nicklin)
- Standards or technologies written into law.

- highlight incentives
## Final Thoughts

## Helpful Resources
- json Schema standard & e-book
- XML data types
- CKAN
- datastandards.directory
- [State-Federal Datasets](https://github.com/OpenDataCT/state-federal-datasets)
