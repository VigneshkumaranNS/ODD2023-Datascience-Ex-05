# Ex:05 Feature Generation
### AIM
To read the given data and perform Feature Generation process and save the data to a file.

### Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

### ALGORITHM
## STEP 1
Read the given Data.

## STEP 2
Clean the Data Set using Data Cleaning Process.

## STEP 3
Apply Feature Generation techniques to all the feature of the data set.

## STEP 4
Save the data to the file.

## Data.csv
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df.head()

df['Ord_1'].unique()

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df['Ord_1']=en.fit_transform(df[["Ord_1"]])
df.head()

df['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df['Ord_2']=en.fit_transform(df[["Ord_2"]])
df.head()

le = LabelEncoder()
df['City'] = le.fit_transform(df[["City"]])
df.head()

from category_encoders import BinaryEncoder
be= BinaryEncoder()
data= be.fit_transform(df['bin_1'])
df= pd.concat([df,data],axis=1)
df.head()

from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df['bin_2'])
df= pd.concat([df1,data1],axis=1)
df
```
## Encodingdata.csv
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

from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df = pd.concat([df,data],axis=1)
df

be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df = pd.concat([df,data],axis=1)
df
```

## BMI.csv
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

### Output
## Data.csv
* Initial Data:
  
 ![1](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/15798873-5764-4317-882c-427cb3930e36)
* Unique Data:

  ![2](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/ce02965e-80c4-41f3-8eb5-bd9848423b79)
* Original Encoder:

![3](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/ce13306a-f489-42bc-8744-38a7a8607257)
![4](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/2fbd98c2-bd25-47cc-8a08-09422a5d8a3c)
* Label Encoder:

![5](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/1a1cf3b4-56f4-4aad-999b-e9ef2f6ee589)
* Binary Encoder:

![6](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/7a5732ab-58f1-43ac-91cb-337f8a78854b) ![7](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/a8cc36ca-97fa-4501-8f9a-5ebe88bed824)

## EncoderData.csv:

* Initial Data:

![8](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/b3982042-2a73-43c6-9903-1805e73e531d)
* Unique Data:
  
![9](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/18b50668-2dba-4e70-95e4-1e24f2e2440c)
* Original Encoder:

![10](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/cf27464f-0783-49ee-a4e5-3642354e0ac4)  
* Label Encoder:

 ![11](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/2c4bc53f-062b-401c-9a4b-c6a3b5651f5b)
* Binary Encoder:
  
 ![12](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/0e94d9c3-bbf8-43bf-baa5-e78697c6a61e)
![13](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/937a769a-28d9-4ae8-b9e0-f385178643f3)

## BMI.csv:
*Initial Data:

![14](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/d07a81da-dc2e-471d-b70d-9795708a46f1)
* Binary Encoder:

 ![15](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/f3a48547-fa2f-4e70-8e25-2aa973e1cf07)
* Dummies:
  
![16](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-05/assets/119393540/a24303cd-4e9b-4979-a9c6-ef0f2b693161)

## Result:
Thus the Feature Generation and Feature Scaling process is applied to the given data set.
