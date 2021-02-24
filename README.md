# Forecasting Covid-19 Cases
### _Data Science Bootcamp Final Project_ 

### The Project Goal:
 **_Forecast (predict) the number of (Covid -19) new cases over time_**
 ___

### The Dataseat:
- [owid-covid-data.csv](https://www.kaggle.com/tunguz/data-on-covid19-coronavirus?utm_medium=social&utm_campaign=kaggle-dataset-share&utm_source=twitter)

  
### Tools & Packages used in the Project:
**Tools** 

 - Python 3.8
 - Jupyter Lab
 - Tableau
 
**Packages:**

 - Pandas 
 - Matplotlib
 - Seaborn
 - Datetime
 - Sklearn
 - Fbprophet

## Project Workflow:
### The Project has 3 Phases:
#### Phase 1: Filling the Null Values 
- All the columns had null values except "date" and "total_cases" 
- Techniques used to fill the Null Values :
  - Fill the columns based on other columns like the "iso_code" & "continen"t columns  based on what in the "location" column
  - Dropped rows that duplicated or the "new_cases" for the "location"column was Null like Hong Kong
  - Use LinearRegression Model to fill columns like "new_deaths_smoothe"
  
**This Phase outed new dataseat had fewer null values named [“Owid-covid-data-filled.csv”](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/data/Owid-covid-data-filled.csv)**




 
    




