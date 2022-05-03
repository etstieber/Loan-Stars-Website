# Loan Default Prediction

This website showcases our final project for FIN 377 - Data Science for Finance course at Lehigh University.

To see our complete analysis file, click [here](https://github.com/julioveracruz/testwebsite/blob/main/notebooks/example.ipynb).
**update analysis file link**

## Table of contents
1. [Introduction](#introduction)
2. [Methodology](#meth)
    1. [Data Collection](#DC)
    2. [EDA](#EDA)
    3. [Pre-processing](#PP)
    4. [Optimizing](#Op)
    5. [Model Selection](#MS)
3. [Analysis](#Analysis)
4. [Conclusion](#conclusion)
5. [About the Team](#about)

## Introduction  <a name="introduction"></a>

The main goal of this project is to explore machine learning models that can best predict loan defaults using data such as standard loan factors, macroeconomic data, and market conditions. 

## Methodology <a name="meth"></a>

We outlined and completed this project through steps of:

- Data Collection
- EDA
- Pre-processing
- Optimizing
- Model Selection

Here is some code that we used to develop our analysis.
 
### Data Collection <a name="DC"></a>
```python
lending = pd.read_csv("input/lending_data.csv")

inf = pdr.DataReader(["T5YIE"], "fred",datetime(2005,1,1), end =datetime(2022,4,1) )
inf.to_csv("input/inflation_exp.csv")

stfips = pd.read_csv("dev/state_fips.csv",skipinitialspace=True)

state_list = pd.DataFrame(lending["addr_state"].unique())
state_list = stfips.merge(state_list, on = "state", how  = "left")
``` 
We read leanding data that we downloaded from kaggle. This is our main dataset and what we build off of to incorporate other variables for our algorithm. Additionally included is some of the add-on data and modifications such as inflation from FRED. You can see the full download_data workbook [here (https://github.com/LeDataSciFi/project-loan-stars/blob/main/download_data.ipynb).

 
### EDA - Exploratory Data Analysis <a name="EDA"></a>
```python
EDA Code Here.
```

### Pre-processing <a name="PP"></a>
```python
PP Code Here.
``` 

### Optimizing <a name="Op"></a>
```python
Optimizing Code Here.
``` 

### Model Selection <a name="MS"></a>
```python
Model Selection Code Here.
``` 

**You have to copy in output/figures from the notebooks.**



## Analysis <a name="Analysis"></a>

Here are some graphs that we created in our analysis. We saved them to the `pics/` subfolder and include them via the usual markdown syntax for pictures.

![](pics/plot1.png)
<br><br>
Some analysis here
<br><br>
![](pics/plot2.png)
<br><br>
More analysis here.
<br><br>
![](pics/plot3.png)
<br><br>
More analysis.

## Conclusion <a name="conclusion"></a>

xxx



## About the Team <a name="about"></a>

<img src="pics/2.jpeg" alt="don" width="300"/>
<br>
Wasti is a Senior '22 Finance major with minors in Data Science and Mathematics. Upon graduation he will return to Lehigh as a Masters of Financial Engineering candidate.
<br><br><br>
<img src="pics/Headshot.JPEG" alt="Eric" width="300"/>
<br>
Eric is a Senior '22 Finance major. Upon graduation he will begin his career as a Financial Services Advisory Associate at KPMG in their NYC Office.
<br><br><br>
<img src="pics/CompositePicture.jpeg" alt="Colin" width="300"/>
<br>
Colin is a Senior '22 Finance major with a minor in Psychology.   


## More 

To view the GitHub repo for this website, click [here](https://github.com/etstieber/Loan-Stars).
