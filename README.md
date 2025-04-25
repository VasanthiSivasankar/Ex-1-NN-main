<H3>EVASANTHI SIVASANKAR</H3>
<H3>212223040234</H3>
<H3>EX. NO.1</H3>
<H3>17.03.25</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.impute import SimpleImputer

data = pd.read_csv('Student_Performance_on_an_Entrance_Examination.csv')


print(data.isnull().sum())


print(data.head())

print(data.info())

encoder= OneHotEncoder()

encoded_data= pd.DataFrame(encoder.fit_transform(data[['Gender']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Caste']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['coaching']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Class_ten_education']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['twelve_education']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['medium']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Class_X_Percentage']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Class_XII_Percentage']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Father_occupation']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Mother_occupation']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['time']]).toarray())
encoded_data= pd.DataFrame(encoder.fit_transform(data[['Performance']]).toarray())


x=data.drop('Performance',axis=1)
y=data['Performance']


x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=42)

print("Training data")
print(x_train)
print(y_train)
print("Testing data")
print(x_test)
print(y_test)
print("Length of X_test: ", len(x_test))
```


## OUTPUT:
SHOW YOUR OUTPUT HERE
![image-1](https://github.com/user-attachments/assets/b6b2762b-5af7-45da-8db0-f928a4aac353)
![image-2](https://github.com/user-attachments/assets/8ee632a7-1287-4363-9103-8ad6b0da4c91)
![image-3](https://github.com/user-attachments/assets/47dc6c68-3d1d-4a98-967e-dbd090f5d1b9)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


