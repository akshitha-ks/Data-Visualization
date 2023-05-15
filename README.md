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

sbn.barplot(x=df['Segment'],y=df['Sales'])

plt.title("Highest Sales of the segment")

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

sbn.barplot(x=df['Sales'], y=df['Region'])

plt.title("Sales of Product based on Region")

sbn.lineplot(x=df['Sales'], y=df['Profit'])

plt.title("Relation between Sales and Profit")

grouped_data = df.groupby('Segment')[['Sales', 'Profit']].mean()

#Create a bar chart of the grouped data

fig, ax = plt.subplots()

ax.bar(grouped_data.index, grouped_data['Sales'], label='Sales')

ax.bar(grouped_data.index, grouped_data['Profit'], bottom=grouped_data['Sales'], label='Profit')

ax.set_xlabel('Segment')

ax.set_ylabel('Value')

ax.legend()

plt.title("Sales and Profit based on Segment")

plt.show()

grouped_data = df.groupby('City')[['Sales', 'Profit']].mean()

#Create a bar chart of the grouped data

fig, ax = plt.subplots()

ax.bar(grouped_data.index, grouped_data['Sales'], label='Sales')

ax.bar(grouped_data.index, grouped_data['Profit'], bottom=grouped_data['Sales'], label='Profit')

ax.set_xlabel('City')

ax.set_ylabel('Value')

ax.legend()

plt.title("Sales and Profit based on City")

plt.show()

grouped_data = df.groupby('State')[['Sales', 'Profit']].mean()

#Create a bar chart of the grouped data

fig, ax = plt.subplots()

ax.bar(grouped_data.index, grouped_data['Sales'], label='Sales')

ax.bar(grouped_data.index, grouped_data['Profit'], bottom=grouped_data['Sales'], label='Profit')

ax.set_xlabel('State')

ax.set_ylabel('Value')

ax.legend()

plt.title("Sales and Profit based on States")

grouped_data = df.groupby(['Segment', 'Ship Mode'])[['Sales', 'Profit']].mean()

pivot_data = grouped_data.reset_index().pivot(index='Segment', columns='Ship Mode', values=['Sales', 'Profit'])

#Create a bar chart of the grouped data

fig, ax = plt.subplots()

pivot_data.plot(kind='bar', ax=ax)

ax.set_xlabel('Segment')

ax.set_ylabel('Value')

plt.legend(title='Ship Mode')

plt.legend(loc="best")

plt.title("Sales and Profit based on Segment and Ship mode")

plt.show()

grouped_data = df.groupby(['Segment', 'Ship Mode','Region'])[['Sales', 'Profit']].mean()

pivot_data = grouped_data.reset_index().pivot(index=['Segment', 'Ship Mode'], columns='Region', values=['Sales', 'Profit'])

sbn.set_style("whitegrid")

sbn.set_palette("Set1")

pivot_data.plot(kind='bar', stacked=True, figsize=(8, 5))

plt.legend(title='Region')

plt.legend(loc='best')

plt.title("Sales and Profit based on Segment,Ship mode and Region")



# OUTPUT:

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/bbc07b9a-e48b-43e8-9ff1-782c53da7a00)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/d65e7fe8-d4c6-4cba-97ba-bd3c0c067d77)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/68dbbc72-3b9a-43fe-b6cf-e90646ac458b)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/cbf5bc9f-5e2f-4152-8ed1-e66aef90426c)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/9583ccf2-aa8b-4824-9a9f-57d55dfe85a9)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/2151cac0-60ba-41fb-b3d3-ec9cb15fc32d)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/e29d03e8-69b9-46ad-9f08-1ee46a3c616e)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/0c03c066-e8a2-4efa-adca-c6cc854520ea)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/cac9b8eb-0a3f-4096-8f93-a80f6fa1acf3)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/f56edb9f-6964-4e61-9fab-0597bbd866ce)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/f5cf0f09-78da-4a1f-800b-47419d1ccd05)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/3bf4d97a-ce3f-4e07-a71b-2e9c575d7a3a)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/96f97dde-5160-40d5-8e45-e29a3b05ae02)

![image](https://github.com/akshitha-ks/Data-Visualization/assets/123535064/18df6e55-22ce-4a64-a785-484f02b11ac7)



# RESULT:

  Thus, the Feature Visualization for the given datasets had been executed successfully.
