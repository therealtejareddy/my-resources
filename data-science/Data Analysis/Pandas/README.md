# PANDAS
### installation
`pip install pandas`

### Import
`import pandas as pd`

### Series
##### Series
`pd_series = pd.series([1,2,3,4])`
##### Series with index
```python
pd_series_idx = pd.Series(data=[1,2,3,4],index=['banana','apple','mango','lemon'])
idx_pd_series_idx = pd_series_idx.index
val_pd_series_idx = pd_series_idx.values
```

##### Update Series values
`pd_series_idx['banana']=20`

##### Drop Series values
`pd_series_idx.drop('apple',inplace=True)`

### DataFrame
##### Create DataFrame
```python
people = {
    "first":["Teja","Teja1", np.nan,"Cool",np.nan],
    "last":["Reddy","Reddy1","Hello","Chill","dude"],
    "email":["yuvatejareddy@gmail.com","teja1@gmail.com",np.nan,np.nan,"chill@chill.com"],
    "age":['10','21','45',None,None]
}
df = pd.DataFrame(people)
```

##### DataFrame Shape
`df.shape`

##### DataFrame Information
`df.info()`

##### DataFrame Column Information
`df.columns`

### Selecting Rows and Columns
##### Select Single Column
`col = df["Column Name"]` or `col = df.column_name`

##### Select Multiple Columns
`new_df = df[["first","last"]]`