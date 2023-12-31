# Data Wrangling using Excel
Data wrangling is a crucial step in any data analysis project, and for this project, Excel was the primary tool utilized for this purpose. Leveraging the powerful features of Excel, we performed various data cleaning, filtering, and transformation tasks to ensure the dataset was ready for analysis. Below are some of the key techniques employed during the data wrangling process:

## Dataset
This Dataset was downloaded on [Kaggle](https://www.kaggle.com/datasets/asterfung/ds-obsdbhk), A dataset about job posting in JobsDB.com.
File name should be data-scientist-2022-12-06-1.csv
Here is the dataset heading extracted on Kaggle:

| column | null placeholder | non-null example |
|---|---|---|
| title | (not applicable) | Data Analyst - Top ranked Virtual Bank |
| salary | "salary" | HK$35,000 - HK$55,000 /month |
| company | "company" | CGP |
| posted | (not applicable) | 2022-11-18 |
| District | "district" | Shatin district |
| job description | (not applicable) | Job Description:  Research, collate, obtain and analyze data ... |
| Career level | empty | Entry Level |
| Years of Experience | empty | N/A |
| Company Website | empty | www.companyname.com |
| Qualification | empty | Degree |
| Job Type | empty | Full Time, Permanent |
| Job Functions | empty | Banking / Finance, Others, Information Technology (IT), Others, Data Scientist |
| url | empty | https://hk.jobsdb.com/hk/en/job/data-analyst-data-governance-... |


I saved it as data-scientist-2022-12-06-1 Before.csv and here is the column count for the dataset

![count](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Count.png)

## Data Cleaning
I carefully examined the dataset to identify and handle any missing or erroneous data. Using Excel's functions and formulas, I addressed missing values, corrected inconsistencies, and resolved data formatting issues to ensure the integrity and quality of the dataset.

### Duplicate data
Since JobsDB.com is a job posting website and it allows employer repost the advertisement, so duplicate data should be deleted to reflect the real statistic

![Duplicate](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Duplicate.png)

### List of Data

| column | Keep?(Y/N) | Missing data |
|---|---|---|
| title | Y | Not found |
| salary | Y | too few data |
| company | N | Deleted |
| posted | Y | Not found |
| District | Y | Not found |
| job description | Y | Not found |
| Career level | Y | Marked as 'No mention' |
| Years of Experience | Y | Replaced from job description, Marked as 'No mention' if No data in Replaced from job description |
| Company Website | N | Deleted |
| Qualification | Y | Replaced from job description, Marked as 'No mention' if No data in Replaced from job description |
| Job Type | Y | Not found |
| Job Functions | Y | Not found |
| url | N | Deleted |

### Replacing values

For some specific columns, we need to get information from 'job description', I use the 'Keywords' to extract the data, here is the example:

![Replace](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Replacing%20values.png)


## Data Transformation
Excel's powerful data transformation features were utilized to derive new variables and restructure the data as needed. I performed calculations, created new columns, and transformed the data to a format suitable for further analysis. This step involved various Excel functions, such as text functions, date functions, and mathematical operations

### Job title
I specparte the data professional into few categories, and tried to format those jobs from different job title name.
![title](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Job%20title.png)


### Job Responsiblity and Job Requirement

I tried to specparte the Job Responsiblities and Job Requirements from 'job description' column, It is easy for me to viualize the result between responsiblities and requirements

![Responsiblity](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Job%20Responsiblity.png)


### Job Function

As employer might include more than one job function, I sperated the job function into mutiple columns using 'Text to column' function

![Function](https://github.com/24billys/JobsDB-data-anlysis/blob/main/Excel%20%26%20powerBI%20project/Data%20Wrangling%20(Excel)/Job%20Function.png)


Throughout the data wrangling process, I maintained thorough documentation of the steps undertaken, ensuring transparency and reproducibility. The clean and transformed dataset served as the foundation for our subsequent data analysis and visualization using Power BI.

