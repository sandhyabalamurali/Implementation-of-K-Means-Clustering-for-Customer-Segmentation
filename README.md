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
data = pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]   #Within-Cluster Sum of Squares.

for i in range(1,11):
    kmeans=KMeans(n_clusters=i, init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
    
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("ELBOW METHOD GRAPH")
plt.show()
km = KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="green",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="purple",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="gold",label="cluster4")
plt.legend()
plt.title("Customer Segments")
 
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


## K means cluster:

![Screenshot 2023-11-11 204130](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/a55d2c97-7942-4908-b594-5be59e6d4e30)


## CUSTOMER SEGMENT GRAPH:

![pic](https://github.com/sandhyabalamurali/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115525118/82c5cd6e-b90d-4e41-b68b-b44d923a55c0)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
