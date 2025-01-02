# About Dataset

This GitHub repository contains compiled data from published waste characterization studies with intent for training waste composition prediction models. The data is first used in a study published in the journal *Waste Management* DOI: 10.1016/j.wasman.2024.12.002

## Data Collection Methodology

Each data point comes from a %adjust to match more specific wording% report called a "Waste Characterization Study." Some reports provide multiple data points %be more specific about what one data point is, a composition for a specific area for a specific time%, such as individual data for each county within a state. The project team manually extracted this data from the publicly available report PDFs. Since different reports often use unique sets of material categories, the team translated the data into a standardized characterization. This process is detailed in the aforementioned paper.

### Data Description

The original reports (all in PDF format) are contained in the "Characterization Studies Used" folder. These copies are included to ensure accessibility, as their locations on government repositories tends to change.

The resulting data table has 58 columns: 3 description columns, 43 detailed waste material category columns, and 12 aggregated waste category columns. Each row (i.e., waste characterization datapoint) contains the following:

1. Note - The area covered by the data, often matching the verbiage of the original report.
2. Year - The reported year the data was gathered (note: this may be earlier than the year that the data was published).
3. FIPS - Comma separated list of Federal Information Processing System (i.e., unique identifiers of geographic areas) codes for the counties that are represented by the data.
4. Detailed Material Categories (Columns 4-46) - Percentage of the waste stream that is made up by the material category represented by each column (note: materials categories that did not match the common categorization were left incomplete). 
5. Aggregated Material Categories (Columns 47-58) - Combination of detailed material categories into fewer general material categories.

# How to Cite This Work

Users of this dataset are politely requested to cite both this data repository as well as the *Waste Management* paper in which the collection and translation methodologies are described.

## Dataset Citation

Grassel, J. T., Hasan, K. W., Bingham, D. R., Rengarajan, N., Escobedo, A. R., Rushforth, R. R., Buch, R. (2024). Translated and compiled waste characterization study data. URL: https://github.com/jtgrasse/Predicting_MSW

```
@misc{waste_characterization_data_2024,
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
