# learn-pandas

This content is totally public and free for everybody who wants to learn Pandas with python.

the original content can be found in utube and special thanks to "Corey Schafer" for the great videos.

# Samples

```python
# first Row -  default index
df.iloc[0]
df.loc[0] # because 0 is the index of the first row so the label as well
# loc -> searching by labels
```

```python
# read csv
import pandas as pd
df = pd.read_csv('data.csv')
```

```python
# write csv
df.to_csv('output.csv')
```

```python
# set columns
df_new.columns = ['column 1','column 2', 'column 3']
```

```python
# drop columns
df = df.drop(['column 2', 'column 3'], axis=1)
```


```python
# set index (label)
df.set_index('column 1', inplace=True)
```

```python
# join 2 dataframes
df = df_new.join(df_old)
```

```python
# get unique / distinct values from a column
df['column 1'].unique()
```

```python
# convert column type to float
df['column 2'] = df['column 2'].astype(float)
```


```python
# calculate new column according to other columns - if/else
# .where(condition, if true, if false)
import numpy as np
df['column - calculated'] = np.where(df['column 1'] == df['column 2'], 
                                     df['column 2'] - df['column 3'], 
                                    np.nan)
```

```python
# find a record according to unique id (index)
#unique value must bu inside the index
df.loc['unique value']
```