```python
import pandas as pd

```


```python
df1=pd.read_excel('./Downloads/Data05.xlsx', skiprows=1)
```


```python
df2=df1.iloc[:, 8:-2]
```


```python
df1.iloc[:, 8:-2].T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>8</th>
      <th>9</th>
      <th>...</th>
      <th>83</th>
      <th>84</th>
      <th>85</th>
      <th>86</th>
      <th>87</th>
      <th>88</th>
      <th>89</th>
      <th>90</th>
      <th>91</th>
      <th>92</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>판매</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>10354.1</td>
      <td>3543.3</td>
      <td>234603.9</td>
      <td>3339.9</td>
      <td>2616.8</td>
      <td>16520.3</td>
      <td>11722.5</td>
      <td>100526.4</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-28.7</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>181331.6</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>9474.3</td>
      <td>7702.6</td>
      <td>56309.6</td>
      <td>3181.8</td>
      <td>24351.4</td>
      <td>26129.3</td>
      <td>26550.6</td>
      <td>17334.1</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>40207.8</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>9741.7</td>
      <td>6117.1</td>
      <td>78268.0</td>
      <td>7674.0</td>
      <td>19767.5</td>
      <td>35423.7</td>
      <td>4279.6</td>
      <td>32889.1</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>6965.7</td>
      <td>4009.9</td>
      <td>74942.2</td>
      <td>3710.2</td>
      <td>18616.7</td>
      <td>26476.3</td>
      <td>15773.6</td>
      <td>16821.8</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>3368.2</td>
      <td>2669.8</td>
      <td>84690.1</td>
      <td>8294.9</td>
      <td>17021.1</td>
      <td>60737.0</td>
      <td>8400.1</td>
      <td>29712.9</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>43576.6</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00.1</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>243.8</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00.1</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00.1</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00.1</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00.2</th>
      <td>98.8</td>
      <td>393.7</td>
      <td>6.4</td>
      <td>7.7</td>
      <td>293.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>112.5</td>
      <td>36.1</td>
      <td>298.1</td>
      <td>...</td>
      <td>14.7</td>
      <td>1.6</td>
      <td>47.1</td>
      <td>7.8</td>
      <td>64.3</td>
      <td>963.4</td>
      <td>3.0</td>
      <td>6.5</td>
      <td>609.5</td>
      <td>1249.7</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00.2</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>10.2</td>
      <td>0.0</td>
      <td>6.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>27.9</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00.2</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>6.4</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>179.1</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>216.9</td>
      <td>0.0</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00.2</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>10.2</td>
      <td>277.2</td>
      <td>0.0</td>
      <td>117.7</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>37.3</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>425.6</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00.3</th>
      <td>98.8</td>
      <td>393.7</td>
      <td>9480.7</td>
      <td>7710.3</td>
      <td>56602.6</td>
      <td>3181.8</td>
      <td>24351.4</td>
      <td>26241.8</td>
      <td>26586.7</td>
      <td>17632.2</td>
      <td>...</td>
      <td>14.7</td>
      <td>1.6</td>
      <td>47.1</td>
      <td>7.8</td>
      <td>64.3</td>
      <td>963.4</td>
      <td>3.0</td>
      <td>6.5</td>
      <td>853.4</td>
      <td>41457.5</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00.3</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>9741.7</td>
      <td>6127.3</td>
      <td>78268.0</td>
      <td>7680.0</td>
      <td>19767.5</td>
      <td>35423.7</td>
      <td>4279.6</td>
      <td>32917.1</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00.3</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>6972.0</td>
      <td>4009.9</td>
      <td>74942.2</td>
      <td>3889.3</td>
      <td>18616.7</td>
      <td>26476.3</td>
      <td>15990.5</td>
      <td>16821.8</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00.3</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>3368.2</td>
      <td>2680.1</td>
      <td>84967.2</td>
      <td>8294.9</td>
      <td>17138.9</td>
      <td>60737.0</td>
      <td>8400.1</td>
      <td>29750.2</td>
      <td>...</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>44002.2</td>
    </tr>
  </tbody>
</table>
<p>17 rows × 93 columns</p>
</div>




```python
df2.stack()
```




    0   판매                            0.0
        2019-12-01 00:00:00           0.0
        2020-10-01 00:00:00           0.0
        2020-11-01 00:00:00           0.0
        2020-12-01 00:00:00           0.0
                                   ...   
    92  2020-12-01 00:00:00.2       425.6
        2019-12-01 00:00:00.3     41457.5
        2020-10-01 00:00:00.3    107175.6
        2020-11-01 00:00:00.3    110209.3
        2020-12-01 00:00:00.3     44002.2
    Length: 1581, dtype: float64




```python
pd.DataFrame(df2.stack())
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="5" valign="top">0</th>
      <th>판매</th>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00</th>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00</th>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00</th>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00</th>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="5" valign="top">92</th>
      <th>2020-12-01 00:00:00.2</th>
      <td>425.6</td>
    </tr>
    <tr>
      <th>2019-12-01 00:00:00.3</th>
      <td>41457.5</td>
    </tr>
    <tr>
      <th>2020-10-01 00:00:00.3</th>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>2020-11-01 00:00:00.3</th>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>2020-12-01 00:00:00.3</th>
      <td>44002.2</td>
    </tr>
  </tbody>
