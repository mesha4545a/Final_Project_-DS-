# Forecasting Covid-19 Cases
### _Data Science Bootcamp Final Project_ 

### The Project:
 - [Forecasting Covid-19 Cases](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/ML_Final/ML_Final.md)
 
 - **_Purpose This project aimed to utilize machine learning on the Covid-19 dataset to predict the future number New cases for ('International, World, Saudi Arabia)**
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


#### Phase 2: Exploratory Data Analysis 
- This phase is done by Jupiter lab and tableau simulations
  - [EDA part](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/EDA/EDA.md)
  - [Tableau part](https://public.tableau.com/views/EDAVis/Sheet2?:language=en&:display_count=y&publish=yes&:origin=viz_share_link)
- **insight:**
  -  There columns that contain null values that should  be dropped 
  -  Europe data were represented as” Europe” and “Europe Union”
  - The location contains some continent
  - The location contains "World"  and "international" 
  -  It logical to forecast every location by itself 

  
**This Phase resulted in:**
- **a new dataset that has no Null Value named [EDA.csv](https://github.com/mesha4545a/Final_Project_-DS-/blob/main/data/EDA.csv)**
- **tableau dashboard [here](https://public.tableau.com/views/EDAVis/Dashboard1?:language=en&:display_count=y&publish=yes&:origin=viz_share_link)**


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

***

### Component Plots:

#### International Component Plot


![output_49_0](https://user-images.githubusercontent.com/48656800/109057109-6266ce80-76f2-11eb-921c-497bd5c3a0a3.png)


- As seen in trend it appears that the number of new cases of covid-19 was high at the start  then it started to come down to 0 and stand like that until the last date recorded
- As observed  in "weekly" the highest number of cases is on Monday 

****

#### World Component Plot


![output_60_0](https://user-images.githubusercontent.com/48656800/109058653-4fed9480-76f4-11eb-8f4b-2d34191e0a98.png)


- As seen in trend it appears that the number of new cases of covid-19 was 0 at the start then it started to come up  at the end of 2020 to 6 and start to slowly decrease 
- As seen in” weekly" it appears that the number of cases is highest between Wednesday and fraidy 

***

#### Saudi Arabia Component Plot


![output_71_0](https://user-images.githubusercontent.com/48656800/109059680-8d065680-76f5-11eb-83d2-7772c4f1d7db.png)


- As seen in trend it appears that the number of new cases of covid-19 was less than 0 at the start then it started to come up then  start to slowly decrease  and return to less than 0
- As seen in” weekly it appears that the number of cases is highest is on Friday and Monday 

***

### Comparing performance between Baseline Model and Facebook prophet Model

-  Comparing performance base on  mean absolute error 


 #### International dataset 
 
 - Baseline Model: 8.011111111111111
 - Facebook Prophet:2.430505

#### World dataset 

 - Baseline Model: 487182.5
 - Facebook Prophet: 297002.705972
 
#### Saudi dataset 

 - Baseline Model: 804.3555555555556
 - Facebook Prophet: 2235.389194
 
#### Conclusion 

- Facebook prophet Model is more accurate than the Baseline Model 
- Facebook prophet has more functions that make handling time series easier and accurate
 
    




