# Forensic Foot Search Simulations — Detection Data

## Overview

This dataset contains detection records from simulated forensic foot searches conducted in a deciduous forest at the University of Toronto Mississauga on three dates: September 27, 2023; October 2, 2024; and May 15, 2025. Volunteer searchers walked 50-metre transects through a study area seeded with objects — including backpacks, shoes, eyeglasses, and fabric scraps — placed at known locations. For each pass, records were made of which objects were detected and where. The study aimed to estimate sweep widths for use in planning real-world forensic foot searches, contributing empirical data to support evidence-based search management.

## Files in This Dataset

| File | Description |
|------|-------------|
| `master/master_forensic_survey_grid_1_2.csv` | Master (uncleaned) detection records for survey Grids 1 and 2, containing the original raw observations as collected in the field. |
| `master/master_forensic_survey_grid_3_4.csv` | Master (uncleaned) detection records for survey Grids 3 and 4, containing the original raw observations as collected in the field. |
| `cleaned/grid_1_2_cleaned_adjusted.csv` | Cleaned detection records for Grids 1 and 2 with positional adjustments applied to correct known recording offsets. |
| `cleaned/grid_1_2_cleaned_no_adjustments.csv` | Cleaned detection records for Grids 1 and 2 without positional adjustments, for comparison with the adjusted version. |
| `cleaned/grid_3_4_cleaned_no_adjustments.csv` | Cleaned detection records for Grids 3 and 4 without positional adjustments. |
| `documentation/Explanation_of_columns.pdf` | Reference document describing all column names, their meanings, and coding conventions used across the dataset files. |

## Column Definitions

| Column Name | Description |
|-------------|-------------|
| `LDist` | Lateral distance (in metres) from the searcher's transect line to the object at the moment of detection. |
| `Dist` | Straight-line distance (in metres) from the searcher to the object at the moment of detection. |
| `LorR` | Side of the transect on which the object was located at detection: `Left` or `Right`. |
| `Type` | Category of the seeded object detected (e.g., Backpack, Shoe, Eyeglasses, Fabric). |
| `End time` | Time at which the searcher completed their transect pass (HH:MM format). |
| `Start time` | Time at which the searcher began their transect pass (HH:MM format). |
| `Total time` | Total elapsed time (in minutes) for the searcher to complete the transect pass. |
| `N` | Number of objects detected by the searcher during the transect pass. |
| `Problem?` | Flag indicating whether any data quality issue or anomaly was noted for that record (e.g., Yes/No or descriptive note). |
| `Date` | Date on which the search trial was conducted. |
| `Notes` | Free-text field for any additional observations or comments recorded by the researcher. |
| `Sort Order` | Numeric field used to order records for processing or display purposes. |

## How to Cite

Citation details will be added upon Zenodo deposit. DOI: [TBD]

## Ethics and Funding

This study was approved under Protocol 28965 by the University of Toronto Office of Research Ethics. Funding was provided by the Social Sciences and Humanities Research Council of Canada (SSHRC).
