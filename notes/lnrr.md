# how to train a linear regression model

```python
X = df[['Avg. Area Income', 'Avg. Area House Age', 'Avg. Area Number of Rooms',
       'Avg. Area Number of Bedrooms', 'Area Population']]
y = df['Price']       
```

```python
from sklearn.model_selection import train_test_split


X_train, X_test, y_train, y_test = train_test_split(X, y, 
                                                    test_size=0.4, 
                                                    random_state=101)
```

```python
from sklearn.linear_model import LinearRegression

lm = LinearRegression()
```

```python
lm.fit(X_train, y_train)
```


```python
cdf = pd.DataFrame(lm.coef_, X.columns, columns=["Coeff"])
```

### boston dataset

```python
from sklearn.datasets import load_boston
```

```python
boston = load_boston()
```

```python
predictions = lm.predict(X_test)
```

```python
from sklearn import metrics
```

```python
metrics.mean_absolute_error(y_test, predictions)
```

```python
metrics.mean_squared_error(y_test, predictions)
```

```python
np.sqrt(metrics.mean_squared_error(y_test, predictions))
```

### project

```python
import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```

```python
customers = pd.read_csv("Ecommerce Customers")
```

```python
X = customers[['Avg. Session Length', 'Time on App',
       'Time on Website', 'Length of Membership']]
y = customers["Yearly Amount Spent"]
```

```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)
```

```python
from sklearn.linear_model import LinearRegression
lm = LinearRegression()
```

```python
lm.fit(X_train, y_train)
```

```python
predictions = lm.predict(X_test)
```

```python
from sklearn import metrics
```

```python
print("MAE ", metrics.mean_absolute_error(y_test, predictions))
```

```python
print("MSE ", metrics.mean_squared_error(y_test, predictions))
```

```python
print("RMSE ", np.sqrt(metrics.mean_squared_error(y_test, predictions)))
```

```python
metrics.explained_variance_score(y_test, predictions)
```