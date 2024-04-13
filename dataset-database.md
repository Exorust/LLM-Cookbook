# How to load data from a database?

## Basic Premise
Datasets stored in databases are typically accessed with SQL queries. With HuggingFace Datasets, you can connect to a database, query for the data you need, and create a dataset out of it. Then you can use all the processing features of HuggingFace Datasets to prepare your dataset for training.

### SQLite
SQLite is a small, lightweight database that is fast and easy to set up. You can use an existing database if you’d like, or follow along and start from scratch.

Start by creating a quick SQLite database with this Covid-19 data from the New York Times:
```
import sqlite3

import pandas as pd

conn = sqlite3.connect("us_covid_data.db")

df = pd.read_csv("https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csv")

df.to_sql("states", conn, if_exists="replace")
```

This creates a states table in the us_covid_data.db database which you can now load into a dataset.

To connect to the database, you’ll need the URI string that identifies your database. Connecting to a database with a URI caches the returned dataset. The URI string differs for each database dialect, so be sure to check the Database URLs for whichever database you’re using.

For SQLite, it is:
```
uri = "sqlite:///us_covid_data.db"
```
Load the table by passing the table name and URI to from_sql():
```
from datasets import Dataset

ds = Dataset.from_sql("states", uri)

ds
>>> Dataset({
    features: ['index', 'date', 'state', 'fips', 'cases', 'deaths'],
    num_rows: 54382
})
```
Then you can use all of 🤗 Datasets process features like filter() for example:
```
ds.filter(lambda x: x["state"] == "California")
```
You can also load a dataset from a SQL query instead of an entire table, which is useful for querying and joining multiple tables.

Load the dataset by passing your query and URI to from_sql():
```
from datasets import Dataset

ds = Dataset.from_sql('SELECT * FROM states WHERE state="California";', uri)

ds
>>> Dataset({
    features: ['index', 'date', 'state', 'fips', 'cases', 'deaths'],
    num_rows: 1019
})
```

### PostGreSQL
You can follow the steps provided in this other wiki: [NateRaw/HuggingFace-Hub-Examples/SQL](https://github.com/nateraw/huggingface-hub-examples/blob/main/sql_with_huggingface_datasets.ipynb)

## See Also
- [Datasets: Load Tabular Data](https://huggingface.co/docs/datasets/en/tabular_load)

## References

This project uses code from the following source:
- **HuggingFace**: Available at: [Datasets: Load Tabular Data](https://huggingface.co/docs/datasets/en/tabular_load)