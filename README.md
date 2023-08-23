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













# Loan_data.csv

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
df=pd.read_csv("Loan_data.csv")
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
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df.isnull().sum()
```
```
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.isnull().sum()
```
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mode()[0])
df.isnull().sum()
```
### MEDIAN
```
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.isnull().sum()
```
## DROP
```
df=df.dropna(subset='Gender')
df.isnull().sum()
```
```
df=df.dropna(subset='LoanAmount')
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
![data1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/ee1c0b05-3b24-46b2-9136-7ae874842367)

![data2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/a4b45d8d-2556-4f93-94a1-af66c1c2bc14)

![data3](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/77932e8d-17f2-46be-9ae8-d01b1478d9ac)

## NON NULL BEFORE
![non null 1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/bfe2be28-325b-434b-9c1b-bf6f2e09ad7e)

![non null2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/888a9c81-cf59-463d-af3b-74951e9dc381)

## FILLING
### MODE
![mode1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/5dc7b7cb-4639-435d-a5ba-ee8f514c6fa4)

![mode2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/b5d3df47-b7e4-479a-86f5-c7ff6ea21bed)

![mode3](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/edf6c763-f2a9-4d2a-bcf2-e79fb6967fc3)

### MEDIAN
![median1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/9de1ee4e-0aa4-48b1-9e7c-593de6fc1901)

## DROP
![drop1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/c1bbe7fe-748d-4e1d-8004-132495ffb51c)

![drop2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/ac5f4247-7026-4350-a16c-0ee57a87c0af)

## NON NULL AFTER
![non null after1](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/52187caa-cfd3-4b62-84dd-66ffba147ab9)

![non null after2](https://github.com/bharathraj1905/ODD2023-Datascience-Ex01/assets/121490575/828092d7-37ed-4364-aef1-84b84697befd)

## RESULT
thus,the given data is read,cleansed and the cleaned data is saved into the file 


