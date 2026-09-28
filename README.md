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


## Mapping state statutes and MuckRock requests
- You can find the requests we've filed to states [on MuckRock](https://www.muckrock.com/project/dlp-patient-safety-1250/) where each adverse events requests has "AER" for adverse events reporting in the title of the request.
- We then organized our requests into categories of whether we recieved the data and whether a [2025 OIG report found the state had a mandated reporting system](https://oig.hhs.gov/documents/evaluation/10842/OEI-06-18-00402.pdf).
- In `data/manual/map.csv` you can find a csv with each state's reporting status according to the OIG report and labeled based on the status of MuckRock requests. Each request is given on of the following categories:
  - `not_requested`: we haven't requested data from this state yet
  - `not_received`: we haven't recieved data from the state because the request was rejected, there were no responsive documents or the request is ongoing
  - `received_incorrect_form`: we recieved data, but it was not in the form we requested as "all adverse events" but aggregrated or seggrated to a smaller portion of data 
  - `received`: we recieved facility-level data for individual events 
    












