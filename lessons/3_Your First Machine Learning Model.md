# [Our First Machine Learning Model](https://www.kaggle.com/code/dansbecker/your-first-machine-learning-model)

## Selecting a prediction target

A **prediction target** conventionally called **y** is the column in the data that we want to predict. We can get this by using dot notation. The data we get from doing this is call a **Series**. It is just like a **DataFrame** but for only a single column.

```
import pandas as pd

# reading the data
melbourne_data = pd.read_csv(/melbourne_data_path)

# selecting the prediction target column
# since we want to predict the price of houses, we will be selecting
# the *Price* column
y = melbourne_data.Price
```


## Selecting the features

**Features** are the columns that we input into our model to help with our prediction and usually referred to as **X**. We select them using bracket notation.

```
# previous code
...

# we first list out the columns we want to select in an array
melbourne_features = ["Rooms", "Distance", "Bathroom", "Landsize", "Longtitude", "Lattitude"]

X = melbourne_data[melbourne_features]
```

We can then use *describe* to display the data and *head* to display the first few rows

```
X.describe()
```

```
X.head()
```


## Building and Using the Model

We will be using the **Scikit-learn** python library to create our models. It is usually referred to as **sk-learn**. This library is the most popular library for modeling **DataFrame** type of data.

The steps for building and using the model are:
1. **Define** - what kind of model will it be? A decision tree? Some kind of other model? Some parameters of the model type are specified too.
2. **Fit** - or training. It is to captures pattern from the provided data. This is the heart of modeling
3. **Predict** - just what the word itself suggests
4. **Evaluate** - determine how accurate the predictions are.

```
# previous code
...

# importing Model we want from sk-learn library
from sk-learn import DecisionTreeRegressor

# defining the model
# many machine learning model allows randomness when training
# specifying a number in the random_state param will ensure that
# each result is the same
melbourne_model = DecisionTreeRegressor()

# training or fitting the model
melbourne_model.fit(X, y)

# predicting values
# here we used the same first 5 rows of the data
melbourne_model.predict(X.head())
```
