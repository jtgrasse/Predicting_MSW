# About Dataset

This GitHub repository contains compiled data from published waste characterization studies with intent for training waste composition prediction models. The data is first used in a study published in the journal *Waste Management* https://doi.org/10.1016/j.wasman.2024.12.002

## About Data collection methodology

Each of the data points comes from a report called a "Waste Characterization Study." Some reports have multiple data points, such as a data point for each county in a state. The data has been manually extracted from each report PDF by the project team. Furthermore, each datapoint may use a different set of material categories, so the team manually translated the data into the common characterization. This process is described in detail in the aforementioned paper.

### Description of the data

The original reports (all of which are PDFs) are contained in the "Characterization Studies Used" folder. These copies are retained, because their location on various government repositories tends to move.

The resulting data table has 3 description columns, 43 detailed waste material category columns, and 12 aggregated waste category columns. The description for each datapoint contains the following:
1. Note - This is a description of the area covered by the data
2. Year - This is the year that the data was gathered (note: this may not be the year the data was published)
3. FIPS - This is a list of the FIPS codes associated with the counties that are represented by the data.

# Dataset Citation

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
