# Ex-01_DS_Data_Cleansing

# Data_set.csv
## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
## DATA
```
import pandas as pd
import numpy as np
df=pd.read_csv("Data_set.csv")
print(df)
```
```
df.head(10)
```
```
df.info()
```
## NON NULL BEFORE
```
df.isnull()
```
```
df.isnull().sum()
```
## FILLING
### MODE
```
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.isnull().sum()
```
```
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.isnull().sum()
```
### MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.isnull().sum()
```
### MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df.isnull().sum()
```
## DROP
```
df=df.dropna(subset='show_name')
df.isnull().sum()
```
```
df=df.dropna(subset='current_overall_rank')
df.isnull().sum()
```
## NON NULL AFTER
```
df.info()
```
```
df.isnull().sum()
```


## OUTPUT
## DATA
![data1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/e036fbe5-bd85-41db-8b20-18c46f077954)

![data2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/75434b12-b5af-4d48-a6da-cecc6894136e)

![data3](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/71d31d12-93d9-4b86-a84d-1304f95d556a)

## NON NULL BEFORE
![non null 1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/6c4a963e-b666-4c2e-b559-2a7711ed2a15)

![non null2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/33c929d3-0d5d-493a-a2d9-d7e03869ef5c)

## FILLING
### MODE
![mode1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/ba566499-adf0-452e-9192-530a4309aa83)

![mode2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/adb961c8-4986-4f78-a92f-c9a46bd27c21)

### MEDIAN
![median1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/3d7fc606-4455-4e54-b55e-8b70847eacad)

### MEAN
![mean1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/0a5cd5bf-f418-4029-b71a-e159b1813cc7)

## DROP
![drop1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/f631b071-0c6d-4e8e-bfe8-d8d226c65ead)

![drop2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/1af523bc-d19a-46cb-819b-b41148dfd5a8)

## NON NULL AFTER
![non null after1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/f1668e3d-793b-4514-b56a-03d7ed09c4e3)

![non null after2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/3b8a2b6c-f9ae-4b81-8ff1-75109f57163c)

## RESULT
thus,the given data is read,cleansed and the cleaned data is saved into the file 













#
