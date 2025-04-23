# Pandas-and-Numpy-Commands

# AIM
To read the given data and perform data analysis using Numpy and Pandas.

# Algorithm
STEP 1: Read the given Data.

STEP 2: Get the information about the data.

STEP 3: Remove and Fill the null values from the data.

STEP 4: Save the Clean data to the respective files.

# Coding and Output
```
import pandas as pd
data = {
    'name': ['John', 'Sarah', 'Mike', 'Emily', 'David'],
    'age': [25, 31, 29, 35, 27],
    'gender': ['M', 'F', 'M', 'F', 'M'],
    'salary': [50000, 70000, 60000, 80000, 55000]
}
df = pd.DataFrame(data)
print(df.head(3))
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144629.png>)

```
import pandas as pd
data = {
    'name': ['John', 'Sarah', 'Mike', 'Emily', 'David'],
    'age': [25, 31, 29, 35, 27],
    'gender': ['M', 'F', 'M', 'F', 'M'],
    'salary': [50000, 70000, 60000, 80000, 55000]
}
df = pd.DataFrame(data)
print(df.tail(3))
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144633.png>)
```
import pandas as pd
data = {
    'name': ['John', 'Sarah', 'Mike', 'Emily', 'David'],
    'age': [25, 31, 29, 35, 27],
    'gender': ['M', 'F', 'M', 'F', 'M'],
    'salary': [50000, 70000, 60000, 80000, 55000]
}
df = pd.DataFrame(data)
df.info()
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144638.png>)
```
import pandas as pd
data = {
    'name': ['John', 'Sarah', 'Mike', 'Emily', 'David'],
    'age': [25, 31, 29, 35, 27],
    'gender': ['M', 'F', 'M', 'F', 'M'],
    'salary': [50000, 70000, 60000, 80000, 55000]
}
df = pd.DataFrame(data)
print(df.describe())
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144646.png>)
```
import pandas as pd
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
    'age': [25, 30, 35, 40],
    'score': [90, 80, 85, 95]
}
df = pd.DataFrame(data)
print(df.sort_values(by='age', ascending = False))
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144650.png>)
```
import pandas as pd
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Emily', 'Frank'],
    'gender': ['F', 'M', 'M', 'M', 'F', 'M'],
    'age': [25, 35, 40, 28, 30, 45],
    'salary': [50000, 70000, 60000, 80000, 65000, 90000]
}
df = pd.DataFrame(data)
print(df.groupby('gender')['salary'].mean())
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144654.png>)
```
import pandas as pd
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Emily', 'Frank'],
    'gender': ['F', 'M', 'M', 'M', 'F', 'M'],
    'age': [25, 35, 40, 28, 30, 45],
    'salary': [50000, 70000, 60000, 80000, 65000, 90000]
}
df = pd.DataFrame(data)
print(df.groupby('gender').count())
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144708.png>)
```
import pandas as pd
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, 32, None, 41, 28],
    'Salary': [50000, None, 70000, 90000, 60000]}
df = pd.DataFrame(data)
df
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144714.png>)
```
df_cleaned = df.dropna(subset=['Salary'])
print(df_cleaned)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144720.png>)
```
df_cleaned_all = df.dropna(how='all')
print(df_cleaned_all)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144723.png>)
```
df_cleaned_any = df.dropna(how='any')
print(df_cleaned_any)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144728.png>)
```
import pandas as pd
import numpy as np
# Create a sample DataFrame with missing values
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve', 'Bob', 'Charlie'],
    'Age': [25, np.nan, 35, 41, np.nan, np.nan, 85],
    'Salary': [50000, np.nan, 70000, np.nan, 60000, np.nan, 70000]
}
df = pd.DataFrame(data)
~df.duplicated()
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144732.png>)
```
import pandas as pd
import numpy as np
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}
df = pd.DataFrame(data)
df_filled = df.fillna(0)
print(df_filled)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144737.png>)
```
import pandas as pd
import numpy as np
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}
df = pd.DataFrame(data)
df_ffilled = df.fillna(method='ffill')
print(df_ffilled)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144749.png>)
```
import pandas as pd
import numpy as np
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}
df = pd.DataFrame(data)
df_bfilled = df.fillna(method='bfill')
print(df_bfilled)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144758.png>)
```
import pandas as pd
import numpy as np
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}
df = pd.DataFrame(data)
df_mean = df.fillna(df.mean(numeric_only=True))
print(df_mean)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144802.png>)
```
import pandas as pd
import numpy as np
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}
df = pd.DataFrame(data)
~df.duplicated()
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144807.png>)
```
import pandas as pd
import numpy as np
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
    'age': [25, 32, 18, 47],
    'gender': ['F', 'M', 'M', 'M'],
    'height': [1.62, 1.78, 1.65, 1.83]
}
df = pd.DataFrame(data)
df_filtered = df[(df['gender'] == 'M') & (df['height'] > 1.7)]
print(df_filtered)
```
![alt text](<Output Screenshots/Screenshot 2025-04-23 144811.png>)
# Result
Data analysis was successfully performed using Python libraries like NumPy, Pandas and the results were verified.
