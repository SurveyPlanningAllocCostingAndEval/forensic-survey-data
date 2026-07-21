# Forensic Foot Search Simulations — Detection Data

## Overview

This dataset contains detection records from simulated forensic foot searches conducted in a deciduous forest at the University of Toronto Mississauga on three dates: September 27, 2023; October 2, 2024; and May 15, 2025. Volunteer searchers walked 50-metre transects through a study area seeded with objects — including backpacks, shoes, eyeglasses, and fabric scraps — placed at known locations. For each pass, records were made of which objects were detected and where. The study aimed to estimate sweep widths for use in planning real-world forensic foot searches, contributing empirical data to support evidence-based search management. This dataset accompanies the paper "Estimation of Sweep Widths as a Tool in More Effective Planning of Forensic Foot Searches."

## Files in This Dataset

### MasterFiles/

File | Description
---|---
`MasterFiles/master_forensic_survey_grid_1_2.csv` | True locations of the 30 seeded targets for Grid 1/2 (lateral distance, range, side, and type). Used as the reference against which reported detections are checked.
`MasterFiles/master_forensic_survey_grid_3_4.csv` | True locations of the 30 seeded targets for Grid 3/4.

### DataFiles/Excel files with all data/

File | Description
---|---
`DataFiles/Excel files with all data/All Grid 1_2.xlsx` | Full detection dataset for Grid 1/2, including every recorded field (distances, side, target type, start/end/total time, detection count, date, notes, and sort order).
`DataFiles/Excel files with all data/All Grid 3_4.xlsx` | Full detection dataset for Grid 3/4, same fields as above.
`DataFiles/Excel files with all data/Explanation of columns.pdf` | Reference document describing all column names, their meanings, and coding conventions used across the dataset files.

### DataFiles/CSV files ready for analysis/

These files are reduced to the four fields (`LDist`, `Dist`, `LorR`, `Type`) used as direct input to the Sweep Width Estimator.

File | Description
---|---
`All Grid 1_2 cleaned.csv` | Cleaned detection records for Grid 1/2.
`All Grid 3_4 cleaned.csv` | Cleaned detection records for Grid 3/4.

**Divided by target type/** — subsets used to compare detectability across target types (bags, cloth, eyeglasses, shoes):

File | Description
---|---
`Bags Grid 1_2.csv`, `Bags Grid 3_4.csv` | Detections of bags only.
`Cloth Grid 1_2.csv`, `Cloth Grid 3_4.csv` | Detections of fabric/clothing scraps only.
`Eyeglasses Grid 1_2.csv`, `Eyeglasses Grid 3_4.csv` | Detections of eyeglasses only.
`Shoes Grid 1_2.csv`, `Shoes Grid 3_4.csv` | Detections of shoes only.
`All but bags Grid 1_2.csv`, `All but bags Grid 3_4.csv` | Detections of all target types except bags.

**Divided by time/** — subsets of Grid 1/2 detections grouped by total search-pass duration, used to assess the effect of search time on detection:

File | Description
---|---
`All Grid 1_2 2-6 minutes.csv` | Passes lasting 2–6 minutes.
`All Grid 1_2 7 to 8 minutes.csv` | Passes lasting 7–8 minutes.
`All Grid 1_2 9-10 minutes.csv` | Passes lasting 9–10 minutes.
`All Grid 1_2 11 plus minutes.csv` | Passes lasting 11 minutes or more.

## Column Definitions

Column Name | Description
---|---
`LDist` | Lateral distance (in metres) from the searcher's transect line to the object at the moment of detection.
`Dist` | Straight-line distance (in metres) from the searcher to the object at the moment of detection.
`LorR` | Side of the transect on which the object was located at detection: `Left` or `Right`.
`Type` | Category of the seeded object detected (e.g., Bag, Shoe, Eyeglasses, Cloth).
`DistanceError` | Difference between the reported detection location and the true seeded location, where applicable.
`Start` | Time at which the searcher began their transect pass.
`End` | Time at which the searcher completed their transect pass.
`Time` | Total elapsed time for the searcher to complete the transect pass.
`N` | Number of objects detected by the searcher during the transect pass.
`Problem` | Flag indicating whether any data quality issue or anomaly was noted for that record.
`Date` | Date on which the search trial was conducted.
`Notes` | Free-text field for any additional observations or comments recorded by the researcher.
`Sort order` | Numeric field used to order records for processing or display purposes.

Note: the CSV files in `DataFiles/CSV files ready for analysis/` retain only `LDist`, `Dist`, `LorR`, and `Type`; the full column set above is preserved in the `.xlsx` files under `DataFiles/Excel files with all data/`.

## Ethics and Funding

This study was approved under Protocol 28965 by the University of Toronto Office of Research Ethics. Funding was provided by the Social Sciences and Humanities Research Council of Canada (SSHRC).
