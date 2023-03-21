# Ex-01_DS_Data_Cleansing

# AIM

To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation

Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM

## STEP 1

Read the given Data

## STEP 2

Get the information about the data

## STEP 3

Remove the null values from the data

## STEP 4

Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT

### DATA:

![image](https://user-images.githubusercontent.com/120443233/226582576-636862c4-3fc0-4876-9457-fe2138a672a4.png)

### NON NULL BEFORE:

### df.info:

![image](https://user-images.githubusercontent.com/120443233/226582812-08f0ed33-fd1f-42b4-b7f6-3814c7498b44.png)

### MODE:

![image](https://user-images.githubusercontent.com/120443233/226582958-33098f3f-42e7-4c6f-8037-f4e2e01fb881.png)

# MEAN:

![image](https://user-images.githubusercontent.com/120443233/226583766-9885c0d0-9845-44a6-a24a-92a0c90bc224.png)

### MEDIAN:

![image](https://user-images.githubusercontent.com/120443233/226583903-2b08c0ff-7505-4428-91aa-89cc3128a69b.png)

### NON NULL AFTER:

### df.info:

![image](https://user-images.githubusercontent.com/120443233/226584192-458bd643-eaad-4ebd-88db-14ebcd37ee60.png)

### df.isnull().sum():

![image](https://user-images.githubusercontent.com/120443233/226584575-8b0bafa1-1648-41a8-a4b6-ae4f77208b98.png)

RESULT:

Thus,the given data is read,cleared and the cleaned data is saved into the file.






















