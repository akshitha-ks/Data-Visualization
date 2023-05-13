# Data-Visualization

# AIM:

     To Perform Data Visualization on a complex dataset and save the data to a file.
     
# EXPLANATION:

     Data Visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.
     
# ALGORITHM:

      Step 1: Read the given data.
      
      Step 2: Clean the Data Set using Data Cleaning Process.
      
      Step 3: Apply Feature Generation and selection techniques to all the features of the data set
      
      Step 4: Apply data visualization techniques to identify the patterns of the data.
      
# CODE:

# Superstore.csv

import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

import seaborn as sbn

df=pd.read_csv("/content/Superstore.csv",encoding='windows-1252')

df.head()

df.info()

df.isnull().sum()

sbn.barplot(x=df['Segment'],data=df)

plt.title("Highest Sales of the Segment")

sbn.barplot(x=df['City'],y=df['Profit'])

plt.title("Highest Profit of Cities")

City=df.loc[:,["City","Profit"]]

df.head(5)

City=City.groupby(by=["City"]).sum().sort_values(by="Profit")

plt.figure(figsize=(17,7))

sbn.barplot(x=City.index,y="Profit",data=City)

plt.xticks(rotation = 90)

plt.xlabel=("City")

plt.ylabel=("Profit")

plt.show()

sbn.barplot(x=df['Ship Mode'],y=df['Profit'])

plt.title("Number of profits in Ship Mode")

sbn.barplot(x=df['Region'],y=df['Sales'])

plt.title("Sales of Product based on Region")

sbn.lineplot(x=df['Sales'], y=df['Profit'])

plt.title("Relation between Sales and Profit")

sbn.barplot(x=df['Segment'],y=df['Profit'])

plt.title("Sales and Profit based on Segment")

sbn.barplot(x=df['City'],y=df['Profit'])

plt.title("Sales and Profit based on City")

sbn.barplot(x=df['Region'],y=df['Profit'])

plt.title("Sales and Profit based on States")

sbn.barplot(x=df['Ship Mode'],y=df['Profit'])

plt.title("Sales and Profit based on Ship mode")

sbn.barplot(x=df['Sales'],y=df['Profit'])

plt.title("Sales and Profit based on Segment")


# OUTPUT:

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/bbc07b9a-e48b-43e8-9ff1-782c53da7a00)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/d65e7fe8-d4c6-4cba-97ba-bd3c0c067d77)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/68dbbc72-3b9a-43fe-b6cf-e90646ac458b)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/6fa29f75-3316-49bb-80dc-1aefcad9bd04)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/3ef417c5-302f-4e93-8287-b15db9dbb851)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/553be871-c1b2-4e56-9d8c-c1a4046c6df5)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/c185cfde-dd55-4e0b-8215-85c641b83d94)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/4baf445e-7c17-4d72-94fc-d6d040191eee)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/b9b675aa-1fda-4217-bda3-590d90b85309)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/2ff5089d-5349-4953-b8df-93e07a5f2bcc)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/dc63be52-789e-4afe-adfc-2ea9d95bc282)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/2ddc86a7-ffb7-48e8-bb69-92b760374027)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/52042663-017e-4657-bf2d-de833a5a03ff)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/acb25b43-8782-4732-9384-d7f929cdb63f)


# RESULT:

  Thus, the Feature Visualization for the given datasets had been executed successfully.
