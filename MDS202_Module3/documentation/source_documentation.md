# Module 3 – Data Source Documentation

## 1. Dataset Information

| Field | Description |
|---|---|
| Dataset Title | Building Energy Benchmarking Data, 2015–Present |
| Selected Option | Option A – Continue Module 2 Dataset |
| Data Provider | City of Seattle |
| Dataset Page | https://data.seattle.gov/Built-Environment/Building-Energy-Benchmarking-Data-2015-Present/teqw-tu6e |
| Dataset ID | teqw-tu6e |
| Data Format | CSV |
| API Format | JSON |
| Geographic Coverage | Seattle, Washington, USA |
| Access Date | [Enter the date you accessed the dataset] |

## 2. Dataset Selection

This project continues the Seattle Building Energy Benchmarking dataset used in Module 2. Option A was selected to maintain continuity between the previous activities and Module 3.

The existing CSV file will serve as the reference dataset for validating the data acquired through the API.

## 3. Working Question

How does building type relate to Site Energy Use Intensity (Site EUI) among benchmarked buildings in Seattle?

## 4. Data Source and API

**Official Dataset Page:**

https://data.seattle.gov/Built-Environment/Building-Energy-Benchmarking-Data-2015-Present/teqw-tu6e

**Socrata API Endpoint:**

https://data.seattle.gov/resource/teqw-tu6e.json

**API Dataset Identifier:** teqw-tu6e

The API will be used to programmatically retrieve the dataset using Python.

## 5. Data Storage Plan

| Data Stage | Storage Location |
|---|---|
| Original CSV | data/raw/seattle_building_energy_original.csv |
| Raw API Response | data/raw/ |
| Parsed API Data | data/interim/ |
| Cleaned and Analysis-Ready Data | data/processed/ |

Raw data will be preserved unchanged. Processing and cleaning will be performed on separate copies.

## 6. Validation Plan

The API-acquired dataset will be compared with the existing CSV to examine:

- Record counts
- Column names and structure
- Data types
- Missing values
- Differences in records and values

Any discrepancies will be documented and investigated rather than silently ignored.

## 7. Notes

The detailed research question, unit of analysis, population, sample, and statistical parameter will be defined further in Activity 1, Task 1.

# Step 2 – API Preparation

## 1. API Overview

The Seattle Building Energy Benchmarking dataset is available through the City of Seattle Open Data portal, which uses the Socrata Open Data API (SODA).

**Dataset:** Building Energy Benchmarking Data, 2015–Present  
**Dataset ID:** teqw-tu6e  
**Data Provider:** City of Seattle  
**Official Dataset Page:** https://data.seattle.gov/Built-Environment/Building-Energy-Benchmarking-Data-2015-Present/teqw-tu6e

## 2. API Endpoint

The SODA3 query endpoint selected for this project is:

https://data.seattle.gov/api/v3/views/teqw-tu6e/query.json

The dataset also supports the SODA2 endpoint:

https://data.seattle.gov/resource/teqw-tu6e.json

The SODA3 endpoint will be used for the programmatic data acquisition workflow.

## 3. API Request Configuration

| Parameter | Configuration |
|---|---|
| HTTP Method | POST |
| Request Format | JSON |
| Response Format | JSON |
| Authentication | Application Token |
| Authentication Header | X-App-Token |
| Planned Page Size | 1,000 records |
| Pagination | Page number and page size |

The application token will be stored in an environment variable and accessed through Python. The actual token will not be included in notebooks, documentation, or public repositories.

## 4. API Acquisition Procedure

The API acquisition will follow these steps:

1. Send a small test request to verify API connectivity.
2. Inspect the HTTP response status and JSON structure.
3. Determine the correct pagination configuration.
4. Retrieve the dataset through successive API requests.
5. Preserve the raw API response.
6. Parse the JSON records into a Pandas DataFrame.
7. Save the parsed API dataset separately from the original CSV.
8. Compare the acquired API dataset with the original CSV.

## 5. Data Storage Plan

| Data Stage | File Location |
|---|---|
| Original CSV | data/raw/seattle_building_energy_original.csv |
| Raw API Response | data/raw/seattle_api_raw.json |
| Parsed API Dataset | data/interim/seattle_api_parsed.csv |
| Cleaned Dataset | data/processed/seattle_cleaned.csv |

The original CSV will remain unchanged and serve as the reference dataset for validation.

## 6. API Validation Plan

The API-acquired dataset will be evaluated using the following checks:

- Total number of records retrieved
- Number of columns and column names
- Data types
- Missing values
- Duplicate records
- Reporting-year distribution
- Record-level differences between the CSV and API datasets

Any discrepancies will be investigated and documented before the dataset is used for further analysis.

## 7. Reproducibility and Security

The API acquisition process will be implemented in Python using the Requests and Pandas libraries.

The application token will be stored in a local environment file and accessed through an environment variable.

Sensitive credentials will not be committed to GitHub or included in publicly shared notebooks.

The acquisition workflow will be documented so that the process can be reproduced and verified.

## 8. Expected Output

The expected outputs of the API acquisition process are:

- Raw API response in JSON format
- Parsed API dataset in CSV format
- API acquisition notebook
- API validation results
- Documentation of any discrepancies between the API and original CSV

### API Acquisition Results

The full Seattle Building Energy Benchmarking dataset was successfully retrieved through the SODA3 API using Python requests and pagination.

| Acquisition Detail | Result |
|---|---|
| HTTP status | 200 (successful request) |
| API query | SELECT * |
| Page size | 1,000 records |
| Total records acquired | 38,309 |
| API dataset columns | 50 |
| Dataset dimensions | 38,309 × 50 |
| JSON output | `data/raw/seattle_building_energy_api.json` |
| CSV output | `data/interim/seattle_building_energy_api.csv` |

The API dataset and original CSV have matching record counts. Further validation is required to determine whether their records and values are equivalent.