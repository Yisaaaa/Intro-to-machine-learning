# [Basic Data Exploration](https://www.kaggle.com/code/dansbecker/basic-data-exploration)

## Using pandas

To start with our machine learning project, we first have to explore our data. We use the **pandas python library** for this. It is the primary tool for exploring and manipulating data.
Most people abbreviate pandas as pd in their code.

```
import pandas as pd
```

The most important part of Pandas is DataFrame. You might think of it as a table like in sql db or sheet in excel.

## Note

We might probably encounter a problem if you try to install pandas with the command:
`pip install pandas`

We can remedy this (and as the error says) by creating a python virtual environment venv and install the library in there.

`python -m venv /path/to/new/virtual/environment`
or
`python -m venv .venv`
