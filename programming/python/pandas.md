# Pandas

### Description

```python
df.info() # types and non null values
df.nunique() # count distinct values
df.describe() # describtive stats for each columns

df.duplicated() # sum(df.duplicated())

df.shape

df['A'].value_counts()
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

```python
df[df[]
```

Bins

```python
df['acidity_levels'] = pd.cut(df['pH'], bin_edges, labels=bin_names)
```

Queries

```text
df.query('name in ["Franck", "Carole"]')
```

### Cleaning

```python
df.fillna()
df.drop_duplicates()
df['timestamp'] = pd.to_datetime(something)

df['cyl'].str.extract('(\d+)').astype(int)
```

### Structure

```python
df.rename(columns={"A": "a", "B": "c"})
df.rename(columns=lambda x: x)

df.drop(["A", "B"], axis=1)
```

### Plotting

```text
plt.bar([1, 2, 3], [224, 620, 425], tick_label=['a', 'b', 'c'])
plt.title('Some Title')
plt.xlabel('Some X Label')
plt.ylabel('Some Y Label');
```

