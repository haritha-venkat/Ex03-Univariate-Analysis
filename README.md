# Ex03-Univariate-Analysis
# Aim

To read the given data and perform the univariate analysis with different types of plots.
# Explanation

Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
## Algorithm
### Step1

Read the given data.
### Step2

Get the information about the data.
### Step3

Remove the null values from the data.
### Step4

Mention the datatypes from the data.
### Step5

Count the values from the data.
### Step6

Do plots like boxplots,countplot,distribution plot,histogram plot.
# Program
```python
Developed by : harithashree.V
Registration Number : 212222230046

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
```
# OUTPUT
# EDA - SuperStore.csv
![image](https://user-images.githubusercontent.com/121285701/228285604-f0cd9917-a3a9-4397-83f3-eaf7dbc0b313.png)
# Displaying information about Dataset
![image](https://user-images.githubusercontent.com/121285701/228285919-7f731f6a-fe15-4d25-a2d3-56ecd49f51a7.png)
#![image](https://user-images.githubusercontent.com/121285701/228286172-7ab4699d-73e1-426e-a831-6b95cbd029d9.png)
# Finding null values and cleaning it
![image](https://user-images.githubusercontent.com/121285701/228286351-a95661ea-5909-465e-a0a5-1cbd7c936af6.png)
# Value counts of "Postal Code"
![image](https://user-images.githubusercontent.com/121285701/228286482-da21637e-95e8-4a48-bb4f-b4f7a72ac9d5.png)
# Distribution of Data
![image](https://user-images.githubusercontent.com/121285701/228286790-6fa5f493-8fe1-4f20-9ce2-259e079f65e4.png)
# Univariate Analysis
![image](https://user-images.githubusercontent.com/121285701/228286944-3cce392b-833e-47d9-b78d-6d80d928a3ef.png)
![image](https://user-images.githubusercontent.com/121285701/228287014-87d8ac99-d83c-43ce-8e93-9c58d5204612.png)
![image](https://user-images.githubusercontent.com/121285701/228287055-22d428af-949b-4a94-84ba-5f7a48a83285.png)
![image](https://user-images.githubusercontent.com/121285701/228287107-742228ac-bbfb-4c24-a37f-c097b0f80383.png)

![image](https://user-images.githubusercontent.com/121285701/228287143-331a3e1f-30f1-4f9c-9c8c-840fcbf319ef.png)
# RESULT:

Thus the program to perform EDA on the given data set is successfully executed.
