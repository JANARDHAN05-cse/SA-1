# SKILL ASSESSMENT - 1
```
NAME : P JANARDHAN
REGISTER NUMBER : 212224040128
```
# CODING AND OUTPUT
```
# creating a dataFrame
import pandas as pd
df = pd.DataFrame(
    [[10,20,30],
     [40,50,60],
     [70,80,90]],
    index=[1,2,3],
    columns = ['i','ii','iii']
)
print(df)
```
![image](https://github.com/user-attachments/assets/470cde00-c2a0-4323-848a-627d0975b021)
```
#creating dataframe from dictionary
mydataset = {
  'Team': ["CSK", "RCB", "MI"],
  'Trophies': [5, 0, 5]
}
myvar = pd.DataFrame(mydataset)
print(myvar)
```
![image](https://github.com/user-attachments/assets/7099fbd0-3e4a-47b3-9427-41ebcf301e7d)
```
# Column addition
data = {'Bikes': ['KTM', 'R15', 'NS200'],  'Weight': [159,142,158], 'Ranking': [3,2,1]} 
df = pd.DataFrame(data) 
Made_in = ['Austria','India','India'] 
df['Made by'] = Made_in 
print(df) 
```
![image](https://github.com/user-attachments/assets/46781107-ff38-4b25-81ac-43c099f90de2)

```
# deleting column
data = {
    'Bikes': ['KTM', 'R15', 'NS200'],  
    'Weight': [159,142,158], 
    'Ranking': [3,2,1],
    'Made by' : ['Austria','India','India']
    }

df = pd.DataFrame(data)
del df['Made by']
print(df)
```
![image](https://github.com/user-attachments/assets/f2d81404-2afe-48a1-8464-37d57745e0cc)

```
# column renaming
import pandas as pd

data = {
    'Bikes': ['KTM', 'R15', 'NS200'],  
    'Weight': [159,142,158], 
    'Ranking': [3,2,1],
    'Made by' : ['Austria','India','India']
    }

df = pd.DataFrame(data)
print(df)
print()

df.rename(columns={'Made by': 'Made in'}, inplace=True)
print(df)
```
![image](https://github.com/user-attachments/assets/128af78a-6deb-4c5a-b60f-beb8757442e8)
```
data = {
    'Bikes': ['KTM', 'R15', 'NS200'],  
    'Weight': [159,142,158], 
    'Ranking': [3,2,1],
    'Made by' : ['Austria','India','India']
    }
df = pd.DataFrame(data)
print(df)
print()
df.columns = ['A', 'B', 'C', 'D']
print(df)
```
![image](https://github.com/user-attachments/assets/00586fbc-dfd0-4c28-80f6-14b04791cc12)
```
# Indexing and Selecting data

data = {
    'Bikes': ['KTM', 'R15', 'NS200'],  
    'Weight': [159,142,158], 
    'Ranking': [3,2,1],
    'Made by' : ['Austria','India','India']
    }
df = pd.DataFrame(data)
df = df['Bikes']
df
```
![image](https://github.com/user-attachments/assets/19d99a51-6b72-4b15-baad-7fe397ae3df5)
```
# Multiple column selection
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [25, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kannauj'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd']
}

df = pd.DataFrame(data)

print(df[['Name', 'Emp_id','Qualification']])
```
![image](https://github.com/user-attachments/assets/5d208a59-347f-48ed-8c59-505a6d245e95)
```
# Finding nlargest
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [25, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kannauj'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd'],
    'salary': [60000, 70000, 80000, 90000]
}
df = pd.DataFrame(data)

top_salaries = df.nlargest(2, columns='salary')
print(top_salaries)
```
![image](https://github.com/user-attachments/assets/583eec7a-9a8d-4e0f-97d8-d696fd83d437)
```
# Handling missing values using Dropna
import pandas as pd

data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun','Joyboy'],
    'Emp_id' : [1001,1002,1003,1004,None],
    'Age': [25, 24, 22, 23,19],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kannauj','Japan'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd',None],
    'salary': [60000, 70000, 80000, 90000,400000000]
}

df = pd.DataFrame(data)
df.dropna(inplace=True)
print(df)
```
![image](https://github.com/user-attachments/assets/b5ed43e2-e1e2-4843-982a-b8044730cf80)
```
# Filling missing values
import pandas as pd

data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun','Joyboy'],
    'Emp_id' : [1001,1002,1003,1004,None],
    'Age': [25, 24, 22, 23,19],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kannauj','Japan'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd',None],
    'salary': [60000, 70000, 80000, 90000,40000]
}

df = pd.DataFrame(data)
df_filled = df.fillna(0)

print(df_filled)
```
![image](https://github.com/user-attachments/assets/17e8ef1b-3a60-4473-818c-04774efcfc10)
```
# Sorting the dataframe with actual value
import pandas as pd
df = pd.DataFrame({'column1':[10,50,20,30,60,40],'column2':[11,77,33,55,66,44],
			'column3':['a','e','h','b','g','l']})
df.sort_values(by='column3')
print(df)
```
![image](https://github.com/user-attachments/assets/49e14abb-2279-4442-b5d1-3059c7f806ed)

```
#Sorting the dataframe with label
df = pd.DataFrame(np.random.randn(10,2),
		index=[1,4,6,2,3,5,9,8,0,7],columns = ['col2','col1'])
df
df1=df.sort_index(ascending=True)
print("Dataframe 1")
print(df1)
print("Dataframe 2")
df2=df.sort_index()
df2
```
![image](https://github.com/user-attachments/assets/a37f205c-8e5e-4ca9-9aeb-a423db0e50c9)

```
# Groupby commands
import pandas as pd
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [22, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kanpur'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd'],
    'salary': [60000, 70000, 80000, 90000]
}
df = pd.DataFrame(data)
print(df,"\n")
print(df.groupby('Age')['salary'].mean(),"\n")
print(df.groupby('Age')['salary'].min())  
```
![image](https://github.com/user-attachments/assets/408cde64-c616-4c89-90d5-df65dab21c5b)
```
df = pd.DataFrame({'c1':[10,20,30,40,50,60],'c2':[100,200,300,400,500,600],'c3':['a','b','c','d','e','f']})
df.head()
```

![image](https://github.com/user-attachments/assets/954e46ea-c49c-47e5-a889-b9831699b4f0)

```
df.describe()
```
![image](https://github.com/user-attachments/assets/24422ee5-d4e6-4dc7-93ca-73ab4bffb31c)
```
# Checking for missing values
df = pd.DataFrame({'A':[1,2,np.nan],
                  'B':[5,np.nan,np.nan],
                  'C':[1,2,3]})
df
```
![image](https://github.com/user-attachments/assets/45ec37a1-3221-4575-bb34-c5d7e61e8547)
```
df.isnull()
```
![image](https://github.com/user-attachments/assets/ded0680a-500b-4360-987a-5e56e5d44c9c)
```
df.notnull()
```
![image](https://github.com/user-attachments/assets/eff434e4-312d-4443-b08a-645f3c003484)
```
df.dropna()
```
![image](https://github.com/user-attachments/assets/64cc9184-9960-419f-b896-e4ae58b25447)
```
df.dropna(axis=1)
```
![image](https://github.com/user-attachments/assets/d9b8bff0-44f2-41bb-9d4e-f71515d792cb)
```
#Replace NaN with a Scalar Value
df.fillna(value=10)
df['A'].fillna(value=df['A'].mean())
df
```
![image](https://github.com/user-attachments/assets/90d6b32a-35b6-4c04-a17d-6eb5db29f059)
```
df.fillna(method='ffill')
```
![image](https://github.com/user-attachments/assets/6524dfdf-0364-4f3b-9d75-8e359ada3884)
```
# Forward and backward filling
df = pd.DataFrame({'A':[1,np.nan,2],
                  'B':[5,np.nan,3],
                  'C':[1,2,3]})
df
```

![image](https://github.com/user-attachments/assets/d5d0cfcb-a17c-4c48-ba6f-31c2534f35f4)
```
# using backward filling
df.fillna(method='ffill')
```
![image](https://github.com/user-attachments/assets/eb824c72-b246-41e0-a879-fdbbd93e1d61)
```
# using forward filling
df.fillna(method='bfill')
```
![image](https://github.com/user-attachments/assets/4108273a-8352-45fc-8ad6-3b2ef6da840d)

```
# DataFrame Commands
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [22, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kanpur'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd'],
    'salary': [60000, 70000, 80000, 90000]
}
df = pd.DataFrame(data)
print("Head Values")
print(df.head(2))
print()
print("Tail Values")
print(df.tail(3))
```
![image](https://github.com/user-attachments/assets/00ea8812-759c-4b6d-b4a5-3d3664e61123)

```
# DataFrame Commands
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [22, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kanpur'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd'],
    'salary': [60000, 70000, 80000, 90000]
}
df = pd.DataFrame(data)
# It will be used to checks for non-duplicated values
~df.duplicated()
```
![image](https://github.com/user-attachments/assets/0e57dedd-fc96-4327-96ca-64a214719893)
```
# filtering in a dataframe
data = {
    'Name': ['Ram', 'Ravi', 'Krish', 'Arjun'],
    'Emp_id' : [1001,1002,1003,1004],
    'Age': [22, 24, 22, 23],
    'Address': ['Tamil Nade', 'Kanpur', 'Kerala', 'Kanpur'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd'],
    'salary': [60000, 70000, 80000, 90000]
}

df = pd.DataFrame(data)
filter = df[(df['Age'] == 22) & (df['salary'] >= 70000 )]
print(filter)
```
![image](https://github.com/user-attachments/assets/b876b787-2947-4e45-94c2-41d001b33559)

