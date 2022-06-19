```python
import pandas as pd
import numpy as np
```


```python
d1=pd.read_excel('./Downloads/D01.xlsx')
d2=pd.read_excel('./Downloads/D02.xlsx')
d3=pd.read_excel('./Downloads/D03.xlsx')
d4=pd.read_excel('./Downloads/D04.xlsx')
d5=pd.read_excel('./Downloads/D05.xlsx')
```

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_10032/2068306046.py:4: FutureWarning: Inferring datetime64[ns] from data containing strings is deprecated and will be removed in a future version. To retain the old behavior explicitly pass Series(data, dtype={value.dtype})
      d4=pd.read_excel('./Downloads/D04.xlsx')



```python
d1.columns
```




    Index(['구분', '플랫폼', 'Base/Deal', '날짜', '요일', '납품처', 'Matching Simplified Name',
           'Simplified Name', '판매량', '비고'],
          dtype='object')




```python
d1_1=d1.groupby(['구분', '플랫폼', 'Base/Deal', '날짜','요일', '납품처', 'Simplified Name']).sum()
d2_1=d2.groupby(['구분', '플랫폼', 'Base/Deal', '날짜','요일', '납품처', 'Simplified Name']).sum()
d3_1=d3.groupby(['구분', '플랫폼', 'Base/Deal', '날짜','요일', '납품처', 'Simplified Name']).sum()
d4_1=d4.groupby(['구분', '플랫폼', 'Base/Deal', '날짜','요일', '납품처', 'Simplified Name']).sum()
d5_1=d5.groupby(['구분', '플랫폼', 'Base/Deal', '날짜','요일', '납품처', 'Simplified Name']).sum()
```


```python
d4=d4.iloc[: ,1:]
d5=d5.iloc[: ,1:]
```


```python
d1_1=d1_1.reset_index()
d2_1=d2_1.reset_index()
d3_1=d3_1.reset_index()
d4_1=d4_1.reset_index()
d5_1=d5_1.reset_index()
```


```python
d1_1.head(2)
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
d2_1.head(2)
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>B2B 특판</td>
      <td>대한푸드</td>
      <td>Base</td>
      <td>2020-07-30</td>
      <td>목요일</td>
      <td>대한푸드</td>
      <td>볶음밥깍두기-대한곱창</td>
      <td>100</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>B2B 특판</td>
      <td>대한푸드</td>
      <td>Base</td>
      <td>2020-07-31</td>
      <td>금요일</td>
      <td>대한푸드</td>
      <td>소막창</td>
      <td>4007</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
d3_1.head(2)
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>B2B 특판</td>
      <td>GS텔레서비스(특판)</td>
      <td>Base</td>
      <td>2020-10-16</td>
      <td>금요일</td>
      <td>GS텔레서비스</td>
      <td>레드칠리 스테이크</td>
      <td>34</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>B2B 특판</td>
      <td>GS텔레서비스(특판)</td>
      <td>Base</td>
      <td>2020-10-16</td>
      <td>금요일</td>
      <td>GS텔레서비스</td>
      <td>밀푀유나베</td>
      <td>39</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
d4_1=d4_1.drop('Unnamed: 0', axis=1)
```


```python
d5_1=d5_1.drop('Unnamed: 0', axis=1)

```


```python
d4_1=d4_1.iloc[: ,1:]
```


```python
d1.sort_values(by=['플랫폼']).head(2)
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Matching Simplified Name</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Online</td>
      <td>11번가</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>NaN</td>
      <td>65.고깃집된장찌개</td>
      <td>고깃집 된장찌개</td>
      <td>2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>248086</th>
      <td>Online</td>
      <td>11번가</td>
      <td>Deal</td>
      <td>2020-02-27</td>
      <td>목요일</td>
      <td>NaN</td>
      <td>15.감바스알아히요</td>
      <td>감바스 알 아히요</td>
      <td>2</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1=pd.concat([d1_1,d2_1,d3_1,d4_1,d5_1])
```


```python
df1.shape
```




    (605287, 9)




