## Creating, reading and writing 

#### DataFrame and Series
```pd.DataFrame({Row1: [Column1],..., index=[labels]})```
```pd.Series([Columns], index=[Row labels], name= '')```

#### Reading data files
```pd.read_csv("path", index_col=num)```
```.shape``` : size (rows*columns)
```.head()```: first 5 rows
```.to_csv("filename.csv")```

***
## Indexing, selecting and assigning

#### Indexing
**`object.property`**
**`object[propperty]`: Better choice**


**`.iloc[row, column]`: index location**
- `var.iloc[0]` : First **row** of the data
- `var.iloc[:, 0]`: First **column** of the data
- `var.iloc[:3, 0]`: 3 rows from the beginning, first column
- `var.iloc[[0, 1, 2], 0]`: same as above
- `var.iloc[-5:]`: **Last** 5 rows 

**`.loc[row, column]`: label location**
- `var.loc[0, 'label']`: First entry of label
- `var.loc[:, 'label1, label2']`: All rows and the corresponding columns

**`.set_index("")`: add a row**

####  Selecting
**`.property`**
- `var.loc[object.property == 'Target property']`: The relevent data of the target property
  - `[(a)&(b)]`: a and b both True
  - `[(a)|(b)]`: a or b

**` .isin()`**
- `var.loc[object.property.isin([values])]`

**`.notnull()`**
- `var.loc[object.property.notnull()]`: show the datas that are not null

#### Assigning 
`object[index] = 'value'`
`object[index] = range(len(object), 0, -1)`: reverse index number