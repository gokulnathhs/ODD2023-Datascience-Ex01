# Ex-01_DS_Data_Cleansing


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
```

# Data_set.csv :

import pandas as pd
import numpy as np
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('/content/Data_set (1).csv')
df.info()
df.head()
df=df.dropna(subset=['show_name'])
df.head()
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].median())
df.head()
df=df.dropna(subset=['current_overall_rank'])
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.head()
df.info()

# Loan_data.csv :

import pandas as pd
import numpy as np
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('Loan_data.csv')
df.info()
df.head()
df['Gender']=df['Gender'].fillna('Female')
df.head()
df['Dependents']=df['Dependents'].fillna(method='ffill')
df.head()
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
df=df.dropna(subset=['LoanAmount'])
df.head()
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].min())
df.head()
df.info()
```

#  OUTPUT

# Data_set.csv :

# non null before: 

![261836958-ad3b2517-f2e6-4d96-87dc-49810fe0a36c](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/5378c87d-265c-4f9b-bf85-d33a1e4ad508)

![261836963-af56a5e6-27a8-4380-b012-2d9e20a983df](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/fce1c06f-70b7-4db3-9680-d0c4f454ec43)

![261836968-37d0a314-ee3b-4d39-addd-8cb6795f7623](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/836812a7-9abd-45c9-8e4c-6aa38e2eaecf)

![261836973-9e0e6cc2-f09d-4898-9cf9-76790c818b7e](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/39b6ecdd-1e81-4600-b075-a2e62a2d2d5c)

![261836979-ffaace5a-4a9d-47a0-b00f-6f63d540143e](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/6fdc61c3-12ba-477b-bcf6-b23549d05252)

![261836988-837aeda2-4ca6-489c-b23c-fc5c1ef8c1c6](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/761ff3c0-03b1-46b6-96cf-bbb991d089c6)

![261836997-775e4f8d-0748-4cd2-80cd-989947c8828f](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/60c2e7d9-a893-40cf-b4b0-0ac382490761)

# non null after:

![261837110-af870054-b99f-4fd3-af78-c861f5ca3c1d](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/61f90ad5-fb88-4224-a5b6-d60e162d334b)


# Loan_data.csv:

# non null before:

![261837537-e0607ba4-f472-447e-9c9b-33abe5e213b2](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/5b618ad4-47e1-4a2a-82d3-63f355701939)

![261838856-57b6ec7b-9706-4f74-831a-f857cc6d0b64](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/4cdb1ca3-388c-4b20-824a-0620a2b0fbf8)

![261838863-430771e5-e43c-4907-99c6-befaefb7433c](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/7d5c0d40-6ff3-49c4-a463-33f0363a3dc2)

![261838867-dd98d932-ba16-4d00-8c37-50d1b517ce5c](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/2ca4d78b-1a8c-4495-9a91-27165dea5577)

![261838880-9ada9191-d888-4e3d-bc6f-8852791081b8](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/7a6e4088-0380-4649-8944-d6fb47cec2f6)

![261838881-6653be15-acd1-4d58-a4bd-7e0a32e880bd](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/9d858ad5-784a-4953-a048-af9a924fd0c0)

![261838884-608c0170-ba81-4b50-af26-c5df77c74452](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/344b46b7-3d73-4e39-b0fd-3c379a714446)

# non null after: 

![261838894-231e324c-6a95-41ed-bc8d-d3c48d4354b9](https://github.com/22002102/ODD2023-Datascience-Ex01/assets/119091638/637e1dfc-7c62-4c0f-a319-4ce532313e51)

# Result:

Thus the given data is read,cleansed and the cleaned data is saved into the file.