```python
df1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 605287 entries, 0 to 122906
    Data columns (total 9 columns):
     #   Column           Non-Null Count   Dtype         
    ---  ------           --------------   -----         
     0   구분               521315 non-null  object        
     1   플랫폼              605287 non-null  object        
     2   Base/Deal        605287 non-null  object        
     3   날짜               605287 non-null  datetime64[ns]
     4   요일               605287 non-null  object        
     5   납품처              605287 non-null  object        
     6   Simplified Name  605287 non-null  object        
     7   판매량              605287 non-null  int64         
     8   비고               398408 non-null  float64       
    dtypes: datetime64[ns](1), float64(1), int64(1), object(6)
    memory usage: 46.2+ MB



```python
df1.head()
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2=df1.drop(['Matching Simplified Name'], axis=1)
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_10032/1230495656.py in <module>
    ----> 1 df2=df1.drop(['Matching Simplified Name'], axis=1)
    

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/util/_decorators.py in wrapper(*args, **kwargs)
        309                     stacklevel=stacklevel,
        310                 )
    --> 311             return func(*args, **kwargs)
        312 
        313         return wrapper


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/frame.py in drop(self, labels, axis, index, columns, level, inplace, errors)
       4904                 weight  1.0     0.8
       4905         """
    -> 4906         return super().drop(
       4907             labels=labels,
       4908             axis=axis,


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/generic.py in drop(self, labels, axis, index, columns, level, inplace, errors)
       4148         for axis, labels in axes.items():
       4149             if labels is not None:
    -> 4150                 obj = obj._drop_axis(labels, axis, level=level, errors=errors)
       4151 
       4152         if inplace:


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/generic.py in _drop_axis(self, labels, axis, level, errors)
       4183                 new_axis = axis.drop(labels, level=level, errors=errors)
       4184             else:
    -> 4185                 new_axis = axis.drop(labels, errors=errors)
       4186             result = self.reindex(**{axis_name: new_axis})
       4187 


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in drop(self, labels, errors)
       6015         if mask.any():
       6016             if errors != "ignore":
    -> 6017                 raise KeyError(f"{labels[mask]} not found in axis")
       6018             indexer = indexer[~mask]
       6019         return self.delete(indexer)


    KeyError: "['Matching Simplified Name'] not found in axis"



```python
len(df1.columns)
```




    9




```python
len(df2.columns)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_10032/3975301288.py in <module>
    ----> 1 len(df2.columns)
    

    NameError: name 'df2' is not defined



```python
df1['YY']=df1['날짜'].dt.year
df1['MM']=df1['날짜'].dt.month
```


```python

```
# 월별 플랫폼별 판매량 
# 월별 플랫폼별 요일별 판매량 
# 월별 플랫포별 베이스/딜별 판매량
# 월별 플랫폼별 상위판매 20 

```python
def func1(x):
    result=str(x)
    return result[0:7]

df1['YM']=df1['날짜'].apply(func1)
```


```python
df1=df1.drop('비고', axis=1)
```


```python
df1['플랫폼'].value_counts(10)
```




    이마트집적화                0.315341
    이마트 구구스               0.174005
    롯데슈퍼(직)               0.082989
    BGF리테일                0.073098
    쿠팡(직)                 0.058627
                            ...   
    아나나스푸드                0.000003
    보성특수농산                0.000002
    건강가정다문화가족지원센터(마포구)    0.000002
    GS홈쇼핑                 0.000002
    미미식품                  0.000002
    Name: 플랫폼, Length: 105, dtype: float64




```python
df1.head()
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
      <th>index</th>
      <th>구분</th>
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>YY</th>
      <th>MM</th>
      <th>YM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
  </tbody>
</table>
</div>




```python
g=df1['판매량'].groupby(df1['YM'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in get_loc(self, key, method, tolerance)
       3360             try:
    -> 3361                 return self._engine.get_loc(casted_key)
       3362             except KeyError as err:


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/_libs/index.pyx in pandas._libs.index.IndexEngine.get_loc()


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/_libs/index.pyx in pandas._libs.index.IndexEngine.get_loc()


    pandas/_libs/hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()


    pandas/_libs/hashtable_class_helper.pxi in pandas._libs.hashtable.PyObjectHashTable.get_item()


    KeyError: 'YM'

    
    The above exception was the direct cause of the following exception:


    KeyError                                  Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_1306/2231525528.py in <module>
    ----> 1 g=df1['판매량'].groupby(df1['YM'])
    

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/frame.py in __getitem__(self, key)
       3456             if self.columns.nlevels > 1:
       3457                 return self._getitem_multilevel(key)
    -> 3458             indexer = self.columns.get_loc(key)
       3459             if is_integer(indexer):
       3460                 indexer = [indexer]


    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/indexes/base.py in get_loc(self, key, method, tolerance)
       3361                 return self._engine.get_loc(casted_key)
       3362             except KeyError as err:
    -> 3363                 raise KeyError(key) from err
       3364 
       3365         if is_scalar(key) and isna(key) and not self.hasnans:


    KeyError: 'YM'



```python
g.sum()
```




    YM
    2020-01     323407
    2020-02     381640
    2020-03     454528
    2020-04     473091
    2020-05     464725
    2020-06     485102
    2020-07     656425
    2020-08     731187
    2020-09     854636
    2020-10     895099
    2020-11     918359
    2020-12    1286153
    2021-01    1143614
    2021-02     874068
    Name: 판매량, dtype: int64




```python
g1=df1.groupby(['YM', '플랫폼']).sum().reset_index().drop(['index', 'YY', 'MM'], axis=1)
```


```python
import seaborn as sns
import matplotlib.pyplot as plt
import matplotlib as mpl

%matplotlib inline
plt.rcParams['axes.unicode_minus'] = False
plt.rcParams['font.family'] = 'AppleGothic'
```


```python
g1.sort_values(by=['판매량'],axis=0 ,ascending=['True'])
```


      File "/var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_1126/2626118264.py", line 1
        g1.sort_values(by=['판매량'],axis=0 ascending=['True'])
                                         ^
    SyntaxError: invalid syntax




```python
plt.figure(figsize=(16,5))
sns.barplot(data=g1, x='YM', y='판매량', ci=None)
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_32_1.png)
    



```python
g1.sort_values(by=['YM','판매량'],axis=0 ,ascending=[True, False])
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
      <th>YM</th>
      <th>플랫폼</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>16</th>
      <td>2020-01</td>
      <td>쿠팡(직)</td>
      <td>144847</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-01</td>
      <td>SSG(직)</td>
      <td>44250</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2020-01</td>
      <td>이마트집적화</td>
      <td>35102</td>
    </tr>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>BGF리테일</td>
      <td>30863</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2020-01</td>
      <td>배민마켓</td>
      <td>28633</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>463</th>
      <td>2021-02</td>
      <td>사러가(직)</td>
      <td>423</td>
    </tr>
    <tr>
      <th>478</th>
      <td>2021-02</td>
      <td>한화호텔앤드리조트</td>
      <td>346</td>
    </tr>
    <tr>
      <th>470</th>
      <td>2021-02</td>
      <td>이마트 특판</td>
      <td>165</td>
    </tr>
    <tr>
      <th>479</th>
      <td>2021-02</td>
      <td>현대백화점</td>
      <td>112</td>
    </tr>
    <tr>
      <th>452</th>
      <td>2021-02</td>
      <td>김집사(직)</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
<p>481 rows × 3 columns</p>
</div>




```python
쿠팡=g1['플랫폼'] =='쿠팡(직)'
SSG=g1['플랫폼'] =='SSG(직)'
이마트집적화=g1['플랫폼'] =='이마트집적화'
BGF리테일=g1['플랫폼'] =='BGF리테일'
배민마켓=g1['플랫폼'] =='배민마켓'
#이마트구구스==g1['플랫폼'] =='이마트 구구스'
#노브랜드==g1['플랫폼'] =='노브랜드'
#노브랜드김치==g1['플랫폼'] =='노브랜드 김치'
#롯데마트==g1['플랫폼'] =='롯데마트'
```


```python
g1['플랫폼'].value_counts().tolist()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_10032/3168985131.py in <module>
    ----> 1 g1['플랫폼'].value_counts().tolist()
    

    NameError: name 'g1' is not defined



```python
plt.figure(figsize=(16,5))
sns.barplot(data=g1.loc[쿠팡], x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_36_1.png)
    



```python
plt.figure(figsize=(16,5))
sns.barplot(data=g1.loc[SSG], x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_37_1.png)
    



```python
plt.figure(figsize=(16,5))
sns.barplot(data=g1.loc[이마트집적화], x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_38_1.png)
    



```python
plt.figure(figsize=(16,5))
sns.barplot(data=g1.loc[BGF리테일], x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_39_1.png)
    



```python

plt.figure(figsize=(16,5))
sns.barplot(data=g1.loc[배민마켓], x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_40_1.png)
    



```python
con1=g1['YM']=='2020-01'
g1.loc[con1].sort_values(by=['판매량'],axis=0 ,ascending=[False]).reset_index().drop('index', axis=1)
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
      <th>YM</th>
      <th>플랫폼</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>쿠팡(직)</td>
      <td>144847</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01</td>
      <td>SSG(직)</td>
      <td>44250</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01</td>
      <td>이마트집적화</td>
      <td>35102</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-01</td>
      <td>BGF리테일</td>
      <td>30863</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-01</td>
      <td>배민마켓</td>
      <td>28633</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2020-01</td>
      <td>이마트 피코크</td>
      <td>14516</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2020-01</td>
      <td>셰프찬 (옥수점)</td>
      <td>12515</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2020-01</td>
      <td>GS심플리쿡</td>
      <td>3764</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2020-01</td>
      <td>이마트 구구스</td>
      <td>3016</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2020-01</td>
      <td>GS프레시</td>
      <td>2532</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2020-01</td>
      <td>그루나무</td>
      <td>960</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2020-01</td>
      <td>SSG(Off)</td>
      <td>889</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2020-01</td>
      <td>조선호텔김치</td>
      <td>560</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2020-01</td>
      <td>아내의식탁</td>
      <td>264</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2020-01</td>
      <td>트레이더스</td>
      <td>228</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2020-01</td>
      <td>육전식당</td>
      <td>211</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2020-01</td>
      <td>세븐일레븐</td>
      <td>182</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2020-01</td>
      <td>신세계백화점</td>
      <td>75</td>
    </tr>
  </tbody>
</table>
</div>




```python
con2=g1['YM']=='2021-01'
g1.loc[con2].sort_values(by=['판매량'],axis=0 ,ascending=[False]).reset_index().drop('index', axis=1)
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
      <th>YM</th>
      <th>플랫폼</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2021-01</td>
      <td>쿠팡(직)</td>
      <td>341250</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2021-01</td>
      <td>이마트 피코크</td>
      <td>212588</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2021-01</td>
      <td>이마트 구구스</td>
      <td>95472</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2021-01</td>
      <td>SSG(직)</td>
      <td>85903</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2021-01</td>
      <td>BGF리테일</td>
      <td>83446</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2021-01</td>
      <td>배민마켓</td>
      <td>63076</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2021-01</td>
      <td>이마트집적화</td>
      <td>44057</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2021-01</td>
      <td>노브랜드</td>
      <td>36192</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2021-01</td>
      <td>노브랜드 김치</td>
      <td>31849</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2021-01</td>
      <td>롯데마트</td>
      <td>28890</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2021-01</td>
      <td>롯데슈퍼(직)</td>
      <td>26165</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2021-01</td>
      <td>세븐일레븐</td>
      <td>14673</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2021-01</td>
      <td>쿠팡(PB)</td>
      <td>11314</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2021-01</td>
      <td>삼성웰스토리(Off)</td>
      <td>11076</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2021-01</td>
      <td>홈플러스HY</td>
      <td>10167</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2021-01</td>
      <td>이마트 특판</td>
      <td>7995</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2021-01</td>
      <td>요마트</td>
      <td>6356</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2021-01</td>
      <td>조선호텔김치</td>
      <td>6210</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2021-01</td>
      <td>테이스티나인</td>
      <td>4424</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2021-01</td>
      <td>이마트 피코크 김치</td>
      <td>4250</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2021-01</td>
      <td>신세계푸드</td>
      <td>3968</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2021-01</td>
      <td>마켓컬리 김치</td>
      <td>2718</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2021-01</td>
      <td>PK마켓</td>
      <td>2662</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2021-01</td>
      <td>SSG(Off)</td>
      <td>1766</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2021-01</td>
      <td>메가마트</td>
      <td>1657</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2021-01</td>
      <td>사러가(직)</td>
      <td>1601</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2021-01</td>
      <td>롯데마트(PB)</td>
      <td>1500</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2021-01</td>
      <td>셰프찬 (옥수점)</td>
      <td>1111</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2021-01</td>
      <td>현대백화점</td>
      <td>1032</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2021-01</td>
      <td>김집사(직)</td>
      <td>127</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2021-01</td>
      <td>가든클래식스</td>
      <td>72</td>
    </tr>
    <tr>
      <th>31</th>
      <td>2021-01</td>
      <td>머니콘</td>
      <td>47</td>
    </tr>
  </tbody>
</table>
</div>




```python
g.to_frame()
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_1126/2998458327.py in <module>
    ----> 1 g.to_frame()
    

    ~/opt/anaconda3/lib/python3.9/site-packages/pandas/core/groupby/groupby.py in __getattr__(self, attr)
        909             return self[attr]
        910 
    --> 911         raise AttributeError(
        912             f"'{type(self).__name__}' object has no attribute '{attr}'"
        913         )


    AttributeError: 'SeriesGroupBy' object has no attribute 'to_frame'



```python
g1.sum()
```




    YM     2020-012020-012020-012020-012020-012020-012020...
    플랫폼    BGF리테일GS심플리쿡GS프레시SSG(Off)SSG(직)그루나무배민마켓세븐일레븐셰프...
    판매량                                              9942034
    dtype: object




```python
g1.loc[쿠팡].sum()
```




    YM     2020-012020-022020-032020-042020-052020-062020...
    플랫폼    쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠팡(직)쿠...
    판매량                                              2633804
    dtype: object




```python

```




    YM     2020-012020-012020-012020-012020-012020-012020...
    플랫폼    BGF리테일GS심플리쿡GS프레시SSG(Off)SSG(직)그루나무배민마켓세븐일레븐셰프...
    판매량                                              9942034
    dtype: object




```python
g1.groupby()  # .reset_index().drop(['index', 'YY', 'MM'], axis=1)
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
      <th>YM</th>
      <th>플랫폼</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>BGF리테일</td>
      <td>30863</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01</td>
      <td>GS심플리쿡</td>
      <td>3764</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01</td>
      <td>GS프레시</td>
      <td>2532</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-01</td>
      <td>SSG(Off)</td>
      <td>889</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-01</td>
      <td>SSG(직)</td>
      <td>44250</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>476</th>
      <td>2021-02</td>
      <td>쿠팡(PB)</td>
      <td>16877</td>
    </tr>
    <tr>
      <th>477</th>
      <td>2021-02</td>
      <td>쿠팡(직)</td>
      <td>188162</td>
    </tr>
    <tr>
      <th>478</th>
      <td>2021-02</td>
      <td>한화호텔앤드리조트</td>
      <td>346</td>
    </tr>
    <tr>
      <th>479</th>
      <td>2021-02</td>
      <td>현대백화점</td>
      <td>112</td>
    </tr>
    <tr>
      <th>480</th>
      <td>2021-02</td>
      <td>홈플러스HY</td>
      <td>10158</td>
    </tr>
  </tbody>
</table>
<p>481 rows × 3 columns</p>
</div>




```python
g2=g1.groupby(['YM']).sum().reset_index()
```


```python
plt.figure(figsize=(16,5))
sns.barplot(data=g2, x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_49_1.png)
    



```python
g2.sum()
```




    YM     2020-012020-022020-032020-042020-052020-062020...
    판매량                                              9942034
    dtype: object




```python
plt.figure(figsize=(16,5))
sns.lineplot(data=g2, x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_51_1.png)
    



```python
g2
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    /var/folders/yx/wyvgfyvx08lfvh3c_whdxxrh0000gn/T/ipykernel_3526/4204226240.py in <module>
    ----> 1 g2
    

    NameError: name 'g2' is not defined



```python
df1.head()
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
      <th>YY</th>
      <th>MM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 605287 entries, 0 to 122906
    Data columns (total 9 columns):
     #   Column           Non-Null Count   Dtype         
    ---  ------           --------------   -----         
     0   구분               521315 non-null  object        
     1   플랫폼              605287 non-null  object        
     2   Base/Deal        605287 non-null  object        
     3   날짜               605287 non-null  datetime64[ns]
     4   요일               605287 non-null  object        
     5   납품처              605287 non-null  object        
     6   Simplified Name  605287 non-null  object        
     7   판매량              605287 non-null  int64         
     8   비고               398408 non-null  float64       
    dtypes: datetime64[ns](1), float64(1), int64(1), object(6)
    memory usage: 46.2+ MB



```python
df2=df1.groupby(['날짜', '구분', '플랫폼','Base/Deal', 'Simplified Name']).sum('판매량').reset_index()
```


```python
t1=df2.groupby(['구분', '플랫폼']).sum().reset_index()
```


```python
t1['구분'].value_counts()
```




    PB         34
    B2B 특판     24
    Offline    16
    직매입        16
    Online      6
    TVHSP       6
    Name: 구분, dtype: int64




```python
t1.sort_values('판매량', ascending=False)
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
      <th>플랫폼</th>
      <th>판매량</th>
      <th>비고</th>
      <th>YY</th>
      <th>MM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>100</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>2202480</td>
      <td>0.0</td>
      <td>64226916</td>
      <td>163196</td>
    </tr>
    <tr>
      <th>70</th>
      <td>PB</td>
      <td>이마트 피코크</td>
      <td>1185597</td>
      <td>0.0</td>
      <td>27274579</td>
      <td>77742</td>
    </tr>
    <tr>
      <th>88</th>
      <td>직매입</td>
      <td>SSG(직)</td>
      <td>836683</td>
      <td>0.0</td>
      <td>53415116</td>
      <td>134341</td>
    </tr>
    <tr>
      <th>69</th>
      <td>PB</td>
      <td>이마트 구구스</td>
      <td>721133</td>
      <td>0.0</td>
      <td>186366038</td>
      <td>570357</td>
    </tr>
    <tr>
      <th>93</th>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>708943</td>
      <td>0.0</td>
      <td>45417132</td>
      <td>89768</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>B2B 특판</td>
      <td>건강가정다문화가족지원센터(마포구)</td>
      <td>30</td>
      <td>0.0</td>
      <td>2020</td>
      <td>11</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Online</td>
      <td>팍스패말리</td>
      <td>22</td>
      <td>0.0</td>
      <td>30300</td>
      <td>105</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Offline</td>
      <td>쿡포유</td>
      <td>8</td>
      <td>0.0</td>
      <td>6060</td>
      <td>26</td>
    </tr>
    <tr>
      <th>16</th>
      <td>B2B 특판</td>
      <td>오사라마켓</td>
      <td>5</td>
      <td>0.0</td>
      <td>10100</td>
      <td>50</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Online</td>
      <td>SSG(On)</td>
      <td>5</td>
      <td>0.0</td>
      <td>10100</td>
      <td>31</td>
    </tr>
  </tbody>
</table>
<p>102 rows × 6 columns</p>
</div>




```python
con1=t1['구분']=='PB'
con2=t1['구분']=='B2B 특판'
con3=t1['구분']=='Offline'
con4=t1['구분']=='직매입'
con5=t1['구분']=='Online'
con6=t1['구분']=='TVHSP'

```


```python
PB=t1.loc[con1].sort_values('판매량', ascending=False)
```


```python
B2B=t1.loc[con2].sort_values('판매량', ascending=False)
```


```python
Offline=t1.loc[con3].sort_values('판매량', ascending=False)
```


```python
직매입=t1.loc[con4].sort_values('판매량', ascending=False)
```


```python
Online=t1.loc[con5].sort_values('판매량', ascending=False)
```


```python
TVHSP=t1.loc[con6].sort_values('판매량', ascending=False)
```


```python
PB['판매량'].sum(axis=0)
```




    2665914




```python
B2B['판매량'].sum(axis=0)
```




    36211




```python
Offline['판매량'].sum(axis=0)
```




    865640




```python
직매입['판매량'].sum(axis=0)
```




    4522485




```python
Online['판매량'].sum(axis=0)
```




    8728




```python
TVHSP['판매량'].sum(axis=0)
```




    197553




```python
# PB/직매입/Offline/TVHSP
```


```python
PB.loc["total", :]=PB['판매량'].sum()
```


```python
PB
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
      <th>플랫폼</th>
      <th>판매량</th>
      <th>비고</th>
      <th>YY</th>
      <th>MM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>70</th>
      <td>PB</td>
      <td>이마트 피코크</td>
      <td>1185597.0</td>
      <td>0.0</td>
      <td>27274579.0</td>
      <td>77742.0</td>
    </tr>
    <tr>
      <th>69</th>
      <td>PB</td>
      <td>이마트 구구스</td>
      <td>721133.0</td>
      <td>0.0</td>
      <td>186366038.0</td>
      <td>570357.0</td>
    </tr>
    <tr>
      <th>50</th>
      <td>PB</td>
      <td>노브랜드 김치</td>
      <td>225980.0</td>
      <td>0.0</td>
      <td>460661.0</td>
      <td>1449.0</td>
    </tr>
    <tr>
      <th>76</th>
      <td>PB</td>
      <td>테이스티나인(홈쇼핑)</td>
      <td>104263.0</td>
      <td>0.0</td>
      <td>20200.0</td>
      <td>90.0</td>
    </tr>
    <tr>
      <th>49</th>
      <td>PB</td>
      <td>노브랜드</td>
      <td>74891.0</td>
      <td>0.0</td>
      <td>10553613.0</td>
      <td>23806.0</td>
    </tr>
    <tr>
      <th>72</th>
      <td>PB</td>
      <td>조선호텔김치</td>
      <td>71141.0</td>
      <td>0.0</td>
      <td>840419.0</td>
      <td>1816.0</td>
    </tr>
    <tr>
      <th>75</th>
      <td>PB</td>
      <td>테이스티나인</td>
      <td>59755.0</td>
      <td>0.0</td>
      <td>840364.0</td>
      <td>3431.0</td>
    </tr>
    <tr>
      <th>58</th>
      <td>PB</td>
      <td>삼성웰스토리(Off)</td>
      <td>49480.0</td>
      <td>0.0</td>
      <td>3258260.0</td>
      <td>15782.0</td>
    </tr>
    <tr>
      <th>71</th>
      <td>PB</td>
      <td>이마트 피코크 김치</td>
      <td>37573.0</td>
      <td>0.0</td>
      <td>779905.0</td>
      <td>2294.0</td>
    </tr>
    <tr>
      <th>46</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>33115.0</td>
      <td>0.0</td>
      <td>1690740.0</td>
      <td>3304.0</td>
    </tr>
    <tr>
      <th>73</th>
      <td>PB</td>
      <td>쿠팡(PB)</td>
      <td>32614.0</td>
      <td>0.0</td>
      <td>1814743.0</td>
      <td>2320.0</td>
    </tr>
    <tr>
      <th>63</th>
      <td>PB</td>
      <td>신세계푸드</td>
      <td>10897.0</td>
      <td>0.0</td>
      <td>272816.0</td>
      <td>389.0</td>
    </tr>
    <tr>
      <th>47</th>
      <td>PB</td>
      <td>GS프레시</td>
      <td>10577.0</td>
      <td>0.0</td>
      <td>2040200.0</td>
      <td>4168.0</td>
    </tr>
    <tr>
      <th>54</th>
      <td>PB</td>
      <td>마켓컬리 김치</td>
      <td>6368.0</td>
      <td>0.0</td>
      <td>22231.0</td>
      <td>16.0</td>
    </tr>
    <tr>
      <th>74</th>
      <td>PB</td>
      <td>태영아이엔씨</td>
      <td>6001.0</td>
      <td>0.0</td>
      <td>993840.0</td>
      <td>4474.0</td>
    </tr>
    <tr>
      <th>51</th>
      <td>PB</td>
      <td>닥터키친</td>
      <td>5350.0</td>
      <td>0.0</td>
      <td>470865.0</td>
      <td>703.0</td>
    </tr>
    <tr>
      <th>64</th>
      <td>PB</td>
      <td>아내의식탁</td>
      <td>5129.0</td>
      <td>0.0</td>
      <td>1454400.0</td>
      <td>3829.0</td>
    </tr>
    <tr>
      <th>53</th>
      <td>PB</td>
      <td>롯데마트(PB)</td>
      <td>4840.0</td>
      <td>0.0</td>
      <td>486957.0</td>
      <td>1274.0</td>
    </tr>
    <tr>
      <th>52</th>
      <td>PB</td>
      <td>동원홈푸드</td>
      <td>4570.0</td>
      <td>0.0</td>
      <td>305020.0</td>
      <td>1576.0</td>
    </tr>
    <tr>
      <th>57</th>
      <td>PB</td>
      <td>삼성웰스토리</td>
      <td>3666.0</td>
      <td>0.0</td>
      <td>189880.0</td>
      <td>752.0</td>
    </tr>
    <tr>
      <th>65</th>
      <td>PB</td>
      <td>얌테이블</td>
      <td>3500.0</td>
      <td>0.0</td>
      <td>14140.0</td>
      <td>72.0</td>
    </tr>
    <tr>
      <th>48</th>
      <td>PB</td>
      <td>그루나무</td>
      <td>1920.0</td>
      <td>0.0</td>
      <td>4040.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>PB</td>
      <td>신세계조선호텔</td>
      <td>1271.0</td>
      <td>0.0</td>
      <td>30300.0</td>
      <td>90.0</td>
    </tr>
    <tr>
      <th>67</th>
      <td>PB</td>
      <td>웰스토리</td>
      <td>1148.0</td>
      <td>0.0</td>
      <td>747400.0</td>
      <td>2577.0</td>
    </tr>
    <tr>
      <th>55</th>
      <td>PB</td>
      <td>마켓컬리(PB)</td>
      <td>1123.0</td>
      <td>0.0</td>
      <td>48504.0</td>
      <td>48.0</td>
    </tr>
    <tr>
      <th>79</th>
      <td>PB</td>
      <td>푸드나무</td>
      <td>881.0</td>
      <td>0.0</td>
      <td>642360.0</td>
      <td>2561.0</td>
    </tr>
    <tr>
      <th>66</th>
      <td>PB</td>
      <td>올가홀푸드</td>
      <td>861.0</td>
      <td>0.0</td>
      <td>74740.0</td>
      <td>326.0</td>
    </tr>
    <tr>
      <th>68</th>
      <td>PB</td>
      <td>육전식당</td>
      <td>811.0</td>
      <td>0.0</td>
      <td>242400.0</td>
      <td>309.0</td>
    </tr>
    <tr>
      <th>59</th>
      <td>PB</td>
      <td>삼성웰스토리(On)</td>
      <td>541.0</td>
      <td>0.0</td>
      <td>456520.0</td>
      <td>2362.0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>PB</td>
      <td>브레덴코</td>
      <td>462.0</td>
      <td>0.0</td>
      <td>8080.0</td>
      <td>36.0</td>
    </tr>
    <tr>
      <th>77</th>
      <td>PB</td>
      <td>트레이더스</td>
      <td>254.0</td>
      <td>0.0</td>
      <td>129280.0</td>
      <td>70.0</td>
    </tr>
    <tr>
      <th>60</th>
      <td>PB</td>
      <td>스낵24</td>
      <td>88.0</td>
      <td>0.0</td>
      <td>6060.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>61</th>
      <td>PB</td>
      <td>신세계백화점</td>
      <td>75.0</td>
      <td>0.0</td>
      <td>8080.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>78</th>
      <td>PB</td>
      <td>팍스패밀리</td>
      <td>39.0</td>
      <td>0.0</td>
      <td>62620.0</td>
      <td>218.0</td>
    </tr>
    <tr>
      <th>total</th>
      <td>2665914</td>
      <td>2665914</td>
      <td>2665914.0</td>
      <td>2665914.0</td>
      <td>2665914.0</td>
      <td>2665914.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
PB
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
      <th>플랫폼</th>
      <th>판매량</th>
      <th>비고</th>
      <th>YY</th>
      <th>MM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>70</th>
      <td>PB</td>
      <td>이마트 피코크</td>
      <td>1185597</td>
      <td>0.0</td>
      <td>27274579</td>
      <td>77742</td>
    </tr>
    <tr>
      <th>69</th>
      <td>PB</td>
      <td>이마트 구구스</td>
      <td>721133</td>
      <td>0.0</td>
      <td>186366038</td>
      <td>570357</td>
    </tr>
    <tr>
      <th>50</th>
      <td>PB</td>
      <td>노브랜드 김치</td>
      <td>225980</td>
      <td>0.0</td>
      <td>460661</td>
      <td>1449</td>
    </tr>
    <tr>
      <th>76</th>
      <td>PB</td>
      <td>테이스티나인(홈쇼핑)</td>
      <td>104263</td>
      <td>0.0</td>
      <td>20200</td>
      <td>90</td>
    </tr>
    <tr>
      <th>49</th>
      <td>PB</td>
      <td>노브랜드</td>
      <td>74891</td>
      <td>0.0</td>
      <td>10553613</td>
      <td>23806</td>
    </tr>
    <tr>
      <th>72</th>
      <td>PB</td>
      <td>조선호텔김치</td>
      <td>71141</td>
      <td>0.0</td>
      <td>840419</td>
      <td>1816</td>
    </tr>
    <tr>
      <th>75</th>
      <td>PB</td>
      <td>테이스티나인</td>
      <td>59755</td>
      <td>0.0</td>
      <td>840364</td>
      <td>3431</td>
    </tr>
    <tr>
      <th>58</th>
      <td>PB</td>
      <td>삼성웰스토리(Off)</td>
      <td>49480</td>
      <td>0.0</td>
      <td>3258260</td>
      <td>15782</td>
    </tr>
    <tr>
      <th>71</th>
      <td>PB</td>
      <td>이마트 피코크 김치</td>
      <td>37573</td>
      <td>0.0</td>
      <td>779905</td>
      <td>2294</td>
    </tr>
    <tr>
      <th>46</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>33115</td>
      <td>0.0</td>
      <td>1690740</td>
      <td>3304</td>
    </tr>
    <tr>
      <th>73</th>
      <td>PB</td>
      <td>쿠팡(PB)</td>
      <td>32614</td>
      <td>0.0</td>
      <td>1814743</td>
      <td>2320</td>
    </tr>
    <tr>
      <th>63</th>
      <td>PB</td>
      <td>신세계푸드</td>
      <td>10897</td>
      <td>0.0</td>
      <td>272816</td>
      <td>389</td>
    </tr>
    <tr>
      <th>47</th>
      <td>PB</td>
      <td>GS프레시</td>
      <td>10577</td>
      <td>0.0</td>
      <td>2040200</td>
      <td>4168</td>
    </tr>
    <tr>
      <th>54</th>
      <td>PB</td>
      <td>마켓컬리 김치</td>
      <td>6368</td>
      <td>0.0</td>
      <td>22231</td>
      <td>16</td>
    </tr>
    <tr>
      <th>74</th>
      <td>PB</td>
      <td>태영아이엔씨</td>
      <td>6001</td>
      <td>0.0</td>
      <td>993840</td>
      <td>4474</td>
    </tr>
    <tr>
      <th>51</th>
      <td>PB</td>
      <td>닥터키친</td>
      <td>5350</td>
      <td>0.0</td>
      <td>470865</td>
      <td>703</td>
    </tr>
    <tr>
      <th>64</th>
      <td>PB</td>
      <td>아내의식탁</td>
      <td>5129</td>
      <td>0.0</td>
      <td>1454400</td>
      <td>3829</td>
    </tr>
    <tr>
      <th>53</th>
      <td>PB</td>
      <td>롯데마트(PB)</td>
      <td>4840</td>
      <td>0.0</td>
      <td>486957</td>
      <td>1274</td>
    </tr>
    <tr>
      <th>52</th>
      <td>PB</td>
      <td>동원홈푸드</td>
      <td>4570</td>
      <td>0.0</td>
      <td>305020</td>
      <td>1576</td>
    </tr>
    <tr>
      <th>57</th>
      <td>PB</td>
      <td>삼성웰스토리</td>
      <td>3666</td>
      <td>0.0</td>
      <td>189880</td>
      <td>752</td>
    </tr>
    <tr>
      <th>65</th>
      <td>PB</td>
      <td>얌테이블</td>
      <td>3500</td>
      <td>0.0</td>
      <td>14140</td>
      <td>72</td>
    </tr>
    <tr>
      <th>48</th>
      <td>PB</td>
      <td>그루나무</td>
      <td>1920</td>
      <td>0.0</td>
      <td>4040</td>
      <td>3</td>
    </tr>
    <tr>
      <th>62</th>
      <td>PB</td>
      <td>신세계조선호텔</td>
      <td>1271</td>
      <td>0.0</td>
      <td>30300</td>
      <td>90</td>
    </tr>
    <tr>
      <th>67</th>
      <td>PB</td>
      <td>웰스토리</td>
      <td>1148</td>
      <td>0.0</td>
      <td>747400</td>
      <td>2577</td>
    </tr>
    <tr>
      <th>55</th>
      <td>PB</td>
      <td>마켓컬리(PB)</td>
      <td>1123</td>
      <td>0.0</td>
      <td>48504</td>
      <td>48</td>
    </tr>
    <tr>
      <th>79</th>
      <td>PB</td>
      <td>푸드나무</td>
      <td>881</td>
      <td>0.0</td>
      <td>642360</td>
      <td>2561</td>
    </tr>
    <tr>
      <th>66</th>
      <td>PB</td>
      <td>올가홀푸드</td>
      <td>861</td>
      <td>0.0</td>
      <td>74740</td>
      <td>326</td>
    </tr>
    <tr>
      <th>68</th>
      <td>PB</td>
      <td>육전식당</td>
      <td>811</td>
      <td>0.0</td>
      <td>242400</td>
      <td>309</td>
    </tr>
    <tr>
      <th>59</th>
      <td>PB</td>
      <td>삼성웰스토리(On)</td>
      <td>541</td>
      <td>0.0</td>
      <td>456520</td>
      <td>2362</td>
    </tr>
    <tr>
      <th>56</th>
      <td>PB</td>
      <td>브레덴코</td>
      <td>462</td>
      <td>0.0</td>
      <td>8080</td>
      <td>36</td>
    </tr>
    <tr>
      <th>77</th>
      <td>PB</td>
      <td>트레이더스</td>
      <td>254</td>
      <td>0.0</td>
      <td>129280</td>
      <td>70</td>
    </tr>
    <tr>
      <th>60</th>
      <td>PB</td>
      <td>스낵24</td>
      <td>88</td>
      <td>0.0</td>
      <td>6060</td>
      <td>6</td>
    </tr>
    <tr>
      <th>61</th>
      <td>PB</td>
      <td>신세계백화점</td>
      <td>75</td>
      <td>0.0</td>
      <td>8080</td>
      <td>4</td>
    </tr>
    <tr>
      <th>78</th>
      <td>PB</td>
      <td>팍스패밀리</td>
      <td>39</td>
      <td>0.0</td>
      <td>62620</td>
      <td>218</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3=df2.iloc[:, :6]
```


```python
df3
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
      <th>날짜</th>
      <th>구분</th>
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>Simplified Name</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>고깃집 된장찌개</td>
      <td>6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>더블스노우 함박 스테이크</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>마라탕</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>밀푀유나베</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>소고기 찹스테이크</td>
      <td>16</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>95258</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>참오징어젓 200g</td>
      <td>20</td>
    </tr>
    <tr>
      <th>95259</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>청포도 리코타 치즈 샐러드</td>
      <td>324</td>
    </tr>
    <tr>
      <th>95260</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>치즈품은닭갈비</td>
      <td>56</td>
    </tr>
    <tr>
      <th>95261</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>토마토 카프레제 샐러드</td>
      <td>300</td>
    </tr>
    <tr>
      <th>95262</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>햄치즈순두부찌개</td>
      <td>12</td>
    </tr>
  </tbody>
</table>
<p>95263 rows × 6 columns</p>
</div>




```python
def func1(x):
    result=str(x)
    return result[0:7]

df3['YM']=df3['날짜'].apply(func1)
```


```python
g4=df3.groupby(['구분', 'YM']).sum().reset_index().sort_values(['YM','판매량'], ascending=True).set_index('YM').reset_index()
```


```python
g4
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>PB</td>
      <td>26126</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01</td>
      <td>Offline</td>
      <td>48506</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01</td>
      <td>직매입</td>
      <td>248775</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-02</td>
      <td>PB</td>
      <td>33127</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-02</td>
      <td>Offline</td>
      <td>34639</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2020-02</td>
      <td>직매입</td>
      <td>313874</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2020-03</td>
      <td>Offline</td>
      <td>42400</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2020-03</td>
      <td>PB</td>
      <td>86836</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2020-03</td>
      <td>직매입</td>
      <td>325292</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2020-04</td>
      <td>Offline</td>
      <td>27896</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2020-04</td>
      <td>PB</td>
      <td>122537</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2020-04</td>
      <td>직매입</td>
      <td>322658</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2020-05</td>
      <td>Offline</td>
      <td>33862</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2020-05</td>
      <td>PB</td>
      <td>98391</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2020-05</td>
      <td>직매입</td>
      <td>332472</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2020-06</td>
      <td>Online</td>
      <td>4</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2020-06</td>
      <td>Offline</td>
      <td>45849</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2020-06</td>
      <td>PB</td>
      <td>144794</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2020-06</td>
      <td>직매입</td>
      <td>294455</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2020-07</td>
      <td>Online</td>
      <td>23</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2020-07</td>
      <td>B2B 특판</td>
      <td>22478</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2020-07</td>
      <td>Offline</td>
      <td>61563</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2020-07</td>
      <td>TVHSP</td>
      <td>111020</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2020-07</td>
      <td>PB</td>
      <td>169039</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2020-07</td>
      <td>직매입</td>
      <td>292302</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2020-08</td>
      <td>B2B 특판</td>
      <td>3981</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2020-08</td>
      <td>Online</td>
      <td>5596</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2020-08</td>
      <td>Offline</td>
      <td>79694</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2020-08</td>
      <td>TVHSP</td>
      <td>83465</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2020-08</td>
      <td>PB</td>
      <td>242549</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2020-08</td>
      <td>직매입</td>
      <td>315902</td>
    </tr>
    <tr>
      <th>31</th>
      <td>2020-09</td>
      <td>B2B 특판</td>
      <td>689</td>
    </tr>
    <tr>
      <th>32</th>
      <td>2020-09</td>
      <td>Online</td>
      <td>1088</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2020-09</td>
      <td>Offline</td>
      <td>92994</td>
    </tr>
    <tr>
      <th>34</th>
      <td>2020-09</td>
      <td>PB</td>
      <td>365943</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2020-09</td>
      <td>직매입</td>
      <td>393922</td>
    </tr>
    <tr>
      <th>36</th>
      <td>2020-10</td>
      <td>Online</td>
      <td>1820</td>
    </tr>
    <tr>
      <th>37</th>
      <td>2020-10</td>
      <td>TVHSP</td>
      <td>2080</td>
    </tr>
    <tr>
      <th>38</th>
      <td>2020-10</td>
      <td>B2B 특판</td>
      <td>4511</td>
    </tr>
    <tr>
      <th>39</th>
      <td>2020-10</td>
      <td>Offline</td>
      <td>78070</td>
    </tr>
    <tr>
      <th>40</th>
      <td>2020-10</td>
      <td>PB</td>
      <td>358691</td>
    </tr>
    <tr>
      <th>41</th>
      <td>2020-10</td>
      <td>직매입</td>
      <td>449927</td>
    </tr>
    <tr>
      <th>42</th>
      <td>2020-11</td>
      <td>Online</td>
      <td>197</td>
    </tr>
    <tr>
      <th>43</th>
      <td>2020-11</td>
      <td>TVHSP</td>
      <td>988</td>
    </tr>
    <tr>
      <th>44</th>
      <td>2020-11</td>
      <td>B2B 특판</td>
      <td>4433</td>
    </tr>
    <tr>
      <th>45</th>
      <td>2020-11</td>
      <td>Offline</td>
      <td>79180</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2020-11</td>
      <td>PB</td>
      <td>248197</td>
    </tr>
    <tr>
      <th>47</th>
      <td>2020-11</td>
      <td>직매입</td>
      <td>338386</td>
    </tr>
    <tr>
      <th>48</th>
      <td>2021-01</td>
      <td>B2B 특판</td>
      <td>119</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2021-01</td>
      <td>Offline</td>
      <td>95006</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2021-01</td>
      <td>PB</td>
      <td>373893</td>
    </tr>
    <tr>
      <th>51</th>
      <td>2021-01</td>
      <td>직매입</td>
      <td>562224</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2021-02</td>
      <td>Offline</td>
      <td>145981</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2021-02</td>
      <td>직매입</td>
      <td>332296</td>
    </tr>
    <tr>
      <th>54</th>
      <td>2021-02</td>
      <td>PB</td>
      <td>395791</td>
    </tr>
  </tbody>
</table>
</div>




```python
con1=g4['YM'] =='2020-01'
d202001=g4.loc[con1]
d202001
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>PB</td>
      <td>26126</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01</td>
      <td>Offline</td>
      <td>48506</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01</td>
      <td>직매입</td>
      <td>248775</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib as mlp
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
plt.rcParams['axes.unicode_minus'] = False
plt.rcParams['font.family'] = 'AppleGothic'


plt.figure(figsize=(16,6))
sns.barplot(data=d202001, x='구분', y='판매량')

```




    <AxesSubplot:xlabel='구분', ylabel='판매량'>




    
![png](output_82_1.png)
    



```python
con2=g4['YM'] =='2021-01'
d202101=g4.loc[con2]
d202101
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>48</th>
      <td>2021-01</td>
      <td>B2B 특판</td>
      <td>119</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2021-01</td>
      <td>Offline</td>
      <td>95006</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2021-01</td>
      <td>PB</td>
      <td>373893</td>
    </tr>
    <tr>
      <th>51</th>
      <td>2021-01</td>
      <td>직매입</td>
      <td>562224</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize=(16,6))
sns.barplot(data=d202101, x='구분', y='판매량')

```




    <AxesSubplot:xlabel='구분', ylabel='판매량'>




    
![png](output_84_1.png)
    



```python
con3=g4['구분'] =='직매입'
direct=g4.loc[con3]
direct
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>2020-01</td>
      <td>직매입</td>
      <td>248775</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2020-02</td>
      <td>직매입</td>
      <td>313874</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2020-03</td>
      <td>직매입</td>
      <td>325292</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2020-04</td>
      <td>직매입</td>
      <td>322658</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2020-05</td>
      <td>직매입</td>
      <td>332472</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2020-06</td>
      <td>직매입</td>
      <td>294455</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2020-07</td>
      <td>직매입</td>
      <td>292302</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2020-08</td>
      <td>직매입</td>
      <td>315902</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2020-09</td>
      <td>직매입</td>
      <td>393922</td>
    </tr>
    <tr>
      <th>41</th>
      <td>2020-10</td>
      <td>직매입</td>
      <td>449927</td>
    </tr>
    <tr>
      <th>47</th>
      <td>2020-11</td>
      <td>직매입</td>
      <td>338386</td>
    </tr>
    <tr>
      <th>51</th>
      <td>2021-01</td>
      <td>직매입</td>
      <td>562224</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2021-02</td>
      <td>직매입</td>
      <td>332296</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize=(16,6))
sns.barplot(data=direct, x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_86_1.png)
    



```python
con4=g4['구분'] =='PB'
PB=g4.loc[con4]
PB
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01</td>
      <td>PB</td>
      <td>26126</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-02</td>
      <td>PB</td>
      <td>33127</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2020-03</td>
      <td>PB</td>
      <td>86836</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2020-04</td>
      <td>PB</td>
      <td>122537</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2020-05</td>
      <td>PB</td>
      <td>98391</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2020-06</td>
      <td>PB</td>
      <td>144794</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2020-07</td>
      <td>PB</td>
      <td>169039</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2020-08</td>
      <td>PB</td>
      <td>242549</td>
    </tr>
    <tr>
      <th>34</th>
      <td>2020-09</td>
      <td>PB</td>
      <td>365943</td>
    </tr>
    <tr>
      <th>40</th>
      <td>2020-10</td>
      <td>PB</td>
      <td>358691</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2020-11</td>
      <td>PB</td>
      <td>248197</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2021-01</td>
      <td>PB</td>
      <td>373893</td>
    </tr>
    <tr>
      <th>54</th>
      <td>2021-02</td>
      <td>PB</td>
      <td>395791</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize=(16,6))
sns.barplot(data=PB, x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_88_1.png)
    



```python
con5=g4['구분'] =='Offline'
OFF=g4.loc[con5]
OFF
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
      <th>YM</th>
      <th>구분</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>2020-01</td>
      <td>Offline</td>
      <td>48506</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-02</td>
      <td>Offline</td>
      <td>34639</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2020-03</td>
      <td>Offline</td>
      <td>42400</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2020-04</td>
      <td>Offline</td>
      <td>27896</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2020-05</td>
      <td>Offline</td>
      <td>33862</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2020-06</td>
      <td>Offline</td>
      <td>45849</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2020-07</td>
      <td>Offline</td>
      <td>61563</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2020-08</td>
      <td>Offline</td>
      <td>79694</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2020-09</td>
      <td>Offline</td>
      <td>92994</td>
    </tr>
    <tr>
      <th>39</th>
      <td>2020-10</td>
      <td>Offline</td>
      <td>78070</td>
    </tr>
    <tr>
      <th>45</th>
      <td>2020-11</td>
      <td>Offline</td>
      <td>79180</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2021-01</td>
      <td>Offline</td>
      <td>95006</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2021-02</td>
      <td>Offline</td>
      <td>145981</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.figure(figsize=(16,6))
sns.barplot(data=OFF, x='YM', y='판매량')
```




    <AxesSubplot:xlabel='YM', ylabel='판매량'>




    
![png](output_90_1.png)
    



```python
df3.to_excel('./Downloads/Fresh.xlx')
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
      <th>날짜</th>
      <th>구분</th>
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>YM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>고깃집 된장찌개</td>
      <td>6</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>더블스노우 함박 스테이크</td>
      <td>7</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>마라탕</td>
      <td>2</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>밀푀유나베</td>
      <td>5</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-01-01</td>
      <td>Offline</td>
      <td>SSG(Off)</td>
      <td>Base</td>
      <td>소고기 찹스테이크</td>
      <td>16</td>
      <td>2020-01</td>
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
    </tr>
    <tr>
      <th>95258</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>참오징어젓 200g</td>
      <td>20</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>95259</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>청포도 리코타 치즈 샐러드</td>
      <td>324</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>95260</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>치즈품은닭갈비</td>
      <td>56</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>95261</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>토마토 카프레제 샐러드</td>
      <td>300</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>95262</th>
      <td>2021-02-28</td>
      <td>직매입</td>
      <td>배민마켓</td>
      <td>Base</td>
      <td>햄치즈순두부찌개</td>
      <td>12</td>
      <td>2021-02</td>
    </tr>
  </tbody>
</table>
<p>95263 rows × 7 columns</p>
</div>




```python
df1.head()
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.shape
```




    (605287, 9)




```python
df1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 605287 entries, 0 to 122906
    Data columns (total 9 columns):
     #   Column           Non-Null Count   Dtype         
    ---  ------           --------------   -----         
     0   구분               521315 non-null  object        
     1   플랫폼              605287 non-null  object        
     2   Base/Deal        605287 non-null  object        
     3   날짜               605287 non-null  datetime64[ns]
     4   요일               605287 non-null  object        
     5   납품처              605287 non-null  object        
     6   Simplified Name  605287 non-null  object        
     7   판매량              605287 non-null  int64         
     8   비고               398408 non-null  float64       
    dtypes: datetime64[ns](1), float64(1), int64(1), object(6)
    memory usage: 46.2+ MB



```python
df1['yy']=df1['날짜'].dt.year
df1['mm']=df1['날짜'].dt.month
```


```python
df1['yy'].value_counts()
```




    2020    477699
    2021    127588
    Name: yy, dtype: int64




```python
df1['mm'].value_counts()
```




    1     94553
    2     92465
    11    67977
    12    60506
    10    57879
    8     47112
    9     41918
    7     34178
    3     29026
    6     27618
    5     26211
    4     25844
    Name: mm, dtype: int64




```python
con1=df1['yy']==2020
con2=df1['yy']==2021
```


```python
d_2020=df1.loc[con1]
d_2021=df1.loc[con2]
```


```python
d_2020['mm'].value_counts()
```




    11    67977
    12    60506
    10    57879
    8     47112
    9     41918
    7     34178
    1     31332
    3     29026
    2     28098
    6     27618
    5     26211
    4     25844
    Name: mm, dtype: int64




```python
import seaborn as sns
import matplotlib.pyplot as plt
import matplotlib as mpl

%matplotlib inline
plt.rcParams['axes.unicode_minus'] = False
plt.rcParams['font.family'] = 'AppleGothic'

```


```python
d_2020
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
      <th>yy</th>
      <th>mm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
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
    </tr>
    <tr>
      <th>83955</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-30</td>
      <td>수요일</td>
      <td>용인3</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>33</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83956</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>부천2</td>
      <td>더큰 쉬림프 크랜베리 스테이크</td>
      <td>6</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83957</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>부천2</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>3</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83958</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>더큰 쉬림프 크랜베리 스테이크</td>
      <td>276</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83959</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>207</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
  </tbody>
</table>
<p>477699 rows × 11 columns</p>
</div>




```python
order=d_2020['플랫폼'].value_counts().index.tolist()
order[:9]
```




    ['이마트집적화',
     '이마트 구구스',
     'BGF리테일',
     '롯데슈퍼(직)',
     '쿠팡(직)',
     'SSG(직)',
     '배민마켓',
     '롯데마트',
     '롯데슈퍼(Off)']




```python
plt.figure(figsize=[16,5])
sns.countplot(data=d_2020, x='납품처', order=order[:10])
```




    <AxesSubplot:xlabel='납품처', ylabel='count'>




    
![png](output_104_1.png)
    



```python
df2=d_2020.groupby(['플랫폼', 'mm']).sum().reset_index().iloc[:, 0:3]
```


```python
df3=d_2021.groupby(['플랫폼', 'mm']).sum().reset_index().iloc[:, 0:3]
```


```python
df2['플랫폼'].unique()
```




    array(['BGF리테일', 'GS리테일', 'GS심플리쿡', 'GS텔레서비스(특판)', 'GS프레시', 'GS홈쇼핑',
           'PK마켓', 'SSG(Off)', 'SSG(On)', 'SSG(off)', 'SSG(직)', '가든클래식스',
           '갤러리아타임월드(직)', '건강가정다문화가족지원센터(마포구)', '건강가정다문화지원센터(산청군)',
           '건강가정지원센터(평택)', '공공기관 특판', '공영홈쇼핑', '교촌', '그루나무', '김집사(직)',
           '내추럴초이스', '노브랜드', '노브랜드 김치', '다문화가족지원센터', '닥터키친', '대한푸드', '더리본샵',
           '동원홈푸드', '디피엘컴퍼니', '띵굴마켓', '롯데마트', '롯데마트(PB)', '롯데슈퍼(Off)',
           '롯데슈퍼(On)', '롯데슈퍼(직)', '마켓컬리 김치', '머니콘', '메가마트', '미도파(공영홈쇼핑)',
           '미도파(홈앤쇼핑)', '미미식품', '배민마켓', '벤디스(식권대장)', '보성특수농산', '부국상사', '브레덴코',
           '사러가(직)', '삼성웰스토리', '삼성웰스토리(Off)', '삼성웰스토리(On)', '세븐일레븐',
           '셰프찬 (옥수점)', '스낵24', '시원', '신세계백화점', '신세계조선호텔', '신세계푸드', '씨앤티플라넷',
           '아나나스푸드', '아내의식탁', '얌테이블', '엠알케이', '오사라마켓', '올가홀푸드', '요마트', '웰스토리',
           '육전식당', '윤스오리지널', '이마트 구구스', '이마트 특판', '이마트 피코크', '이마트 피코크 김치',
           '이마트집적화', '정육각', '제이커머스', '조선호텔김치', '쿠팡(PB)', '쿠팡(직)', '쿡포유',
           '태영아이엔씨', '테이스티나인', '테이스티나인(홈쇼핑)', '트레이더스', '팍스패말리', '팍스패밀리',
           '페이즈커뮤', '평택시 서정동복지센터', '푸드나무', '푸드머스(PB)', '푸드패밀리', '풍성',
           '하이웨이마트', '한솥', '한화호텔앤드리조트', '해강물류', '해강물산(공영홈쇼핑)', '헬로네이처',
           '현대백화점', '홈앤쇼핑', '홈플러스EXP', '홈플러스HY'], dtype=object)




```python
df2.groupby(['플랫폼']).sum().reset_index().sort_values(['판매량'], ascending=False)
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
      <th>플랫폼</th>
      <th>mm</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>78</th>
      <td>쿠팡(직)</td>
      <td>78</td>
      <td>2104392</td>
    </tr>
    <tr>
      <th>71</th>
      <td>이마트 피코크</td>
      <td>78</td>
      <td>1020452</td>
    </tr>
    <tr>
      <th>10</th>
      <td>SSG(직)</td>
      <td>78</td>
      <td>831595</td>
    </tr>
    <tr>
      <th>42</th>
      <td>배민마켓</td>
      <td>78</td>
      <td>685652</td>
    </tr>
    <tr>
      <th>69</th>
      <td>이마트 구구스</td>
      <td>78</td>
      <td>670389</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>84</th>
      <td>팍스패말리</td>
      <td>7</td>
      <td>22</td>
    </tr>
    <tr>
      <th>37</th>
      <td>머니콘</td>
      <td>23</td>
      <td>16</td>
    </tr>
    <tr>
      <th>79</th>
      <td>쿡포유</td>
      <td>30</td>
      <td>10</td>
    </tr>
    <tr>
      <th>63</th>
      <td>오사라마켓</td>
      <td>10</td>
      <td>5</td>
    </tr>
    <tr>
      <th>8</th>
      <td>SSG(On)</td>
      <td>13</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
<p>102 rows × 3 columns</p>
</div>




```python
df3.groupby(['플랫폼']).sum().reset_index().sort_values(['판매량'], ascending=False)
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
      <th>플랫폼</th>
      <th>mm</th>
      <th>판매량</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>32</th>
      <td>쿠팡(직)</td>
      <td>3</td>
      <td>529412</td>
    </tr>
    <tr>
      <th>26</th>
      <td>이마트 피코크</td>
      <td>3</td>
      <td>432542</td>
    </tr>
    <tr>
      <th>24</th>
      <td>이마트 구구스</td>
      <td>3</td>
      <td>169250</td>
    </tr>
    <tr>
      <th>4</th>
      <td>SSG(직)</td>
      <td>3</td>
      <td>133905</td>
    </tr>
    <tr>
      <th>17</th>
      <td>배민마켓</td>
      <td>3</td>
      <td>116879</td>
    </tr>
    <tr>
      <th>29</th>
      <td>이마트집적화</td>
      <td>3</td>
      <td>91382</td>
    </tr>
    <tr>
      <th>0</th>
      <td>BGF리테일</td>
      <td>3</td>
      <td>90723</td>
    </tr>
    <tr>
      <th>8</th>
      <td>노브랜드 김치</td>
      <td>3</td>
      <td>65961</td>
    </tr>
    <tr>
      <th>10</th>
      <td>롯데마트</td>
      <td>3</td>
      <td>65006</td>
    </tr>
    <tr>
      <th>19</th>
      <td>삼성웰스토리(Off)</td>
      <td>3</td>
      <td>58292</td>
    </tr>
    <tr>
      <th>7</th>
      <td>노브랜드</td>
      <td>3</td>
      <td>56119</td>
    </tr>
    <tr>
      <th>12</th>
      <td>롯데슈퍼(직)</td>
      <td>3</td>
      <td>44500</td>
    </tr>
    <tr>
      <th>31</th>
      <td>쿠팡(PB)</td>
      <td>3</td>
      <td>28191</td>
    </tr>
    <tr>
      <th>20</th>
      <td>세븐일레븐</td>
      <td>3</td>
      <td>20945</td>
    </tr>
    <tr>
      <th>36</th>
      <td>홈플러스HY</td>
      <td>3</td>
      <td>20325</td>
    </tr>
    <tr>
      <th>27</th>
      <td>이마트 피코크 김치</td>
      <td>3</td>
      <td>13495</td>
    </tr>
    <tr>
      <th>30</th>
      <td>조선호텔김치</td>
      <td>3</td>
      <td>11299</td>
    </tr>
    <tr>
      <th>22</th>
      <td>신세계푸드</td>
      <td>3</td>
      <td>9462</td>
    </tr>
    <tr>
      <th>25</th>
      <td>이마트 특판</td>
      <td>3</td>
      <td>8160</td>
    </tr>
    <tr>
      <th>23</th>
      <td>요마트</td>
      <td>3</td>
      <td>7909</td>
    </tr>
    <tr>
      <th>1</th>
      <td>GS슈퍼마켓</td>
      <td>2</td>
      <td>7656</td>
    </tr>
    <tr>
      <th>13</th>
      <td>마켓컬리 김치</td>
      <td>3</td>
      <td>6368</td>
    </tr>
    <tr>
      <th>9</th>
      <td>닥터키친</td>
      <td>2</td>
      <td>5142</td>
    </tr>
    <tr>
      <th>33</th>
      <td>테이스티나인</td>
      <td>1</td>
      <td>4424</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PK마켓</td>
      <td>3</td>
      <td>4244</td>
    </tr>
    <tr>
      <th>16</th>
      <td>메가마트</td>
      <td>3</td>
      <td>3048</td>
    </tr>
    <tr>
      <th>11</th>
      <td>롯데마트(PB)</td>
      <td>3</td>
      <td>2900</td>
    </tr>
    <tr>
      <th>3</th>
      <td>SSG(Off)</td>
      <td>3</td>
      <td>2777</td>
    </tr>
    <tr>
      <th>18</th>
      <td>사러가(직)</td>
      <td>3</td>
      <td>2024</td>
    </tr>
    <tr>
      <th>21</th>
      <td>셰프찬 (옥수점)</td>
      <td>3</td>
      <td>1835</td>
    </tr>
    <tr>
      <th>35</th>
      <td>현대백화점</td>
      <td>3</td>
      <td>1144</td>
    </tr>
    <tr>
      <th>14</th>
      <td>마켓컬리(PB)</td>
      <td>2</td>
      <td>1123</td>
    </tr>
    <tr>
      <th>28</th>
      <td>이마트24</td>
      <td>2</td>
      <td>638</td>
    </tr>
    <tr>
      <th>34</th>
      <td>한화호텔앤드리조트</td>
      <td>2</td>
      <td>346</td>
    </tr>
    <tr>
      <th>6</th>
      <td>김집사(직)</td>
      <td>3</td>
      <td>137</td>
    </tr>
    <tr>
      <th>5</th>
      <td>가든클래식스</td>
      <td>1</td>
      <td>72</td>
    </tr>
    <tr>
      <th>15</th>
      <td>머니콘</td>
      <td>1</td>
      <td>47</td>
    </tr>
  </tbody>
</table>
</div>




```python
d_2020.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 477699 entries, 0 to 83959
    Data columns (total 11 columns):
     #   Column           Non-Null Count   Dtype         
    ---  ------           --------------   -----         
     0   구분               398408 non-null  object        
     1   플랫폼              477699 non-null  object        
     2   Base/Deal        477699 non-null  object        
     3   날짜               477699 non-null  datetime64[ns]
     4   요일               477699 non-null  object        
     5   납품처              477699 non-null  object        
     6   Simplified Name  477699 non-null  object        
     7   판매량              477699 non-null  int64         
     8   비고               398408 non-null  float64       
     9   yy               477699 non-null  int64         
     10  mm               477699 non-null  int64         
    dtypes: datetime64[ns](1), float64(1), int64(3), object(6)
    memory usage: 59.9+ MB



```python
sns.barplot(data=d_2020, x='mm', y='판매량', estimator=sum, ci=None)
```




    <AxesSubplot:xlabel='mm', ylabel='판매량'>




    
![png](output_111_1.png)
    



```python
sns.count
```


```python
sns.barplot(data=d_2021, x='mm', y='판매량', estimator=sum, ci=None)
```




    <AxesSubplot:xlabel='mm', ylabel='판매량'>




    
![png](output_113_1.png)
    



```python
d_2020.groupby(['플랫폼', ])
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>비고</th>
      <th>yy</th>
      <th>mm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>0.0</td>
      <td>2020</td>
      <td>1</td>
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
    </tr>
    <tr>
      <th>83955</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-30</td>
      <td>수요일</td>
      <td>용인3</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>33</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83956</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>부천2</td>
      <td>더큰 쉬림프 크랜베리 스테이크</td>
      <td>6</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83957</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>부천2</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>3</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83958</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>더큰 쉬림프 크랜베리 스테이크</td>
      <td>276</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
    <tr>
      <th>83959</th>
      <td>NaN</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2020-12-31</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>207</td>
      <td>NaN</td>
      <td>2020</td>
      <td>12</td>
    </tr>
  </tbody>
</table>
<p>477699 rows × 11 columns</p>
</div>




```python
df1
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
      <th>플랫폼</th>
      <th>Base/Deal</th>
      <th>날짜</th>
      <th>요일</th>
      <th>납품처</th>
      <th>Simplified Name</th>
      <th>판매량</th>
      <th>YY</th>
      <th>MM</th>
      <th>YM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>90</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>1</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-01</td>
      <td>수요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>35</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>2</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>들깨 백순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-02</td>
      <td>목요일</td>
      <td>GS네트웍스(PB)</td>
      <td>매콤 깻잎순대볶음-GS심플리쿡</td>
      <td>50</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PB</td>
      <td>GS심플리쿡</td>
      <td>Base</td>
      <td>2020-01-03</td>
      <td>금요일</td>
      <td>GS네트웍스(PB)</td>
      <td>돼지고기 짜글이-GS심플리쿡</td>
      <td>2</td>
      <td>2020</td>
      <td>1</td>
      <td>2020-01</td>
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
    </tr>
    <tr>
      <th>122902</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2021-02-25</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>쉬림프 네로 스파게티</td>
      <td>42</td>
      <td>2021</td>
      <td>2</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>122903</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2021-02-25</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>시칠리아 베이컨 파스타</td>
      <td>24</td>
      <td>2021</td>
      <td>2</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>122904</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2021-02-25</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>짬뽕 순두부찌개</td>
      <td>48</td>
      <td>2021</td>
      <td>2</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>122905</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2021-02-25</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>파빌리온 설악 황태진국</td>
      <td>36</td>
      <td>2021</td>
      <td>2</td>
      <td>2021-02</td>
    </tr>
    <tr>
      <th>122906</th>
      <td>직매입</td>
      <td>쿠팡(직)</td>
      <td>Deal</td>
      <td>2021-02-25</td>
      <td>목요일</td>
      <td>용인3</td>
      <td>파빌리온 얼큰 소고기전골</td>
      <td>87</td>
      <td>2021</td>
      <td>2</td>
      <td>2021-02</td>
    </tr>
  </tbody>
</table>
<p>605287 rows × 11 columns</p>
</div>




```python
df1['플랫폼'].value_counts().
```




    [190872,
     105323,
     50232,
     44245,
     35486,
     30112,
     28599,
     23491,
     15338,
     13684,
     13383,
     11474,
     6382,
     4687,
     4207,
     3662,
     2778,
     2340,
     1904,
     1556,
     1225,
     1222,
     1127,
     1101,
     1031,
     968,
     839,
     734,
     614,
     532,
     497,
     480,
     450,
     414,
     370,
     362,
     302,
     287,
     233,
     196,
     193,
     192,
     181,
     157,
     144,
     138,
     120,
     109,
     100,
     94,
     87,
     83,
     64,
     64,
     52,
     46,
     46,
     45,
     44,
     40,
     37,
     34,
     31,
     30,
     30,
     29,
     28,
     27,
     27,
     24,
     23,
     15,
     15,
     15,
     15,
     15,
     13,
     12,
     12,
     12,
     10,
     10,
     10,
     9,
     6,
     6,
     6,
     6,
     5,
     5,
     4,
     4,
     3,
     3,
     2,
     2,
     2,
     2,
     2,
     2,
     2,
     1,
     1,
     1,
     1]




```python

```
