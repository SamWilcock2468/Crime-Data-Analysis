# Crime Data Analysis Pipeline

## Overview
This pipeline creates a data warehouse for crime data in England within the years 2023 - 2026.
It currently supports the analysis of 4 police areas - merseyside, west midlands, west yorkshire, and south yorkshire.
It aggregates supplementary data of: population, deprivation, and crime severity.
It also creates a location lookup table, dated 2025 for all areas within England.

## Repositry Structure
CrimeData/
├── README.md
├── Data/
    ├── Output/
    ├── Processed/
        ├── crime-severity-raw/
    ├── Raw/
        ├── crime-data/
        ├── crime-severity
        ├── deprivation/
        ├── lookup/
        ├── population/
├── Scripts/
    ├── 01_SamplingAndCleaning
    ├── 02_SupportiveTables
    ├── 03_AggregatingCrimeData
├── Documents/
    ├── Data-Dictionary.xlsx
    ├── Statement of Work.docx
    ├── Workflow Diagram.pdf


## Installation and Quickstart Guide
1) Download the repository.
2) Download the raw data and processed data (ask personally for downloads, instead of overloading github).
3) Run the scripts held in the 'Scripts' folder in the order presented. 01, 02, then 03.
       If you run them in the wrong order, the processed warehouse may not be completed and won't be imported correctly.
4) A final database will be created in the Data\Output folder holding the outputted data, which is readily able to be analysed in visualisation software.


## Raw Data
1) LSOA -> LAD conversion table: __https://ckan.publishing.service.gov.uk/dataset/local-authority-district-to-community-safety-partnership-to-pfa-april-2025-lookup-in-ew/resource/e8cc60d8-f3bb-4a29-ad58-821247d88d95__

2) LAD -> PFA conversion table: __https://ckan.publishing.service.gov.uk/dataset/lsoa-2021-to-electoral-ward-2024-to-lad-2024-best-fit-lookup-in-ew__

3) Population: __https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/lowersuperoutputareamidyearpopulationestimates__

4) Deprivation: __https://www.gov.uk/csv-preview/691ded56d140bbbaa59a2a7d/File_7_IoD2025_All_Ranks_Scores_Deciles_Population_Denominators.csv__

5) Crime severity weighting: __https://www.ons.gov.uk/peoplepopulationandcommunity/crimeandjustice/datasets/crimeseverityscoredatatool__

6) Crime category data: __https://data.police.uk/static/files/police-uk-category-mappings.csv__

7) Crime Data: __https://data.police.uk/data/__

