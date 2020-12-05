# Pandas

### Description

```python
df.info() # types and non null values
df.nunique() # count distinct values
df.describe() # describtive stats for each columns

df.duplicated() # sum(df.duplicated())
```

### Selection

`.loc` uses labels

```python
df.loc[:,'id':'fractal_dimension_mean'] 
```

while `.iloc` uses indices

```python
df.iloc[:,:12]
df.iloc[:, np.r_[1:2, 12:]] # np.r_ to use multiple intervals
```

Filters

```text
df[df[]
```

Bins

```text
df['acidity_levels'] = pd.cut(df['pH'], bin_edges, labels=bin_names)
```

### Cleaning

```python
df.fillna()
df.drop_duplicates()
df['timestamp'] = pd.to_datetime(something)
```



