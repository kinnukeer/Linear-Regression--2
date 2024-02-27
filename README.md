# Linear-Regression--2
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
df=pd.read_csv('/content/sample_data/minihomeprices (3).csv')
df.head()
df.describe()
print(df.info())
print(df.isna().sum())
df['bedrooms']=df['bedrooms'].fillna(df['bedrooms'].median())
plt.figure(figsize=(10,7))
plt.title("Bedrooms wise price increase")
plt.xlabel("Bedrooms")
plt.ylabel('price')
sns.scatterplot(x='bedrooms',y='price',data=df)
plt.show()
plt.figure(figsize=(10,7))
plt.title("Bedrooms wise price increase")
plt.xlabel("Bedrooms")
plt.ylabel('price')
sns.barplot(x='bedrooms',y='price',data=df)
plt.show()
plt.figure(figsize=(10,7))
sns.lmplot(x='bedrooms',y='price',data=df)
plt.title(" price and Bedrooms wise price line plot")
plt.xlabel(" house Bedrooms")
plt.ylabel(' house price')
plt.show()
