# Pandas
### Cheatsheet

```python 
pd.Series(data = my_data)
```
![](https://woosal.com/1337/chrome_nJTSNcS0Vt.png)

```python 
pd.Series(data = my_data, index = labels)
```
![](https://woosal.com/1337/chrome_QUNL0LOBvD.png)

```python
pd.Series(arr)
```
![](https://woosal.com/1337/chrome_pd1TfR0wwc.png)

```python
pd.Series(arr, labels)
```
![](https://woosal.com/1337/chrome_QzYkxUa40L.png)

```python 
pd.Series(d)
```
##### Direct dictionary usage 
![](https://woosal.com/1337/chrome_cNB4lhFfvL.png)

```python 
pd.Series(data=labels)
```
![](https://woosal.com/1337/chrome_Pq4OJk1xVZ.png)

```python 
series1 = pd.Series([1,2,3,4], ["Azerbaijan", "Turkey", "Israel", "US"])
series1
```
![](https://woosal.com/1337/chrome_RPn7LvZM96.png)

```python 
series1["Azerbaijan"]
```
![](https://woosal.com/1337/chrome_0LHtjggOyQ.png)

```python 
series2 = pd.Series([1,2,3,4,5,6,7], ["Azerbaijan", "Azerbaijan", "Germany","Azerbaijan", "Azerbaijan", "Germany","Japan"])

series2
```
![](https://woosal.com/1337/chrome_S2G9yIBWFC.png	)

```python 
series2[5]
```
![](https://woosal.com/1337/chrome_4WAocxedzo.png)

```python 
2 * series1
```
![](https://woosal.com/1337/chrome_busUieAVMs.png)

```python 
df = pd.DataFrame(np.random.randn(5,4), 
				 ["A", "B", "C", "D", "E"],
				 ["W", "X", "Y", "Z"])

df
```
![](https://woosal.com/1337/chrome_89DugJCWsS.png)

```python 
df["X"]
```
![](https://woosal.com/1337/chrome_TEcZoDCig9.png)

```python 
df[["W", "X"]]
```
![](https://woosal.com/1337/chrome_43AgUkWeMs.png)

```python 
df["new"] = df["W"] + df["Y"]
print(df)
print(df["new"])
```
![](https://woosal.com/1337/Code_pqHkJwZGvy.png)

```python 
df.drop("new", axis=1, inplace=True)
```
![](https://woosal.com/1337/Code_gIS8iscdhY.png)

```python 
df.drop("E", inplace=True)
```
![](https://woosal.com/1337/Code_JfnI9WNxXm.png)

```python 
df.loc["A"]
```
![](https://woosal.com/1337/Code_GhWejWqj1C.png)

```python 
df.iloc[0]
```
![](https://woosal.com/1337/Code_iBQFhOOpa3.png)

```python 
df.loc["A", "X"]
```
![](https://woosal.com/1337/Code_dYOoNEj86G.png)

```python 
df.loc[ ["A", "B", "C"], 
 		["Y", "Z"]]
```
![](https://woosal.com/1337/Code_8EVSXmAdlk.png)

```python 
df.iloc[[0,1], 
 		[0,1]]
```
![](https://woosal.com/1337/Code_L5C1Sh9gfB.png)

```python 
df > 0
```
![](https://woosal.com/1337/Code_tTPbHJ0X22.png)

```python 
df[df > 0]
```
![](https://woosal.com/1337/Code_zEdfs6ZlS9.png)

```python 
df["W"][df["W"] > 0]
```
![](https://woosal.com/1337/Code_14bgAwTmp7.png)

```python 
df[df["W"] > 0]
df[df["Z"] < 0]
```
![](https://woosal.com/1337/Code_0Vo1CfD2ET.png)

```python 
```

```python 
```

```python 
```

```python 
```

```python 
```

```python 
```

