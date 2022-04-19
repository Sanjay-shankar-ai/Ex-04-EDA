## Ex-04-EDA
## AIM:
To perform EDA on the given data set.

## EXPLANATION:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM:
### STEP 1:
Import the required packages(pandas,numpy,seaborn).

### STEP 2:
Read the given .csv file.

### STEP 3:
Convert the file into a dataframe and get information of the data.

### STEP 4:
Remove the non numerical data columns using drop() method.

### STEP 5:
Replace the null values using (.fillna).

### STEP 6:
Returns object containing counts of unique values using (value_counts()).

### STEP 7:
Plot the counts in the form of Histogram or Bar Graph.

### STEP 8:
Find the pairwise correlation of all columns in the dataframe(.corr()).

### STEP 9:
Save the final data set into the file.

## CODE:
~~~
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("supermarket.csv")
df.info()
df.head()
df.tail()
df.isnull().sum()
df["City"].value_counts()
df["Gender"].value_counts()
df["Payment"].value_counts()
sns.countplot(x="Invoice ID",data=df)
sns.countplot(x="Total",data=df)
sns.countplot(x='gross income',data=df)
sns.countplot(x='Payment',data=df)
sns.displot(df["cogs"])
sns.countplot(x="Gender",hue="Quantity",data=df)
sns.displot(df[df["Product line"]==0]["Total"])
pd.crosstab(df["Payment"],df["Quantity"])
pd.crosstab(df["Gender"],df["Quantity"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
## OUTPUT:
![op1](https://user-images.githubusercontent.com/94231938/163914477-c4234171-734d-4a1d-8b43-6a4884047800.png)

## READ THE DATA:
![op3](https://user-images.githubusercontent.com/94231938/163914591-c0916810-0646-4888-b146-0e7f4f46ea74.jpg)
![op4](https://user-images.githubusercontent.com/94231938/163914686-b37672e6-ad89-4131-9e42-e8bcff3aabce.jpg)

## CHECKING THE MISSING VALUES IN THE DATASET :
![op2](https://user-images.githubusercontent.com/94231938/163914775-ca61db00-5371-4554-b1a2-343a42235045.png)

## Values count:
![op6](https://user-images.githubusercontent.com/94231938/163914886-0291e2bd-c791-4832-90c2-8df838a322dd.png)

## PLOTTING GRAPHS FOR VARIOUS DATASETS :
![op7](https://user-images.githubusercontent.com/94231938/163914978-e838bccd-db6e-442a-9d64-046224f4db1d.jpg)

![op8](https://user-images.githubusercontent.com/94231938/163915098-b43b1dc2-ecc8-4440-8d52-3d92423b8b34.jpg)

![op9](https://user-images.githubusercontent.com/94231938/163915135-5a59aba2-2db6-4364-b15c-c2e3bdb1558c.jpg)

![op10](https://user-images.githubusercontent.com/94231938/163915177-cbbad53e-9a3f-4aee-878b-fcb5adaa9ee5.jpg)

![op11](https://user-images.githubusercontent.com/94231938/163915222-58a800f3-a80d-4b77-a7a8-027c4ac7ef80.jpg)

![op12](https://user-images.githubusercontent.com/94231938/163915273-c5ece19e-6be7-4235-991f-bf00c049f9f6.jpg)

![op14](https://user-images.githubusercontent.com/94231938/163915317-6e2e2b2f-2d26-43f8-af50-408c7dd2ab27.jpg)

![op15](https://user-images.githubusercontent.com/94231938/163915338-fa6e1fd1-b22c-4f94-84bc-4ff9d6165f6b.jpg)

## CORRELATION:
![op16c](https://user-images.githubusercontent.com/94231938/163915416-bfb5963a-2461-4e0e-9ad0-8ea711971703.jpg)

## Heatmap:
![op17h](https://user-images.githubusercontent.com/94231938/163915518-149e48e5-f4b1-4a1c-8ab8-a149d8fd494f.jpg)

## Result:
Thus the Exploratory Data Analysis (EDA) on the given data set is successfully completed.