</table>
<p>1581 rows × 1 columns</p>
</div>




```python
pd.DataFrame(df2.stack()).reset_index()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>level_0</th>
      <th>level_1</th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>판매</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>2019-12-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>2020-10-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>2020-11-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>2020-12-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1576</th>
      <td>92</td>
      <td>2020-12-01 00:00:00.2</td>
      <td>425.6</td>
    </tr>
    <tr>
      <th>1577</th>
      <td>92</td>
      <td>2019-12-01 00:00:00.3</td>
      <td>41457.5</td>
    </tr>
    <tr>
      <th>1578</th>
      <td>92</td>
      <td>2020-10-01 00:00:00.3</td>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>1579</th>
      <td>92</td>
      <td>2020-11-01 00:00:00.3</td>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>1580</th>
      <td>92</td>
      <td>2020-12-01 00:00:00.3</td>
      <td>44002.2</td>
    </tr>
  </tbody>
</table>
<p>1581 rows × 3 columns</p>
</div>




```python
pd.DataFrame(df2.stack()).reset_index().iloc[1:]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>level_0</th>
      <th>level_1</th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>2019-12-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>2020-10-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>2020-11-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>2020-12-01 00:00:00</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>2019-12-01 00:00:00.1</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1576</th>
      <td>92</td>
      <td>2020-12-01 00:00:00.2</td>
      <td>425.6</td>
    </tr>
    <tr>
      <th>1577</th>
      <td>92</td>
      <td>2019-12-01 00:00:00.3</td>
      <td>41457.5</td>
    </tr>
    <tr>
      <th>1578</th>
      <td>92</td>
      <td>2020-10-01 00:00:00.3</td>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>1579</th>
      <td>92</td>
      <td>2020-11-01 00:00:00.3</td>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>1580</th>
      <td>92</td>
      <td>2020-12-01 00:00:00.3</td>
      <td>44002.2</td>
    </tr>
  </tbody>
</table>
<p>1580 rows × 3 columns</p>
</div>




```python
df3=df1.iloc[:, 6:-2].drop(columns=['Unnamed: 7', '판매'])
```


```python
df4=pd.DataFrame(df3.set_index(['제품명']).stack()).reset_index()
```

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_895/3723966535.py:1: FutureWarning: Inferring datetime64[ns] from data containing strings is deprecated and will be removed in a future version. To retain the old behavior explicitly pass Series(data, dtype={value.dtype})
      df4=pd.DataFrame(df3.set_index(['제품명']).stack()).reset_index()



```python
df4.rename(columns={'level_1':'날짜', 0:'재고량'})  #rename(columns={})
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>제품명</th>
      <th>날짜</th>
      <th>재고량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>2019-12-01 00:00:00.000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>2020-10-01 00:00:00.000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>2020-11-01 00:00:00.000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>2020-12-01 00:00:00.000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>2019-12-01 00:00:00.100</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1483</th>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>2020-12-01 00:00:00.200</td>
      <td>425.6</td>
    </tr>
    <tr>
      <th>1484</th>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>2019-12-01 00:00:00.300</td>
      <td>41457.5</td>
    </tr>
    <tr>
      <th>1485</th>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>2020-10-01 00:00:00.300</td>
      <td>107175.6</td>
    </tr>
    <tr>
      <th>1486</th>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>2020-11-01 00:00:00.300</td>
      <td>110209.3</td>
    </tr>
    <tr>
      <th>1487</th>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>2020-12-01 00:00:00.300</td>
      <td>44002.2</td>
    </tr>
  </tbody>
</table>
<p>1488 rows × 3 columns</p>
</div>




```python
df1.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>구분</th>
      <th>0</th>
      <th>카테고리명</th>
      <th>자재그룹</th>
      <th>자재그룹명</th>
      <th>제품코드</th>
      <th>제품명</th>
      <th>Unnamed: 7</th>
      <th>판매</th>
      <th>2019-12-01 00:00:00</th>
      <th>...</th>
      <th>2019-12-01 00:00:00.2</th>
      <th>2020-10-01 00:00:00.2</th>
      <th>2020-11-01 00:00:00.2</th>
      <th>2020-12-01 00:00:00.2</th>
      <th>2019-12-01 00:00:00.3</th>
      <th>2020-10-01 00:00:00.3</th>
      <th>2020-11-01 00:00:00.3</th>
      <th>2020-12-01 00:00:00.3</th>
      <th>안전재고</th>
      <th>분류</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>구분</td>
      <td>501</td>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>천원</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>...</td>
      <td>98.8</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>98.8</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>E</td>
    </tr>
  </tbody>
