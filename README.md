# Forecasting Covid-19 Cases
### _Data Science Bootcamp Final Project_ 

### The Project:
 - [Forecasting Covid-19 Cases](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/ML_Final/ML_Final.md)
 
 - **_The goal is to Forecast (predict) the number of (Covid -19) new cases over time_**
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
#### Phase 1: [Filling the Null Values](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/Null_Fill/Null_Fill.ipynb)  
- All the columns had null values except "date" and "total_cases" 
- Techniques used to fill the Null Values :
  - Fill the columns based on other columns like the "iso_code" & "continen"t columns  based on what in the "location" column
  - Dropped rows that duplicated or the "new_cases" for the "location"column was Null like Hong Kong
  - Use LinearRegression Model to fill columns like "new_deaths_smoothe"
  
**This Phase resulted in a new dataset that has fewer Null values named [“Owid-covid-data-filled.csv”](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/data/Owid-covid-data-filled.csv)**


#### Phase 2: Exploratory Data Analysis [(EDA)](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/EDA/EDA.md)
- This phase is done by Jupiter lab and tableau simulations
- insight:
 -  There columns that contain null values that should  be dropped 
 -  Europe data were represented as” Europe” and “Europe Union”
 - The location contains some continent
 - The location contains "World"  and "international" 
 -  It logical to forecast every location by itself 

  
**This Phase resulted in:**
- **a new dataset that has no Null Value named [EDA.csv](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/data/EDA.csv)**
- **tableau dashboard [here](https://dub01.online.tableau.com/#/site/mesha4544/views/EDA/Dashboard1)**
- 

#### Phase 3: [Forecasting Covied-19 new_cases:](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/ML_Final/ML_Final.md)
- In this Phase, applied  Baseline Model & Facebook Prophet Model
- The  baseline model approach is most recent day reflect the future 

  **Some Difficulty:**
The idea was to use the entire dataset and apply the facebook prophet model to every country 
But due to some technical difficulty(my laptop was close to crash), the idea changed to  apply the model on 
"International", "world" and "Saudi Arabia" locations
---

#### Baseline Model:
In the baseline model, I chose the approach history is the best reflect for the future  
Take the value of the data and shift it one step to represent the future day then repeat this 90 time to represent 90 days into the future 
that as you will see result in a fixed model
#### Baseline Plots:

![output_26_0](https://user-images.githubusercontent.com/48656800/109050036-04ce8400-76ea-11eb-8f8a-2ff35dd02330.png)


![output_27_0](https://user-images.githubusercontent.com/48656800/109050237-37787c80-76ea-11eb-8460-ec41afa8ed24.png)


![output_28_0](https://user-images.githubusercontent.com/48656800/109050304-4a8b4c80-76ea-11eb-9420-02925b74102d.png)


***

#### Facebook's Prophet Model:
By plotting the forecast you can evaluate how is the model dowing 
- The black dots: represrnt the actual data point in the data set 
- The deep blue line: represents the prediction 
- The light blue represents: the boundary of our prediction

#### Forecast Plots:


![output_46_0](https://user-images.githubusercontent.com/48656800/109053492-d05cc700-76ed-11eb-9bca-3df0035a781b.png)



![output_57_0](https://user-images.githubusercontent.com/48656800/109053543-dfdc1000-76ed-11eb-85e7-d7697d33d756.png)



![output_68_0](https://user-images.githubusercontent.com/48656800/109053622-f6826700-76ed-11eb-8047-095549df75fc.png)



As seen can see the prediction line (deep blue line) is  close to the data points(black dots) which is good that means that the model is predicting accurately to some extent 


The model  score better the baseline 



 
    




