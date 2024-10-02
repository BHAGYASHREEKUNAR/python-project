# python-project
import pandas as pd
import numpy as nm
import matplotlib.pyplot as plt
import seaborn as sns
housing = pd.read_csv('C:/Users/KIIT/Downloads/housing.csv')
print(housing.head())


housing.info()

housing.dropna(inplace= True)
housing.info

      
from sklearn.model_selection import train_test_split
X = housing.drop(['median_house_value'], axis=1)
y = housing['median_house_value']
X


y

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2 )
train_housing = X_train.join(y_train)
train_housing



train_housing.hist(figsize=(15,8))

