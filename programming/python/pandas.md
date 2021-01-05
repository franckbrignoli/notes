# Pandas/Numpy

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

### Random

```python
np.random.randint(2, size=100) # generate 100 numbers between 0 inclusive and 2 exclusive
np.random.choice([0, 1], size=10000, p=[0.8, 0.2]) # generate 1000 numbers between 0 and 1 with a biased probability
```

