Experiment 1

import numpy as np 
import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt 
%matplotlib inline 

df=pd.read_csv("california_housing.csv") 
df.head() 

df.shape 
df.info() 
df.describe()
list(df.columns) 
df.isnull().values.any() 
df.duplicated().sum() 
df.isnull().sum() 

df['median_income'].hist() 

df.hist(bins=30, figsize=(12, 10), edgecolor='black') 

sns.boxplot(y=df['population']) 
plt.show()

sns.boxplot(y=df['housing_median_age']) 
plt.show()

sns.distplot(df['housing_median_age']) 

df.hist(stacked=False, bins=100, figsize=(12,40), layout=(14,2));
