# Urban Growth prediction


### Description

This project analyzes data from the [World Development Index dataset](https://databank.worldbank.org/source/world-development-indicators) of the World Bank. The main motivation is to predict urban population growth for countries and to estimate which factors contribute to urban population growth. This could enable urban planners to make data-driven decisions to ensure cities are prepared for the future growth. The following questions are answered: 

1) How accurately can we predict urban population growth across different countries?
2) What factors contribute the most to urban population growth?
3) What distinguishes the 10 fastest-growing urban areas from those with the slowest growth?
4) How can we use this knowledge for future urban planning?

### Machine learning methods

In the script a Random Forest model is trained to predict urban population growth (% of population). Relevant features are identified using shapley values. 

### Folder structure

* **data**
    * contains the raw data as well as the meta data in **WorldDevelopmentIndicators**
    * data saved during analyses will be stores here
* **img**
    * all plots are saved here
    * **Table_features.png** shows the features used in the analyses
* analyses.ipynb
    * Jupyter notebook script to perform the analyses


### Libraries used

* matplotlib==3.9.4
* numpy==1.26.4
* pandas==2.2.3
* scikit-learn==1.6.1
* seaborn==0.13.2
* shap==0.46.0


### Summary of the results

The code provides a Random Forest model with which you can predict urban population growth (% annual) for individual countries with a RMSE of 1.1. 

The most important predictors, determined by shapley values: 
* **Rural population growth**  - if the overall population is growing, urban areas are likely to expand as well. 
* **Age dependency ratio**  - Countries with a higher proportion of seniors tend to experience lower urban growth, whereas a larger percentage of children correlates with higher urban growth. 
* **Merchandise trade and internet infrastructure**  -  Countries with a lower percentage of merchandise trade as part of their GDP and fewer secure internet servers also experience higher urban population growth
* **Compulsory education (years)**  -  Countries with fewer compulsory years of education tend to have a higher urban population growth
* **Existing urban population size**  -  Interestingly countries with already high urbanization levels tend to have slower urban growth


### Further information

This project is part of the Data Scientist nanodegree from Udacity. You can find the corresponding blog post [here](https://medium.com/@samirasaak/23566a2c571b) to learn more about the results of the analyses.

