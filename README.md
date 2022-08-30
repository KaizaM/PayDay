# PayDay
Salary Prediction Tool: https://kaizam.github.io/PayDay/

Create a 'Resources' Folder and input 2016-2022 data from here: https://insights.stackoverflow.com/survey

## Introduction
​As more and more job candidates enter the world of Data Science and Analytics, future candidates ask whether will become a lucrative field to enter. PayDay took on this question to answer this as well as other concerns a future candidate may have. 

The data came from the Annual Stack OverFlow Salary survey (https://insights.stackoverflow.com/survey) for the years 2016 to 2022. 

An analysis of salaries for Data Analysts, Data Scientists, and Machine Learning Engineers was performed using years of experience and year of pay. PayDay took this data and developed a tool to help candidates not only look at the future of salaries, but current salaries for negotiations and to help determine if they are compensated appropriately.
​
## Data
​Once the csv's are downloaded from Stack Overflow, the data needs to be transformed to include only the necessary data. Each set of data includes different columns and datasets requiring manual updating to grab neccessary columns. 

Once needed columns are gathered, editing of the data is required to have only numerical values. For example, the job titles in string format need to be replaced with numerical values for machine learning to be performed.

Each set of data was cleaned using Pandas and Jupyter Notebook. The data used includes the following:
1.	Years of Experience
2.	Job Title
3.	Salary
4.	Company Size
5.  Year of Data (Add Manually)

Due to the wide range of titles in Data Science and Analytics, this was reduced to 3 categories, Data Analyst, Data Science, and Machine Learning Engineer. 
​
This cleansing was performed for all the datasets and then joined into one final dataframe used for machine learning analysis.
​
## Analysis
The machine learning method used in this model is Supervised Linear Regression. To perform this analysis, 'Salary' was dropped for analysis.

The initial run of linear regression returns a very low testing score due to there being high variability in the data.

Therefore, filtering down the data using percentiles was necessary. The percentiles were based off each year of experience. This was to get the average salaries for each year of experience per title. To perform this, loop through all years of experience and filter out any outlier salaries.

Once filtered down, linear regression should be performed again. If a training and testing score of 75% is achieved, predictions can be made. 

By printing the intercept and coefficent, obtaining a linear formula for the salary prediction is done. 

Output the final dataframes to a csv or excel to be used in Tableau for visualizations.

## Visualizations
Visualizations are created by using Tableau. Exported dataframes are imported into Tableau to make a scatter plot with trend lines for the three different variables (Years of Experience, Job Title, Year).
