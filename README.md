# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries .
2.Read the data frame using pandas.
3.Get the information regarding the null values present in the dataframe.
4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5.Determine training and test data set.
6.Apply k means clustering for customer segmentation

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SANDHYA BN
RegisterNumber: 212222040144
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("mall.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
*/
```

## Output:


## DATA.HEAD():

![Screenshot 2023-11-11 203929](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/40393a8a-a2ad-4b6a-840e-bbc3a3f40ae0)


## DATA.INFO()
![Screenshot 2023-11-11 203939](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/91bffdf2-01b1-4f5e-8b83-71d0ecef9a69)


## DATA.NULL():

![Screenshot 2023-11-11 203947](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/a46ac70a-f927-4dbf-b0e6-0e4c81953898)


## ELBOW METHOD GRAPH:


![Screenshot 2023-11-11 204105](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/39a753e9-80ab-44cb-86b1-6b04aad79553)


## KMEANS CLUSTERS:


![Screenshot 2023-11-11 204120](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/5898815f-11cc-4d4e-aab3-346cee84c5b3)


## CUSTOMER SEGMENT GRAPH :
![Screenshot 2023-11-11 204130](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/a55d2c97-7942-4908-b594-5be59e6d4e30)




## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
