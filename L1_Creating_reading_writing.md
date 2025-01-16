## 1. Core objects: **DataFrame**, **Series**

### 1.1 DataFrame (`pd.DataFrame`)
- a table

```python
pd.DataFrame({Row1: [Column1], Row2:[Column2], ... , 
                  index=[row labal1, row label2]}) 
```
  
- e,g,
```python
pd.DataFrame({'Yes': [50, 21], 'No': [131, 2]})
```
  |Yes |No
0 |50  |131
1 |21  |2

"0, No" => 131

### 1.2 Series (`pd.Series`)
- a sequence of data values
  - a single column of Dataframe
  
```python
pd.Series([column], index=[row label], name='')
```

- e.g.
```python
pd.Series([30,35,40], index=['2015', '2016', '2017'], name= 'A')
```

## 2. Reading data files (CSV, Comma-Separated Values)
### use `pd.read_csv("path", index_col=num)` to read data into DataFrame

- e.g.
```python
wine_review = pd.read_csv("...")
```
### use `shape` for size: rows * columns
- e.g.
```python
wine_review.shape #(129971, 14)
```

### use `.head() for the first five rows`
- e.g.
```python
wine_review.head()
```

- specifing an index
``` python
wine_review = pd.read_csv("...", index_col=0)
wine_review.head()
```

### use `.to_csv('file_name.csv')` for saving
- e.g.
```python
animals = pd.DataFrame({'Cows': [12, 20], 'Goats': [22, 19]}, index=['Year 1', 'Year 2'])

animals.to_csv("cows_goats.csv")
```
