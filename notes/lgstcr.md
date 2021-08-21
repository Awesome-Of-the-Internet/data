# how to train a logistic regression model

```python
from sklearn.linear_model import LogisticRegression
```

```python
lrm = LogisticRegression()
```

```python
X = df[['WTT', 'PTI', 'EQW', 'SBI', 'LQE', 'QWG', 'FDJ', 'PJF', 'HQE', 'NXJ']]
y = df['TARGET CLASS']
```

```python
from sklearn.model_selection import train_test_split
```

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)
```

```python
lrm.fit(X_train, y_train)
```

```python
predictions = lrm.predict(X_test)
```

```python
from sklearn.metrics import classification_report
print(classification_report(y_test, predictions))
```