</table>
<p>1 rows × 27 columns</p>
</div>




```python
df1.columns.tolist()
```




    ['구분',
     0,
     '카테고리명',
     '자재그룹',
     '자재그룹명',
     '제품코드',
     '제품명',
     'Unnamed: 7',
     '판매',
     datetime.datetime(2019, 12, 1, 0, 0),
     datetime.datetime(2020, 10, 1, 0, 0),
     datetime.datetime(2020, 11, 1, 0, 0),
     datetime.datetime(2020, 12, 1, 0, 0),
     '2019-12-01 00:00:00.1',
     '2020-10-01 00:00:00.1',
     '2020-11-01 00:00:00.1',
     '2020-12-01 00:00:00.1',
     '2019-12-01 00:00:00.2',
     '2020-10-01 00:00:00.2',
     '2020-11-01 00:00:00.2',
     '2020-12-01 00:00:00.2',
     '2019-12-01 00:00:00.3',
     '2020-10-01 00:00:00.3',
     '2020-11-01 00:00:00.3',
     '2020-12-01 00:00:00.3',
     '안전재고',
     ' 분류']




```python
df6=df1[['카테고리명','자재그룹','자재그룹명','제품코드', '제품명','안전재고',' 분류']]
```


```python
df7=pd.merge(df6,df4, how='right',on= '제품명')
df7.to_excel('join.xlsx')
```


```python
df7.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 1488 entries, 0 to 1487
    Data columns (total 9 columns):
     #   Column   Non-Null Count  Dtype         
    ---  ------   --------------  -----         
     0   카테고리명    1488 non-null   object        
     1   자재그룹     1488 non-null   int64         
     2   자재그룹명    1488 non-null   object        
     3   제품코드     1488 non-null   int64         
     4   제품명      1488 non-null   object        
     5   안전재고     1488 non-null   float64       
     6    분류      1488 non-null   object        
     7   level_1  1488 non-null   datetime64[ns]
     8   0        1488 non-null   float64       
    dtypes: datetime64[ns](1), float64(2), int64(2), object(4)
    memory usage: 116.2+ KB



```python
df8=df7.rename(columns={'level_1': 'ymd', 0:'판매량'})
```


```python
def dataf(x):
    result=str(x)
    return result[0:10]


