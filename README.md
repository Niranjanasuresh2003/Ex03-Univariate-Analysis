# Ex03-Univariate-Analysis

Aim:

To perform Univariate EDA on the given data set

Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

Algorithm

STEP 1

Import the built libraries required to perform EDA and outlier removal.

STEP 2

Read the given csv file

STEP 3

Convert the file into a dataframe and get information of the data.

STEP 4

Return the objects containing counts of unique values using (value_counts()).

STEP 5

Plot the counts in the form of Histogram or Bar Graph.

STEP 6

Use seaborn the bar graph comparison of data can be viewed.

STEP 7

Save the final data set into the file

Program

Name: NIRANJANA DEVI S

Reg no:212221220036


import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)
*/

Output:

Dataset:

![image](https://user-images.githubusercontent.com/129851738/229985651-cdb30612-1ab6-40b8-b60b-4636e3fe3334.png)


Head:

![image](https://user-images.githubusercontent.com/129851738/229985735-0bcfceff-133d-47db-861f-77f9715739b8.png)

Info:

![image](https://user-images.githubusercontent.com/129851738/229985802-5f436c44-92e2-4e2f-8baf-1cfbb50646f9.png)

Describe:

![image](https://user-images.githubusercontent.com/129851738/229985857-cf3bcb54-443d-497c-9630-78498bf3e252.png)

Isnull:

![image](https://user-images.githubusercontent.com/129851738/229985943-0b8430fb-c063-4a5f-bd4a-f181d4ce267a.png)

dtypes:

![image](https://user-images.githubusercontent.com/129851738/229986032-0177439b-9349-4553-93a7-2b24f948eb52.png)

Value count:

![image](https://user-images.githubusercontent.com/129851738/229986116-539ca646-2d79-4c3b-a04e-429a2c277330.png)

Boxplot:

![image](https://user-images.githubusercontent.com/129851738/229986244-a085894d-e937-46e2-8064-3d05c7b68fa1.png)

Countplot:

![image](https://user-images.githubusercontent.com/129851738/229986335-1e0a17d0-053d-4cba-a56b-b3001b15ecfb.png)

Distribution plot:

![image](https://user-images.githubusercontent.com/129851738/229986507-4dd7a2e8-d64c-4b88-b208-98d19570c1ed.png)

Histogram plot:

![image](https://user-images.githubusercontent.com/129851738/229986626-a3cb9ae9-db3d-44e8-8165-553f33321655.png)

Result:

Thus we have read the given data and performed the univariate analysis with different types of plots.











