# About Dataset

This GitHub repository contains compiled data from published waste characterization studies with intent for training waste composition prediction models. The data is first used in a study published in the journal *Waste Management* DOI: 10.1016/j.wasman.2024.12.002. For reproducibility, this repository includes the predictor variables used to train and test the model described in the aforementioned paper.

# Municipal Solid Waste Composition Data

## Collection Methodology

The data available is contained in reports that we refer to as *waste characterization studies*; these reports are often titled similarly. The data is pulled from these reports, where each data point is an estimated percentage breakdown of the waste stream into various material categories for a particular geographic area and year. Some reports provide multiple data points, such as data for each county within a state. The project team manually extracted this data from the publicly available report PDFs. Since different reports often use unique sets of material categories, the team translated the data into a standardized characterization. This process is detailed in the aforementioned paper.

### Data Description

The original reports (all in PDF format) are contained in the "Characterization Studies Used" folder. These copies are included to ensure accessibility, as their locations on government repositories tends to change.

The resulting data table has 58 columns: 3 description columns, 43 detailed waste material category columns, and 12 aggregated waste category columns. Each row (i.e., waste characterization datapoint) contains the following:

1. Note - The area covered by the data, often matching the verbiage of the original report.
2. Year - The reported year the data was gathered (note: this may be earlier than the year that the data was published).
3. FIPS - Comma separated list of Federal Information Processing System (i.e., unique identifiers of geographic areas) codes for the counties that are represented by the data.
4. Detailed Material Categories (Columns 4-46) - Percentage of the waste stream that is made up by the material category represented by each column (note: materials categories that did not match the common categorization were left incomplete). 
5. Aggregated Material Categories (Columns 47-58) - Combination of detailed material categories into fewer general material categories.

The following is a sample from the data:

| Notes                     | YEAR | FIPS  | Newspaper | Corrugated Cardboard | Office | Magazine/Glossy | Paperboard | Mixed Paper | Other Paper | ... |
| -------------------------- | ---- | ----- | --------- | -------------------- | ------ | --------------- | ---------- | ----------- | ----------- | --- |
| Montgomery County, Maryland | 2017 | 24031 | 0.014     | 0.028                | 0.01   | 0.004           | 0.045      | 0.039       | 0.085       | ... |

This data point indicates that Montgomery County in Maryland (with 24031 as the associated FIPS code) reported in 2017 that their MSW consisted of 1.4% Newspaper, 2.8% Cardboard, 1% Office paper, etc.

# How to Cite This Work

Users of this dataset are politely requested to cite both this data repository as well as the *Waste Management* paper in which the collection and translation methodologies are described.

## Dataset Citation

Grassel, J. T., Hasan, K. W., Bingham, D. R., Rengarajan, N., Escobedo, A. R., Rushforth, R. R., Buch, R. (2024). Translated and compiled waste characterization study data. URL: https://github.com/jtgrasse/Predicting_MSW

```
@misc{grassel2024translated,
    author = {Grassel, Joshua T and Hasan, Kazi W and Bingham, Darren R and Rengarajan, Nivedita and Escobedo, Adolfo R and Rushforth, Richard R and Buch, Rajesh},
    year={2024},
    title = {Translated and compiled waste characterization study data},
    howpublished= {\url{https://github.com/jtgrasse/Predicting\_MSW}
} 
```

## *Waste Management* Paper Citation

Grassel, J. T., Escobedo, A. R., & Buch, R. (2025). Predicting the composition of solid waste at the county scale. *Waste Management*, 193, 293-306.

```
@article{grassel2025predicting,
  title={Predicting the composition of solid waste at the county scale},
  author={Grassel, Joshua T and Escobedo, Adolfo R and Buch, Rajesh},
  journal={Waste Management},
  volume={193},
  pages={293--306},
  year={2025},
  publisher={Elsevier}
}
```

# Independent Variable Data

The data used to train and test the composition prediction model is included in this repository as a ZIP folder. This folder contains two files: "Compiled_Predictors.csv" includes the all the independent variable data, and "Prediction_Data_Descriptors.csv" provides more detailed information on what the column names represet. This data was compiled from three sources: Bureau of Economic Analysis (BEA),  U.S. Census Bureau, and National Cancer Institute (NCI).

1. YEAR and FIPS - Identifiers for when and where the data applies.
2. BEA Data (Columns 3-86) - This covers a variety of economic data collected by the BEA, ranging from GDP to personal income.
3. U.S. Census Bureau Data (Column 87) - The "Area" represents the land and water area defined by the FIPS code. Note: this measure was taken in 2000 and was applied to all years.
4. NCI Data (Columns 88-106) - This estimated data breaks down the population into 19 age groups for each year and each FIPS.

Note: this data was not used for prediction as it is shared on this repository. The composition prediction model described in the paper used transformations of this data. The data was made scale invariant (such as population/area to get population density and GDP/population to get per-capita GDP), and the natural logorithm was taken to better linearly correlate with the isometric log ratio transformed compositions. Details can be found in the paper.

## Data Sources
The BEA data was retrieved in 2024 from the interactive tables hosted on the BEA website: https://www.bea.gov/itable/.
The U.S. Census Bureau data was retrieved in 2024 from the TIGERweb application: https://tigerweb.geo.census.gov/tigerwebmain/TIGERweb_main.html.
The NCI data was retrieved from the SEER county population data posted in 2022: https://seer.cancer.gov/popdata/
