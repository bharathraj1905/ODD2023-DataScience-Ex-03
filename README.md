# ODD2023-DataScience-Ex-03
## AIM:
To read the given data and perform the univariate analysis with different types of plots.
## EXPLANATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
## ALGORITHM:
### Step 1:
Read the given data.
### Step 2:
Get the information about the data.
### Step 3:
Remove the null values from the data.
### Step 4:
Mention the datatypes from the data.
### Step 5:
Count the values from the data.
### Step 6:
Do plots like boxplots,countplot,distribution plot,histogram plot.
## PROGRAM:
```
NAME: B.Barathraj
REG NO: 212222230019
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("iris.csv")

df.nunique()
```
```
df.head()
```
```
df.tail()
```
```
df.iloc[:,4].value_counts()
```
```
for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")
```
```
sns.countplot(x='species',data=df)
```
```
dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')
```
```
dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
```
```
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
plt.xlabel('petal_length')
plt.show()
```
```
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()
```
## OUTPUT:
![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/a855e4e9-d879-491a-9fa6-2905e1f0b7c7)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/832526d2-ee2e-4692-ad9c-918beaf23270)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/bb75ec99-62fe-47e2-a7e1-c6ee9541f38f)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/870df2b9-a53e-4d9f-85e2-eb2b79bd861e)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/e9417b11-e2cd-4615-b708-2628e10be41f)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/35e57aeb-9473-4a54-b531-5cd6d2bcb776)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/dfd7912f-1391-4b9c-94af-6f1d14ace2e9)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/5bc985a7-c9b1-4170-a379-2240b7b70ac9)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/51944e5e-ab35-49c6-8e5a-79ffe861c402)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/ab4d9643-fe1b-4959-bbaf-c1dddb604447)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/fcbdeffe-fb09-466f-8859-30edfae82616)

![image](https://github.com/bharathraj1905/ODD2023-DataScience-Ex-03/assets/121490575/68e78e6f-f802-43bb-9917-204234b09188)

## RESULT:
The given datasets are read and outliers are detected and are removed using IQR and z-score methods.
