# Python Data Analysis with Pandas

This project demonstrates basic data analysis using Pandas in Python. I
practiced using functions like head(), tail(), count(), selecting
specific columns, filtering rows using conditions, and applying multiple
conditions using logical operators (& and \|).

## Project Objectives

-   Load and explore datasets using Pandas
-   Use head(), tail(), and count() for basic inspection
-   Select specific columns from the dataset
-   Filter rows using conditions
-   Use logical operators (& for AND, \| for OR)
-   Find targeted data based on multiple conditions

## Technologies Used

Python, Pandas, Jupyter Notebook / Google Colab

## Dataset Details

The dataset includes car-related information such as manufacturer,
model, engine size, city mpg, highway mpg, cylinders, and drive type.

## Loading the Dataset

``` python
import pandas as pd
mpg = pd.read_csv("mpg.csv")
```

## Basic Exploration

``` python
mpg.head()
mpg.head(10)
mpg.tail()
mpg.count()
```

## Selecting Specific Columns

``` python
mpg[["manufacturer", "model", "mpg"]]
mpg[["manufacturer", "cty", "hwy"]].head()
```

## Filtering Data

### Cars with highway mpg greater than 30

``` python
mpg[mpg["hwy"] > 30]
```

### Engine size greater than 2.5 AND city mpg above 20

``` python
mpg[(mpg["displ"] > 2.5) & (mpg["cty"] > 20)]
```

### Cars made by Ford OR Honda

``` python
mpg[(mpg["manufacturer"] == "ford") | (mpg["manufacturer"] == "honda")]
```

### Highway mpg above 25 AND manufacturer is Audi or Toyota

``` python
mpg[(mpg["hwy"] > 25) & ((mpg["manufacturer"] == "audi") | (mpg["manufacturer"] == "toyota"))]
```

## Additional Useful Commands

``` python
mpg.describe()
mpg.info()
mpg["manufacturer"].unique()
mpg["manufacturer"].value_counts()
```

## Key Learnings

-   Display dataset using head(), tail(), and count()
-   Select specific columns for cleaner display
-   Filter rows using conditions
-   Apply AND (&) and OR (\|) operators to combine multiple conditions
-   Extract rows matching specific criteria

## Future Enhancements

-   Use groupby() for grouped analysis
-   Create visualizations using Matplotlib or Seaborn
-   Handle missing data
-   Build dashboards using Streamlit or Plotly

## Conclusion

This project helped build confidence in using Pandas for basic data
analysis. I learned how to explore datasets, select columns, filter data
using conditions, and apply logical operators to extract meaningful
information.
