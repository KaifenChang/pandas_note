# Native accessors
1. `object.property`
2. `object[propperty]`: Better choice 

***
# Indexing in pandas
## 1. Index-based selection (`.iloc[row, column]`: index location)

`var.iloc[0]` : First **row** of the data
`var.iloc[:, 0]`: First **column** of the data
`var.iloc[:3, 0]`: 3 rows from the beginning, first column
`var.iloc[[0, 1, 2], 0]`: same as above
`var.iloc[-5:]`: **Last** 5 rows 

## 2. Label-based seletion (`.loc[row, column]`: label location)

`var.loc[0, 'label']`: First entry of label
`var.loc[:, ['label1, label2']]`: All rows and the corresponding columns

***
# Manipulating the index
## `.set_index("")`
add a row

*** 
# Conditional selection

1. `var.loc[object.property == 'Target property']`: The relevent data of the target property
- `[(a)&(b)]`: a and b both True
- `[(a)|(b)]`: a or b

2. ` .isin()`
- `var.loc[object.property.isin([values])]`

3. `.notnull()`
- `var.loc[object.property.notnull()]`: show the datas that are not null

***
# Assigning data
1. constant value
`object[index] = 'value'`

2. iterable values
`object[index] = range(len(object), 0, -1)`: reverse index number