# About Dataset

This GitHub repository contains compiled data from published waste characterization studies with intent for training waste composition prediction models. The data is first used in a study published in the journal *Waste Management* DOI: 10.1016/j.wasman.2024.12.002

## Data Collection Methodology

Each data point comes from a report called a "Waste Characterization Study." Some reports provide multiple data points, such as individual data for each county within a state. The data has been manually extracted from each report PDF by the project team. The project team manually extracted this data from the report PDFs. Since different reports often use unique sets of material categories, the team translated the data into a standardized characterization. This process is detailed in the aforementioned paper.

### Data Description

The original reports (all in PDF format) are contained in the "Characterization Studies Used" folder. These copies are included to ensure accessibility, as their locations on government repositories may change.

The resulting data table has 3 description columns, 43 detailed waste material category columns, and 12 aggregated waste category columns. Each datapoint contains the following:
1. Note - This describes the area covered by the data, often matching the verbiage of the original report.
2. Year - The year that the data was gathered (note: this may be earlier than the year that the data was published).
3. FIPS - Comma separated list of the FIPS codes of the counties that are represented by the data.
4. Detailed Material Categories (Columns 4-46) - Each column includes the percentage of the waste stream that is made up by the specified material category.
5. Aggregated Material Categories (Columns 47-58) - Each column represents a more agregated material category. This breakdown avoids missing values for reports that provide less detailed data.

# Dataset Citation

If you use this dataset, please cite both this data repository as well as the *Waste Management* paper in which the collection and translation methodology is described.

Grassel, J. T., Hasan, K. W., Bingham, D. R., Rengarajan, N., Escobedo, A. R., Rushforth, R. R., Buch, R. (2024). Translated and compiled waste characterization study data. URL: https://github.com/jtgrasse/Predicting_MSW

```
@misc{waste_characterization_data_2024,
    author = {Grassel, Joshua T and Hasan, Kazi W and Bingham, Darren R and Rengarajan, Nivedita and Escobedo, Adolfo R and Rushforth, Richard R and Buch, Rajesh},
    year={2024},
    title = {Translated and compiled waste characterization study data},
    howpublished= {\url{https://github.com/jtgrasse/Predicting\_MSW}
} 
```

# *Waste Management* Paper Citation

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
