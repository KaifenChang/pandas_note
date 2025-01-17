# Summary functions

`.describe()`: generate some common summary
`.mean()`
`.unique()`
`.value_counts()`

# Maps
**`.map(func)`**: map a new value to the original value
e.g.
```python
review_points_mean = reviews.points.mean()
reviews.points.map(lambda p: p - review_points_mean)
```
transform to a **Series**

**`.apply(func,)`**
e.g.
```python
def remean_points(row):
    row.points = row.points - review_points_mean
    return row

reviews.apply(remean_points, axis='columns')
```



