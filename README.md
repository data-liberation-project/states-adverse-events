# Adverse Events State by State Data

This data is part of [the Data Liberation Project's patient safety data initiative](https://www.muckrock.com/project/patient-safety-1250/). We're requesting and publishing datasets about health care delivery at both the federal level and state by state.

Adverse events are a core piece of patient safety. They’re medical errors and their consequences, an idea that captured the field of healthcare’s attention after the[ Institute of Medicine’s 1999 report](https://pubmed.ncbi.nlm.nih.gov/25077248/) that laid the problem of patient harm bare. The report sparked decades of nationwide efforts, but a recent[ Office of Inspector General](https://oig.hhs.gov/reports/featured/adverse-events/) (OIG) report[ still found](https://oig.hhs.gov/reports/all/2025/the-patient-safety-organization-program-key-barriers-impeding-nationwide-progress-toward-reducing-patient-harm-in-hospitals/) that “patient harm events in hospitals remain a serious concern.”

## Data

An[ adverse event](https://psnet.ahrq.gov/primer/adverse-events-near-misses-and-errors) is a term for the types of harm that can happen during medical care like mistakes in surgeries or hospital-induced infections. They’re injuries that happen as a result of medical care, not due to the patient’s underlying injury or disease.

[An OIG survey found](https://oig.hhs.gov/reports/all/2025/hospitals-reported-few-captured-patient-harm-events-to-cms-and-states/) that 26 states and the District of Columbia had reporting requirements for adverse events.[ We’ve filed requests](https://www.muckrock.com/project/dlp-patient-safety-1250/) to over 30 states so far to find out which have reporting requirements and provide records in public records requests.

The data from each state provide slightly different variations or variables but have a few things in common: 
- Each row is an adverse event
- Each adverse event has a type or category for the harm that occurred
- Each adverse event has a date
- Each adverse event has a facility or location


### Summaries of states that have returned useful data

#### California
- Timeframe: January 2023 - December 2024 (though [we requested a decade of data more](https://www.muckrock.com/foi/california-52/aer-ca-dept-of-public-health-215077/))
- Number of rows: 4, 682
- Important variables:
    - `recvdate` - date given to the event in the data, could be the day the event was recorded or received and not the date of the event itself
    - `intakeid` - could be the unique id of the event
    - `adverse_event` - general description of the event
    - `finding_detail`- whether the event was "substantiated" or "unsubtantiated"
    - `name` - name of the facility
    - `aspen_facid` - facility id

#### Colorado
- Timeframe: January 2013 - December 2024
- Number of rows: 63, 016
- Important variables:
    - `facility_name` - name of the facility
    - `bed_license_total` - licensed amount of beds, which could be useful for a rough rate
    - `owner_company` - company that owns the hospital, which could be useful for digging into trends in hospitals owned by same overarching company
    - `occurence_id` - could be the unique id of the event
    - `type_of_occurence` - the type of adverse event
    - `occurence_date` - date given to the event in the data
    - `occurcence_description` - free text description events
        - **These are very detailed descriptions that would be critical for reporting**, but we only received them for years 2023 and 2024. When we requested a decade more of data, we agreed to leave this aside because the agency told us "the cost and processing time will be significant" for a "manual review of over 50,000 occurrence descriptions." But that could be revisited or a future request could be made for the occurence descriptions of only some types of requests.

#### Washington
- Timeframe: 2014 - 2025
- Number of rows: 188,160
- Important variables:
    - `facility_name` - name of the facility
    - `event_type` - grouping for adverse types
    - `adverse_event` - more specific adverse event type
    - `facility_size` - could be total number of licensed beds, useful for a rough rate
    - `year` - year event took place in; we didn't receive dates for events in this dataset

#### Michigan 
- Timeframe: January 2023 - December 2024
- Number of rows: 11, 980
- Important variables:
    - **This data seems to be only events that [happened at Michigan's state-owned mental health hospitals](https://www.muckrock.com/foi/michigan-117/aer-mi-department-of-health-and-human-services-208166/)** and could be worth requesting broader data
    - `event_type` - grouping for adverse types
    - `date_of_incident` - date given to the event in the data

## Caveats and Limitations

In each state, it’s important to keep in mind three major limitations of this data:

1) Each state’s reporting requirements are different, so the data reported are a result of the requirements and the purpose they serve for that facility or state. Some facilities may report only major adverse events, others may have detailed state requirements beyond major events, like[ Pennsylvania](https://patientsafety.pa.gov/PA-PSRS/Pages/PAPSRS.aspx?t=papsrs) or[ California](https://www.cdph.ca.gov/Programs/CHCQ/LCP/Pages/Reportable-Adverse-Events.aspx).
2) Even if the state has detailed requirements, the data are still self-reported and subject to the same risks of omission and bias of all self-reported data.
3) Without more data on the facilities themselves, comparing facilities across a state presents confounding variables that could increase the number of adverse events it reported, such as the average length of stay for a patient, the number of beds in the hospital or the age and health of the population the facility serves. Even a better culture of reporting could cause higher rates of adverse events that make a facility stand out when its actual number of events isn’t higher than other facilities.

### First questions to ask the data for each state
- What types of events are most common? How could this reflect the reporting requirements in the state?
- What types of facilities have the most adverse events? Is there data available on the size of the facility or population it serves?
- What do experts say about the above two questions in relation to broader changes in healthcare, like shortages of staff or[ COVID’s strain on resources](https://www.startribune.com/hospital-adverse-events-rose-during-pandemic/600195240)?



## Requests

| Jurisdiction | Agency | Status | Request Link |
|---|---|---|---|
| Alabama | Alabama Medicaid Agency | Fix Required | [MuckRock request](https://www.muckrock.com/foi/alabama-159/aer-al-medicaid-agency-207530/) |
| Arkansas | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/arkansas-114/aer-ar-dept-of-health-207532/) |
| California | California Department of Public Health | Completed | [MuckRock request](https://www.muckrock.com/foi/california-52/aer-ca-dept-of-public-health-207525/) |
| California | California Department of Public Health | Awaiting Response | [MuckRock request](https://www.muckrock.com/foi/california-52/aer-ca-dept-of-public-health-215077/) |
| Colorado | Department of Public Health and Environment | Completed | [MuckRock request](https://www.muckrock.com/foi/colorado-127/aer-co-dept-of-public-health-and-env-207526/) |
| Colorado | Department of Public Health and Environment | Completed | [MuckRock request](https://www.muckrock.com/foi/colorado-127/aer-co-dept-of-public-health-and-env-215078/) |
| Connecticut | Department of Public Health | Awaiting Response | [MuckRock request](https://www.muckrock.com/foi/connecticut-53/aer-ct-dept-of-public-health-207527/) |
| Delaware | Department of Health and Social Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/delaware-236/aer-de-dept-of-health-and-social-services-207533/) |
| Delaware | Department of Health and Social Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/delaware-236/aer-de-dept-of-health-and-social-services-211210/) |
| Florida | Agency for Healthcare Administration | Rejected | [MuckRock request](https://www.muckrock.com/foi/florida-34/aer-fl-agency-for-healthcare-admin-207528/) |
| Florida | Agency for Healthcare Administration | Rejected | [MuckRock request](https://www.muckrock.com/foi/florida-34/aer-fl-agency-for-healthcare-admin-210811/) |
| Georgia | Department of Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/georgia-230/aer-ga-dept-of-human-services-207529/) |
| Georgia | Department of Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/georgia-230/aer-ga-dept-of-human-services-210816/) |
| Idaho | Department of Health and Welfare | Completed | [MuckRock request](https://www.muckrock.com/foi/idaho-228/aer-id-dept-of-health-and-welfare-207534/) |
| Illinois | Department of Public Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/illinois-168/aer-il-dept-of-public-health-207535/) |
| Kansas | Department of Health & Environment | Rejected | [MuckRock request](https://www.muckrock.com/foi/kansas-111/aer-ks-dept-of-health-and-environment-208098/) |
| Kansas | Kansas Department for Aging and Disability Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/kansas-111/aer-ks-dept-of-aging-and-disability-services-208801/) |
| Kansas | Kansas Department for Aging and Disability Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/kansas-111/aer-ks-dept-of-aging-and-disability-services-redo-210806/) |
| Louisiana | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/louisiana-233/aer-la-department-of-health-208165/) |
| Louisiana | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/louisiana-233/aer-la-department-of-health-210809/) |
| Maine | Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/maine-13/aer-me-dept-of-health-and-human-services-208100/) |
| Maine | Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/maine-13/aer-me-dept-of-health-and-human-services-210812/) |
| Maryland | Department of Health and Mental Hygiene | Rejected | [MuckRock request](https://www.muckrock.com/foi/maryland-154/aer-md-department-of-health-and-mental-hygiene-208108/) |
| Maryland | Department of Health and Mental Hygiene | Rejected | [MuckRock request](https://www.muckrock.com/foi/maryland-154/aer-md-department-of-health-and-mental-hygiene-redo-210814/) |
| Massachusetts | Department of Public Health | Fix Required | [MuckRock request](https://www.muckrock.com/foi/massachusetts-1/aer-ma-department-of-public-health-208109/) |
| Michigan | Michigan Department of Health and Human Services | Completed | [MuckRock request](https://www.muckrock.com/foi/michigan-117/aer-mi-department-of-health-and-human-services-208166/) |
| Minnesota | Minnesota Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/minnesota-156/aer-mn-department-of-health-208110/) |
| Minnesota | Minnesota Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/minnesota-156/aer-mn-department-of-health-210808/) |
| Missouri | Department of Health and Senior Services | Completed | [MuckRock request](https://www.muckrock.com/foi/missouri-299/aer-mo-department-of-health-and-human-services-208167/) |
| Nebraska | Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/nebraska-300/aer-ne-department-of-health-and-human-services-208168/) |
| Nevada | Department of Health and Human Services | Consolidated | [MuckRock request](https://www.muckrock.com/foi/nevada-301/aer-nv-state-health-division-208113/) |
| Nevada | Nevada Health Authority | Completed | [MuckRock request](https://www.muckrock.com/foi/nevada-301/aer-nv-state-health-division-210801/) |
| New Hampshire | Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/new-hampshire-81/aer-nh-department-of-health-and-human-services-208169/) |
| New Hampshire | Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/new-hampshire-81/aer-nh-department-of-health-and-human-services-210810/) |
| New Jersey | Department of Health | Awaiting Response | [MuckRock request](https://www.muckrock.com/foi/new-jersey-229/aer-nj-department-of-health-and-senior-services-208115/) |
| New York | New York State Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/new-york-16/aer-ny-department-of-health-208123/) |
| North Dakota | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/north-dakota-232/aer-nh-department-of-health-208170/) |
| Ohio | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/ohio-116/aer-oh-department-of-health-208124/) |
| Oklahoma | Oklahoma Department of Health | Awaiting Acknowledgement | [MuckRock request](https://www.muckrock.com/foi/oklahoma-248/aer-ok-department-of-health-208171/) |
| Oregon | Oregon Health Authority | Rejected | [MuckRock request](https://www.muckrock.com/foi/oregon-158/aer-or-health-authority-208125/) |
| Oregon | Patient Safety Commission | Completed | [MuckRock request](https://www.muckrock.com/foi/oregon-158/aer-or-health-authority-209408/) |
| Oregon | Patient Safety Commission | Completed | [MuckRock request](https://www.muckrock.com/foi/oregon-158/aer-or-patient-safety-commission-211209/) |
| Pennsylvania | Pennsylvania Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/pennsylvania-126/aer-pa-patient-safety-authority-208126/) |
| Rhode Island | Department of Health | Fix Required | [MuckRock request](https://www.muckrock.com/foi/rhode-island-82/aer-ri-department-of-health-208127/) |
| Rhode Island | Department of Health | Awaiting Response | [MuckRock request](https://www.muckrock.com/foi/rhode-island-82/aer-ri-department-of-health-redo-212247/) |
| South Carolina | Department of Health and Environmental Control | Awaiting Acknowledgement | [MuckRock request](https://www.muckrock.com/foi/south-carolina-302/aer-sc-department-of-health-and-environmental-control-208128/) |
| South Dakota | Department of Health | Awaiting Acknowledgement | [MuckRock request](https://www.muckrock.com/foi/south-dakota-303/aer-south-dakota-department-of-health-208136/) |
| Tennessee | Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/tennessee-155/aer-tn-dept-of-health-208159/) |
| Texas | Texas Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/texas-109/aer-tx-department-of-health-and-human-services-208172/) |
| Texas | Texas Department of State Health Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/texas-109/aer-tx-department-of-state-health-services-208802/) |
| Texas | Texas Department of State Health Services | Completed | [MuckRock request](https://www.muckrock.com/foi/texas-109/aer-tx-department-of-state-health-services-210805/) |
| Utah | Utah Department of Health and Human Services | Rejected | [MuckRock request](https://www.muckrock.com/foi/utah-234/aer-ut-dept-of-health-208160/) |
| Vermont | Vermont Department Of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/vermont-80/aer-vt-dept-of-health-208161/) |
| Washington | Department of Health | Completed | [MuckRock request](https://www.muckrock.com/foi/washington-54/aer-wa-dept-of-health-208163/) |
| West Virginia | Department of Health and Human Resources | Rejected | [MuckRock request](https://www.muckrock.com/foi/west-virginia-304/aer-wv-department-of-health-and-human-resources-208175/) |
| West Virginia | West Virginia Department Of Health | No Responsive Documents | [MuckRock request](https://www.muckrock.com/foi/west-virginia-304/aer-wv-department-of-health-and-human-resources-208800/) |
| Wisconsin | Wisconsin Department of Health Services | No Responsive Documents | [MuckRock request](https://www.muckrock.com/foi/wisconsin-146/aer-wi-department-of-health-services-208176/) |
| Wyoming | Wyoming Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/wyoming-305/aer-wy-dept-of-health-208164/) |
| Wyoming | Wyoming Department of Health | Rejected | [MuckRock request](https://www.muckrock.com/foi/wyoming-305/aer-wy-dept-of-health-redo-210807/) |