df8['ymd'].apply(dataf)
```




    0       2019-12-01
    1       2020-10-01
    2       2020-11-01
    3       2020-12-01
    4       2019-12-01
               ...    
    1483    2020-12-01
    1484    2019-12-01
    1485    2020-10-01
    1486    2020-11-01
    1487    2020-12-01
    Name: ymd, Length: 1488, dtype: object




```python
pd.to_datetime(df9['ymd'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in get_loc(self, key, method, tolerance)
       3360             try:
    -> 3361                 return self._engine.get_loc(casted_key)
       3362             except KeyError as err:


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/_libs/index.pyx in pandas._libs.index.IndexEngine.get_loc()


    pandas/_libs/index_class_helper.pxi in pandas._libs.index.Int64Engine._check_type()


    pandas/_libs/index_class_helper.pxi in pandas._libs.index.Int64Engine._check_type()


    KeyError: 'ymd'

    
    The above exception was the direct cause of the following exception:


    KeyError                                  Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_895/3620749935.py in <module>
    ----> 1 pd.to_datetime(df9['ymd'])
    

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/series.py in __getitem__(self, key)
        940 
        941         elif key_is_scalar:
    --> 942             return self._get_value(key)
        943 
        944         if is_hashable(key):


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/series.py in _get_value(self, label, takeable)
       1049 
       1050         # Similar to Index.get_value, but we do not fall back to positional
    -> 1051         loc = self.index.get_loc(label)
       1052         return self.index._get_values_for_loc(self, loc, label)
       1053 


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in get_loc(self, key, method, tolerance)
       3361                 return self._engine.get_loc(casted_key)
       3362             except KeyError as err:
    -> 3363                 raise KeyError(key) from err
       3364 
       3365         if is_scalar(key) and isna(key) and not self.hasnans:


    KeyError: 'ymd'



```python
df8.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 1488 entries, 0 to 1487
    Data columns (total 9 columns):
     #   Column  Non-Null Count  Dtype         
    ---  ------  --------------  -----         
     0   카테고리명   1488 non-null   object        
     1   자재그룹    1488 non-null   int64         
     2   자재그룹명   1488 non-null   object        
     3   제품코드    1488 non-null   int64         
     4   제품명     1488 non-null   object        
     5   안전재고    1488 non-null   float64       
     6    분류     1488 non-null   object        
     7   ymd     1488 non-null   datetime64[ns]
     8   판매량     1488 non-null   float64       
    dtypes: datetime64[ns](1), float64(2), int64(2), object(4)
    memory usage: 148.5+ KB



```python
df8['yy']=df8['ymd'].dt.year
df8['mm']=df8['ymd'].dt.month
df8['요일']=df8['ymd'].dt.day_name()
```


```python
df8
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>카테고리명</th>
      <th>자재그룹</th>
      <th>자재그룹명</th>
      <th>제품코드</th>
      <th>제품명</th>
      <th>안전재고</th>
      <th>분류</th>
      <th>ymd</th>
      <th>판매량</th>
      <th>yy</th>
      <th>mm</th>
      <th>요일</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>0.0</td>
      <td>E</td>
      <td>2019-12-01 00:00:00.000</td>
      <td>0.0</td>
      <td>2019</td>
      <td>12</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>1</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>0.0</td>
      <td>E</td>
      <td>2020-10-01 00:00:00.000</td>
      <td>0.0</td>
      <td>2020</td>
      <td>10</td>
      <td>Thursday</td>
    </tr>
    <tr>
      <th>2</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>0.0</td>
      <td>E</td>
      <td>2020-11-01 00:00:00.000</td>
      <td>0.0</td>
      <td>2020</td>
      <td>11</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>3</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>0.0</td>
      <td>E</td>
      <td>2020-12-01 00:00:00.000</td>
      <td>0.0</td>
      <td>2020</td>
      <td>12</td>
      <td>Tuesday</td>
    </tr>
    <tr>
      <th>4</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6068068</td>
      <td>18청렴세제 리필4KG(GS리테일마</td>
      <td>0.0</td>
      <td>E</td>
      <td>2019-12-01 00:00:00.100</td>
      <td>0.0</td>
      <td>2019</td>
      <td>12</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1483</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6067006</td>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>0.0</td>
      <td>M</td>
      <td>2020-12-01 00:00:00.200</td>
      <td>425.6</td>
      <td>2020</td>
      <td>12</td>
      <td>Tuesday</td>
    </tr>
    <tr>
      <th>1484</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6067006</td>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>0.0</td>
      <td>M</td>
      <td>2019-12-01 00:00:00.300</td>
      <td>41457.5</td>
      <td>2019</td>
      <td>12</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>1485</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6067006</td>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>0.0</td>
      <td>M</td>
      <td>2020-10-01 00:00:00.300</td>
      <td>107175.6</td>
      <td>2020</td>
      <td>10</td>
      <td>Thursday</td>
    </tr>
    <tr>
      <th>1486</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6067006</td>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>0.0</td>
      <td>M</td>
      <td>2020-11-01 00:00:00.300</td>
      <td>110209.3</td>
      <td>2020</td>
      <td>11</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>1487</th>
      <td>SSA</td>
      <td>6132</td>
      <td>청렴세제 오리지널</td>
      <td>6067006</td>
      <td>18청렴세제 9.5KG 리필(온라인)</td>
      <td>0.0</td>
      <td>M</td>
      <td>2020-12-01 00:00:00.300</td>
      <td>44002.2</td>
      <td>2020</td>
      <td>12</td>
      <td>Tuesday</td>
    </tr>
  </tbody>
</table>
<p>1488 rows × 12 columns</p>
</div>




```python
import seaborn as sns
import matplotlib as mpl
import matplotlib.pyplot as plt

%matplotlib inline
plt.rcParams['axes.unicode_minus'] = False
plt.rcParams['font.family'] = 'AppleGothic'

sns.barplot(data=df8, x='mm', y='판매량', hue='yy', ci=None, estimator=sum)

plt.savefig('img.png')
```


    
![png](output_22_0.png)
    



```python

```
