
# PowerBI Data Analysis

## Data Professional Survey Breakdown Analysis

### Table of Contents

- [Project Description](#project-description)
- [Data Source](#data-source)
- [Data Cleaning](#data-cleaning)
- [Tools](#tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
  

### Project Description
The project aims to create a comprehensive dashboard to analyze the data professional survey responses. We have analyzed the salary breakdown, language preference, whether they are happy with their work, and others.
![Data Professional Survey Breakdown Dashboard image](Survey%20Dashboard.png)

### Data Source
- Data professional survey response Data: The data is available in the "Power BI - Final Project.xlsx" file which contains all the responses to the survey.

### Tools
- Power BI Desktop: For data cleaning and visualization.

### Data Cleaning
- In the Power BI Desktop, we have inserted the xlsx data. I have checked each column for missing values and formatting issues. I have also checked whether the datatypes assigned to each column are correct. I have created an average salary column from the range of salary provided by the surveyor. I have also combined various languages which are not as common into one group known as others.  

### Exploratory Data Analysis
Performed some exploratory data analysis to find some information about key questions like
- Total number of surveyors and how many of them are male and female.
- From which country the survey is taken?
- What is the average salary for the different data jobs?
- What is your favorite programming language in each field?
- Whether the employee happy with the salary and work-life balance?

### Data Analysis
To find the answer to the key questions, I have written some query in the MySQL as
``` PowerBI
Female count = CALCULATE(COUNTROWS('Data Professional Survey'), 'Data Professional Survey'[Q9 - Male/Female?] = "Female")
```
``` PowerBI
Male count = SUMX('Data Professional Survey', IF('Data Professional Survey'[Q9 - Male/Female?] = "Male", 1,0))
```

### Results/Findings
- The average age of the surveyor is 29 years.
- The surveyor has mixed feelings about the current work-life balance.
- Surveyor are not happy with their current salary.
- Python is the favorite language among the data analyst.
- Data Scientist is the highest earned job.
