# Tholkapian_N_PATP_exp02
# Experiment-2-Data-Visualization-Using-Matplotlib-and-Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm

1.  **Start.**
2.  Import the Matplotlib and Seaborn libraries.
3.  Load data into a Pandas DataFrame.
4.  Plot a histogram for age distribution using `plt.hist()`.
5.  Plot a scatter plot for Age vs. Salary using `sns.scatterplot()`.
6.  Plot salary distribution using `sns.boxplot()`.
7.  Show the plots sequentially.
8.  **Stop.**


## Program
## Input 1
## Create Dataset
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
# Create  dataset
data ={
    'Age': [23,34,25,45,42,31,22,29,33,24],
    'Salary': [30000,35000,40000,56000,34000,20000,40000,26000,37000,40000],
    'Salary_color':["red","lightblue","gold","orange","yellow","green", "violet", "pink"
, "brown","darkblue"]
    }
df= pd.DataFrame(data)
print("\nDataset:")
print(df)
```
## Output 1
```
Dataset:
   Age  Salary Salary_color
0   23   30000          red
1   34   35000    lightblue
2   25   40000         gold
3   45   56000       orange
4   42   34000       yellow
5   31   20000        green
6   22   40000       violet
7   29   26000         pink
8   33   37000        brown
9   24   40000     darkblue
```
## Input 2
## Histrogram
```
plt.figure(figsize=(10,4))
plt.hist(df['Age'], bins=10, color='red', edgecolor='black')
plt.title("Age distribution")
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
```
## Output 2

<img width="846" height="393" alt="image" src="https://github.com/user-attachments/assets/b893bedc-6645-4707-95eb-74a0202ed8c4" />

## Input 3
## Scatter plot
```
plt.figure(figsize=(6,4))
sns.scatterplot(x='Age', y='Salary', data=df, color='green')
plt.title("Age vs Salary")
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
````
## Output 3

<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/36c711d6-5282-420d-ac32-05d33b240101" />

## Input 4
## Piechart
```
plt.figure(figsize=(6,6))
plt.pie(
    df['Salary'],
    labels=df['Age'],
    colors=df['Salary_color'],
    autopct='%1.1f%%'
)
plt.title("Salary distribution by Age")
plt.show()
```
## Output 4

<img width="481" height="504" alt="image" src="https://github.com/user-attachments/assets/e6f9fb99-71b8-44fa-acea-790a16d5b37c" />


## Input 5
## Box plot
```
plt.figure(figsize=(6,4))
sns.boxplot(x=df['Salary'], color='gold')
plt.title('Salary Distribution')
plt.xlabel('Salary')
plt.show()
```
## Output 5

<img width="489" height="393" alt="image" src="https://github.com/user-attachments/assets/d3c8e563-4979-42ae-a877-b5a709bcee21" />

## Result
Thus, the dataset was successfully created and visualized using Matplotlib and Seaborn libraries. Histogram, scatter plot, and box plot were generated to analyze age distribution, the relationship between age and salary, and salary distribution, respectively.
