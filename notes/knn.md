# how to train a knn model

```python
from sklearn.model_selection import train_test_split
```

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)
```

```python
from sklearn.preprocessing import StandardScaler
```

```python
scaler = StandardScaler()
```

```python
scaler.fit(df.drop("TARGET CLASS", axis=1))
```

```python
scaled_features = scaler.transform(df.drop("TARGET CLASS", axis=1))
```

```python
df_feat = pd.DataFrame(scaled_features, columns=df.columns[:-1])
```

```python
X = df_feat # scaled_features
y = df["TARGET CLASS"]

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)
```

```python
from sklearn.neighbors import KNeighborsClassifier
```

```python
knn = KNeighborsClassifier(n_neighbors=1) # n_neighbours is the number of neighbours to use for classification (customize for your own case of usage)
```

```python
knn.fit(X_train, y_train)
```

```python
pred = knn.predict(X_test)
```

```python
from sklearn.metrics import classification_report, confusion_matrix
print(classification_report(y_test, pred))
```

```python
print(confusion_matrix(y_test, pred))
```

```python
error_rate = []

for i in range(1, 40):
  knn = KNeighborsClassifier(n_neighbors=i)
  knn.fit(X_train, y_train)
  pred = knn.predict(X_test)
  error_rate.append(np.mean(pred != y_test))
  print(f"----------------{i}:---------------")
  print(classification_report(y_test, pred))
  print(f"---------------------------------")
```

```python
plt.plot(range(1,40), error_rate, color="blue", linestyle="dashed", marker="o",
         markerfacecolor="red", markersize=10)
```

```python
print(confusion_matrix(y_test, pred))
print(classification_report(y_test, pred))
```