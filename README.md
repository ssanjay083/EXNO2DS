# EXNO2DS
      Name:Sanjay S
      Reg No: 212224110047
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
      import pandas as pd
      import numpy as np
      import matplotlib.pyplot as plt
      import seaborn as sns
![image](https://github.com/user-attachments/assets/957da68d-d668-4f0e-af24-a164c3779f05)

      dt.info()
![image](https://github.com/user-attachments/assets/8f7a0711-1029-4e14-873e-b7103c83ecfc)

      dt.nunique()
![image](https://github.com/user-attachments/assets/880a7855-22c1-46e3-9364-a786e080c652)

      dt["Survived"].value_counts()
![image](https://github.com/user-attachments/assets/a7fd5d5b-f938-4e94-ab61-51cb0f1b19f2)

      dt.shape()
![image](https://github.com/user-attachments/assets/ed75a6fa-169e-4035-9168-e9e589aa21cb)

      dt.describe()
![image](https://github.com/user-attachments/assets/1950797e-a754-4937-8fcf-74f2fd24d90c)

      per = (dt["Survived"].value_counts() / dt.shape[0] * [100]).round(2)
      per
![image](https://github.com/user-attachments/assets/07c7e5d6-2528-4403-a21d-0b37cbdba5bd)

      sns.countplot(data=dt,x="Survived")
![image](https://github.com/user-attachments/assets/8d7c5750-fe49-482b-aea6-3aeff26b5653)

      dt
![image](https://github.com/user-attachments/assets/09d1af97-d973-4ffd-915d-088869e34daf)

      dt.Pclass.unique()
![image](https://github.com/user-attachments/assets/5e1322f4-6a81-4c47-9e61-c37e8e248b31)

      dt.rename(columns={'Sex':'Gender'},inplace=True)
      dt
![image](https://github.com/user-attachments/assets/37489d8d-5811-40cf-a9d6-49c75a4f339a)

      sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)
![image](https://github.com/user-attachments/assets/3e2adde3-751d-498f-9da1-ee4a15e8af45)

      sns.catplot(x="Survived",hue="Gender",data=dt,kind="count")
![image](https://github.com/user-attachments/assets/30e53759-c9f4-4f2e-8fa9-4b536d2d6ca1)

      dt.boxplot(column="Age",by="Survived")
![image](https://github.com/user-attachments/assets/fdea9090-e57b-4303-b1b1-981f7190f761)

      sns.scatterplot(x=dt["Age"],y=dt["Fare"])
![image](https://github.com/user-attachments/assets/df916a8d-b151-4572-b1a7-df559b2a9ca5)

      sns.jointplot(x="Age",y="Fare",data=dt)
![image](https://github.com/user-attachments/assets/efec451d-2b30-4e52-9366-85903b71a5d3)

      fig,ax1=plt.subplots(figsize=(8,5))
      pt=sns.boxplot(ax=ax1,x="Pclass",y="Age",hue="Gender",data=dt)
![image](https://github.com/user-attachments/assets/dd3aa773-2ba1-4ff3-8ded-1f6ecbcc5565)

      sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")
![image](https://github.com/user-attachments/assets/a849edd9-44b4-4d78-b508-17a0d687d049)

Co-relation
     
      corr=dt.corr()
      sns.heatmap(corr,annot=True)
![image](https://github.com/user-attachments/assets/62926709-fef1-45f6-858f-5bb81caed062)

      sns.pairplot(dt)
![image](https://github.com/user-attachments/assets/a2945300-723b-467b-ab32-5156dd562849)

# RESULT
        The Exploratory Data Analysis was successfully completed by examining data distribution, outliers, and anomalies.
