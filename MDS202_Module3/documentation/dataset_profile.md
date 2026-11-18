# Dataset Profile

## 1. Dataset Overview

- Dataset: Seattle Building Energy Benchmarking
- Rows: 38,309
- Columns: 46
- Exact duplicate records: 0
- Reporting period: 2015–2025

## 2. Column Names

- OSEBuildingID
- DataYear
- BuildingName
- BuildingType
- TaxParcelIdentificationNumber
- Address
- City
- State
- ZipCode
- Latitude
- Longitude
- Neighborhood
- CouncilDistrictCode
- YearBuilt
- NumberofFloors
- NumberofBuildings
- PropertyGFATotal
- PropertyGFABuildings
- PropertyGFAParking
- SelfReportGFATotal
- SelfReportGFABuildings
- SelfReportParking
- ENERGYSTARScore
- SiteEUIWN(kBtu/sf)
- SiteEUI(kBtu/sf)
- SiteEnergyUse(kBtu)
- SiteEnergyUseWN(kBtu)
- SourceEUIWN(kBtu/sf)
- SourceEUI(kBtu/sf)
- EPAPropertyType
- LargestPropertyUseType
- LargestPropertyUseTypeGFA
- SecondLargestPropertyUseType
- SecondLargestPropertyUseTypeGFA
- ThirdLargestPropertyUseType
- ThirdLargestPropertyUseTypeGFA
- Electricity(kWh)
- SteamUse(kBtu)
- NaturalGas(therms)
- ComplianceStatus
- ComplianceIssue
- Electricity(kBtu)
- NaturalGas(kBtu)
- TotalGHGEmissions
- GHGEmissionsIntensity
- Demolished

## 3. Data Types

| Column | Data Type |
|---|---|
| OSEBuildingID | int64 |
| DataYear | int64 |
| BuildingName | str |
| BuildingType | str |
| TaxParcelIdentificationNumber | str |
| Address | str |
| City | str |
| State | str |
| ZipCode | int64 |
| Latitude | float64 |
| Longitude | float64 |
| Neighborhood | str |
| CouncilDistrictCode | int64 |
| YearBuilt | int64 |
| NumberofFloors | int64 |
| NumberofBuildings | int64 |
| PropertyGFATotal | str |
| PropertyGFABuildings | str |
| PropertyGFAParking | str |
| SelfReportGFATotal | str |
| SelfReportGFABuildings | str |
| SelfReportParking | str |
| ENERGYSTARScore | float64 |
| SiteEUIWN(kBtu/sf) | str |
| SiteEUI(kBtu/sf) | str |
| SiteEnergyUse(kBtu) | str |
| SiteEnergyUseWN(kBtu) | str |
| SourceEUIWN(kBtu/sf) | str |
| SourceEUI(kBtu/sf) | str |
| EPAPropertyType | str |
| LargestPropertyUseType | str |
| LargestPropertyUseTypeGFA | str |
| SecondLargestPropertyUseType | str |
| SecondLargestPropertyUseTypeGFA | str |
| ThirdLargestPropertyUseType | str |
| ThirdLargestPropertyUseTypeGFA | str |
| Electricity(kWh) | str |
| SteamUse(kBtu) | str |
| NaturalGas(therms) | str |
| ComplianceStatus | str |
| ComplianceIssue | str |
| Electricity(kBtu) | str |
| NaturalGas(kBtu) | str |
| TotalGHGEmissions | str |
| GHGEmissionsIntensity | str |
| Demolished | bool |

## 4. Missing Values

| Column | Missing Values |
|---|---:|
| ENERGYSTARScore | 10,417 |
| SiteEUIWN(kBtu/sf) | 1,961 |
| SiteEUI(kBtu/sf) | 1,562 |
| SiteEnergyUse(kBtu) | 1,555 |
| SiteEnergyUseWN(kBtu) | 1,953 |
| SourceEUIWN(kBtu/sf) | 1,961 |
| SourceEUI(kBtu/sf) | 1,562 |
| EPAPropertyType | 21 |
| LargestPropertyUseType | 21 |
| LargestPropertyUseTypeGFA | 21 |
| SecondLargestPropertyUseType | 15,937 |
| SecondLargestPropertyUseTypeGFA | 17,818 |
| ThirdLargestPropertyUseType | 29,200 |
| ThirdLargestPropertyUseTypeGFA | 30,256 |
| Electricity(kWh) | 1,100 |
| SteamUse(kBtu) | 37,016 |
| NaturalGas(therms) | 14,829 |
| ComplianceIssue | 481 |
| Electricity(kBtu) | 1,100 |
| NaturalGas(kBtu) | 14,822 |
| TotalGHGEmissions | 1,240 |
| GHGEmissionsIntensity | 1,834 |

## 5. Reporting Years

| Year | Records |
|---|---:|
| 2015 | 3,175 |
| 2016 | 3,253 |
| 2017 | 3,310 |
| 2018 | 3,381 |
| 2019 | 3,456 |
| 2020 | 3,530 |
| 2021 | 3,578 |
| 2022 | 3,617 |
| 2023 | 3,687 |
| 2024 | 3,712 |
| 2025 | 3,610 |

## 6. Initial Observations

- The dataset contains 38,309 records and 46 columns.
- There are 0 exact duplicate rows.
- Several variables contain missing values.
- Some numerical variables may require type conversion during cleaning.
- Data quality issues will be investigated before statistical analysis.
