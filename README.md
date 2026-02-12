# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
print(df)
```
<img width="1075" height="823" alt="Screenshot 2025-10-03 135621" src="https://github.com/user-attachments/assets/47d13b07-7d8b-4598-a27a-2aa985d6b0fb" />

```py
df.isnull()
```
<img width="971" height="583" alt="Screenshot 2025-10-03 135946" src="https://github.com/user-attachments/assets/3c827297-ad32-4de2-b17f-8990c51ec0c7" />

```py
df.isnull().sum()
```
<img width="637" height="234" alt="Screenshot 2025-10-03 140103" src="https://github.com/user-attachments/assets/d2b82721-4ca2-4a58-81c3-1b1e5aefd56c" />

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
drop=df.dropna(axis=1)
print("before dropna \n\n",df)
print("after dropna \n\n",drop)
```
<img width="883" height="876" alt="Screenshot 2025-10-03 140619" src="https://github.com/user-attachments/assets/767a436a-3cf6-4b7a-bda3-6720e62d9f45" />

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
drop=df.dropna(axis=1,inplace=True)
print("before dropna",df)
print("after dropna",drop)
```
<img width="764" height="247" alt="Screenshot 2025-10-03 140919" src="https://github.com/user-attachments/assets/2bb0af3d-4702-44bc-946d-7a742c44064d" />

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df.fillna(method='ffill')
print(df)
```
<img width="884" height="646" alt="Screenshot 2025-10-03 141009" src="https://github.com/user-attachments/assets/753212db-6f53-48a6-b48a-dbdfbb0728e2" />

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
loc=df.iloc[1:21:3]
print(loc)
```
![Screenshot_3-10-2025_14138_localhost](https://github.com/user-attachments/assets/bcb20f75-d0ae-4fd1-a1e8-d81015b1b092)

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df=df.fillna(df.median(numeric_only=True))
print(df)
```
![Screenshot_3-10-2025_141726_localhost](https://github.com/user-attachments/assets/fd526bcb-bcb0-408a-b726-0ee99c721c2e)

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df.fillna(method='bfill')
print(df)
```
![Screenshot_3-10-2025_141726_localhost](https://github.com/user-attachments/assets/557756c5-17a1-4825-a459-129bdefc5a88)

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df=df.mode()
print(df)
```
![Screenshot_3-10-2025_141726_localhost](https://github.com/user-attachments/assets/b6f4b21a-e2ae-4450-a246-1582326ce678)

```py
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df=df.drop_duplicates()
print(df)
```
![Screenshot_3-10-2025_14213_localhost](https://github.com/user-attachments/assets/2de1df0d-d5cb-4d97-9c83-e24f0fb453a4)

```py
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
df.info()
```
![Screenshot_3-10-2025_142514_localhost](https://github.com/user-attachments/assets/3997c4c1-594e-45a9-a3a2-994f9889f333)

```py
import matplotlib.pyplot as plt
import pandas as pd 
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
plt.bar(df['country'],df['rating'],color='black')
plt.show()
```
<img width="655" height="496" alt="Screenshot 2026-02-12 104952" src="https://github.com/user-attachments/assets/107eb085-7e2e-4160-8fcc-839f62b62d85" />

```py
import matplotlib.pyplot as plt
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
plt.barh(df['country'],df['rating'],color='grey')
plt.show()
```
<img width="753" height="505" alt="image" src="https://github.com/user-attachments/assets/a08b436c-26b0-4f53-bea3-a8a78500e7e2" />

```py
import matplotlib.pyplot as plt
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
plt.plot(df['country'],df['rating'],color='black')
plt.show()
```
<img width="774" height="504" alt="image" src="https://github.com/user-attachments/assets/e6d94ada-3b9c-40de-8087-8336c2bda7e5" />

```py
import matplotlib.pyplot as plt
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
plt.scatter(df['country'],df['rating'],color='black')
plt.show()
```
<img width="725" height="492" alt="image" src="https://github.com/user-attachments/assets/d4b78058-4838-4f17-bdbb-0096c70250d9" />

# Result
Thus the given data has been read, cleaned and the data has been saved to a file.

