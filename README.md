# Extreme-Whether-Event-Prediction

## Project Overview

This project aims to predict extreme weather events with a focus on wildfires. Wildfires are significant natural disasters that cause extensive damage to the environment, property, and human life. Accurate prediction of wildfires can help in planning and mitigating these risks.

## Dataset Sources

We are using publicly available wildfire datasets. Below are two reliable sources where the same dataset can be accessed:

1. [National Interagency Fire Occurrence - Sixth Edition (1992-2020) on Data.gov](https://catalog.data.gov/dataset/national-interagency-fire-occurrence-sixth-edition-1992-2020-feature-layer)
2. [Kaggle - US Wildfire Records (6th Edition)](https://www.kaggle.com/datasets/behroozsohrabi/us-wildfire-records-6th-edition)

## Setup Instructions

1. Download the dataset from one of the sources above.
2. Save the dataset as `data.csv` in the project directory.

## Libraries Needed

- `pandas` for data manipulation and analysis

## Steps and Progress

### Exploratory Data Analysis (EDA)

We start with EDA to understand the structure and characteristics of the dataset.

#### Data Loading and Overview

- Load the dataset into a Pandas DataFrame.
- Display the first few rows.
- Print a summary of the dataset.

#### Data Cleaning and Processing

- Handle missing values.
- Remove duplicate rows.
- Ensure data consistency by converting columns to appropriate data types.
  - Convert `DISCOVERY_DATE` and `CONT_DATE` to datetime format.

## Column Descriptions

- **FOD_ID**: Unique numeric record identifier.
- **FPA_ID**: Unique identifier that contains information necessary to track back to the original record in the source dataset.
- **SOURCE_SYSTEM_TYPE**: Type of source database or system that the record was drawn from (FED = federal, NONFED = nonfederal, or INTERAGCY = interagency).
- **SOURCE_SYSTEM**: Name or other identifier for the source database or system that the record was drawn from.
- **NWCG_REPORTING_AGENCY**: Active National Wildlife Coordinating Group (NWCG) Unit Identifier for the agency preparing the fire report (BIA = Bureau of Indian Affairs, BLM = Bureau of Land Management, BOR = Bureau of Reclamation, DOD = Department of Defense, DOE = Department of Energy, FS = Forest Service, FWS = Fish and Wildlife Service, IA = Interagency Organization, NPS = National Park Service, ST/C&L = State, County, or Local Organization, and TRIBE = Tribal Organization).
- **NWCG_REPORTING_UNIT_ID**: Active NWCG Unit Identifier for the unit preparing the fire report.
- **NWCG_REPORTING_UNIT_NAME**: Active NWCG Unit Name for the unit preparing the fire report.
- **SOURCE_REPORTING_UNIT**: Code for the agency unit preparing the fire report, based on code/name in the source dataset.
- **SOURCE_REPORTING_UNIT_NAME**: Name of the reporting agency unit preparing the fire report, based on code/name in the source dataset.
- **LOCAL_FIRE_REPORT_ID**: Number or code that uniquely identifies an incident report for a particular reporting unit and a particular calendar year.
- **LOCAL_INCIDENT_ID**: Number or code that uniquely identifies an incident for a particular local fire management organization within a particular calendar year.
- **FIRE_CODE**: Code used within the interagency wildland fire community to track and compile cost information for emergency fire suppression (https://www.firecode.gov/).
- **FIRE_NAME**: Name of the incident, from the fire report (primary) or ICS-209 report (secondary).
- **ICS_209_PLUS_INCIDENT_JOIN_ID**: Primary identifier needed to join into operational situation reporting data for the incident in the ICS-209-PLUS dataset.
- **ICS_209_PLUS_COMPLEX_JOIN_ID**: If part of a complex, secondary identifier potentially needed to join to operational situation reporting data for the incident in the ICS-209-PLUS dataset.
- **MTBS_ID**: Incident identifier, from the MTBS perimeter dataset.
- **MTBS_FIRE_NAME**: Name of the incident, from the MTBS perimeter dataset.
- **COMPLEX_NAME**: Name of the complex under which the fire was ultimately managed, when discernible.
- **FIRE_YEAR**: Calendar year in which the fire was discovered or confirmed to exist.
- **DISCOVERY_DATE**: Date on which the fire was discovered or confirmed to exist.
- **DISCOVERY_DOY**: Day of year on which the fire was discovered or confirmed to exist.
- **DISCOVERY_TIME**: Time of day that the fire was discovered or confirmed to exist.
- **NWCG_CAUSE_CLASSIFICATION**: Broad classification of the reason the fire occurred (Human, Natural, Missing data/not specified/undetermined).
- **NWCG_GENERAL_CAUSE**: Event or circumstance that started a fire or set the stage for its occurrence (Arson/incendiarism, Debris and open burning, Equipment and vehicle use, Firearms and explosives use, Fireworks, Misuse of fire by a minor, Natural, Power generation/transmission/distribution, Railroad operations and maintenance, Recreation and ceremony, Smoking, Other causes, Missing data/not specified/undetermined).
- **NWCG_CAUSE_AGE_CATEGORY**: If cause attributed to children (ages 0-12) or adolescents (13-17), the value for this data element is set to Minor; otherwise null.
- **CONT_DATE**: Date on which the fire was declared contained or otherwise controlled (mm/dd/yyyy where mm=month, dd=day, and yyyy=year).
- **CONT_DOY**: Day of year on which the fire was declared contained or otherwise controlled.
- **CONT_TIME**: Time of day that the fire was declared contained or otherwise controlled (hhmm where hh=hour, mm=minutes).
- **FIRE_SIZE**: The estimate of acres within the final perimeter of the fire.
- **FIRE_SIZE_CLASS**: Code for fire size based on the number of acres within the final fire perimeter (A=greater than 0 but less than or equal to 0.25 acres, B=0.26-9.9 acres, C=10.0-99.9 acres, D=100-299 acres, E=300 to 999 acres, F=1000 to 4999 acres, and G=5000+ acres).
- **LATITUDE**: Latitude (NAD83) for point location of the fire (decimal degrees).
- **LONGITUDE**: Longitude (NAD83) for point location of the fire (decimal degrees).
- **OWNER_DESCR**: Name of primary owner or entity responsible for managing the land at the point of origin of the fire at the time of the incident.
- **STATE**: Two-letter alphabetic code for the state in which the fire burned (or originated), based on the nominal designation in the fire report (not from a spatial overlay).
- **COUNTY**: County, or equivalent, in which the fire burned (or originated), based on nominal designation in the fire report (not from a spatial overlay).
- **FIPS_CODE**: Five-digit code from the Federal Information Process Standards (FIPS) publication 6-4 for representation of counties and equivalent entities, based on the nominal designation in the fire report (not from a spatial overlay).
- **FIPS_NAME**: County name from the FIPS publication 6-4 for representation of counties and equivalent entities, based on the nominal designation in the fire report (not from a spatial overlay).
