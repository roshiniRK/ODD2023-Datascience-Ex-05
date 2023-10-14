# Ex:05 FEATURE GENERATION :
## AIM : 
To read the given data and perform Feature Generation process and save the data to a file.
## EXPLANATION :
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
## ALGORITHM :
### STEP 1 :
Read the given Data
### STEP 2 :
Clean the Data Set using Data Cleaning Process
### STEP 3 :
Apply Feature Generation techniques to all the feature of the data set
### STEP 4 :
Save the data to the file
## PROGRAM : 

### NAME : ROSHINI RK
### REG NO : 212222230123

### Encoding.csv :
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
## OUTPUT :
## For encoding.csv file

![ds 1](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/6c34ae2c-4d52-456d-bb59-9b7f5cc8f3fe)

![ds 2](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/21345ca8-6a5e-4d97-8915-5768d2a2b1ff)

![ds 3](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/c0a9c907-2093-4843-9cf0-90733db72cdd)

![ds 4](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/4256251a-0674-4582-a620-a496043a3901)

![ds new6 ](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/845df31e-9fcb-4875-a1e7-3ac70619dc37)
![ds 6](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/d2e22be5-704d-49c7-bb93-68500443d07a)

### Data.csv :
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
## OUTPUT :
## For Data.csv file

![ds 7](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/c0cf7a08-e44a-43f1-b950-535934cbe5d6)

![ds 8](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/1e68c3e1-d24f-45c1-a2cd-064faf4bfb2d)

![ds 9](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/a299b218-7585-4b86-a770-a432c7d7e6f6)
![ds 10](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/0bf8837c-21dd-4b8f-a46c-385e8bf736a7)

![ds 11](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/84ada579-4192-4bac-9878-821db5289436)

![ds 12](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/d2897922-ec3d-4940-bf0a-0e8bc043d787)
![ds 13](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/6f0d391e-3702-40b5-9a37-03eb5eae2565)
### BMI.csv file
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
### OUTPUT :
## For bmi.csv file

![ds 14](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/76f9810f-3172-4b60-bdc1-50d44d22333b)

![ds 15](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/dd491703-47c8-45f0-86a3-c56c9bd8cc1a)

![ds 16](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-05/assets/119393935/2c20cca9-b38d-49cc-8e40-47a73e727506)
## RESULT:
The Feature Generation process was performed and saved the data to a file.
