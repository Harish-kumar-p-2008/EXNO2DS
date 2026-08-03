# EXNO2DS
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
```
import pandas as pd
df=pd.read_csv("titanic_dataset.csv")
print(df)
```
![alt text](<Screenshot 2026-08-03 160127.png>)
![alt text](<Screenshot 2026-08-03 160133.png>)

```
df.info()
```
![alt text](<Screenshot 2026-08-03 160140.png>)

```
df.dtypes
```
![alt text](<Screenshot 2026-08-03 160147.png>)
```
df.shape
```
![alt text](<Screenshot 2026-08-03 160153.png>)

```
df.describe()
```
![alt text](<Screenshot 2026-08-03 160201.png>)

```
df.value_counts()
```
![alt text](<Screenshot 2026-08-03 160211.png>)

```
df["Survived"].value_counts()
```
![alt text](<Screenshot 2026-08-03 160221.png>)

```
df.nunique()
```
![alt text](<Screenshot 2026-08-03 160229.png>)

```
import seaborn as sns
sns.boxplot(data=df,x="Age")
```
![alt text](<Screenshot 2026-08-03 160247.png>)

```
sns.countplot(data=df,x="Survived")
```
![alt text](<Screenshot 2026-08-03 160255.png>)

```
sns.histplot(data=df,x="Age")
```
![alt text](<Screenshot 2026-08-03 160302.png>)

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
![alt text](<Screenshot 2026-08-03 160314.png>)

```
sns.catplot(x="Gender",col="Survived",kind="count",data=df)
```
![alt text](<Screenshot 2026-08-03 160324.png>)

```
sns.scatterplot(x=df['Age'], y=df['Fare'])
```
![alt text](<Screenshot 2026-08-03 160335.png>)
```
sns.boxplot(x=df['Survived'], y=df['Age'])
```
![alt text](<Screenshot 2026-08-03 160343.png>)

```
sns.barplot(x=df['Survived'], y=df['Age'])
```
![alt text](<Screenshot 2026-08-03 160349.png>)
```
sns.boxplot(x='Pclass', y='Age', hue='Gender', data=df)
```
![alt text](<Screenshot 2026-08-03 160356.png>)

```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![alt text](<Screenshot 2026-08-03 160405.png>)

```
corr=df.corr()
sns.heatmap(corr,annot=True)
```
![alt text](<Screenshot 2026-08-03 154746.png>)

# RESULT
Thus, the Performed Exploratory Data Analysis on the given data set executed successfully.
