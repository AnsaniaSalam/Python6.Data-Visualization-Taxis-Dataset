# Data Visualization using the Taxis Dataset

This Jupyter notebook contains hands-on Python exercises on data visualization. It demonstrates how to load and clean the Seaborn `taxis` dataset, and how to explore taxi trips with ten different charts using Matplotlib, Pandas plot and Seaborn.

## Concepts Used

### Loading a Dataset
`sns.load_dataset("taxis")` loads a built-in sample dataset into a Pandas DataFrame. It contains one row per taxi trip.

### Checking Missing Values
`isnull().sum()` counts the empty cells in each column, which shows which columns need attention.

### Imputation
`fillna()` fills missing values. The mode (most frequent value) is used for the categorical columns, since mean and median only work for numbers.

### Removing Rows with Missing Values
`dropna()` removes rows with gaps. It is used on the pickup zone and borough, which are critical and cannot be reasonably guessed.

### Datetime Conversion
`pd.to_datetime()` converts a column to a proper date and time format, so it can be used on a time axis.

### Line Chart
`plt.plot()` joins points in order. It is used to show fare over pickup time, after sorting the rows by time.

### Bar Chart
`groupby()` with `sum()` totals the fare for each pickup borough, and `plot(kind='bar')` draws the result.

### Pie Chart
`value_counts()` counts trips per payment method, and `plot(kind='pie')` shows each count as a slice with its percentage.

### Histogram
`plt.hist()` groups values into bins. It is used to show the distribution of trip distance, with the number of bins customised.

### Box Plot
Shows the median, the middle 50% of values and the outliers. It is used to compare tip amounts across boroughs.

### Count Plot
`sns.countplot()` counts the rows in each category and draws the bars without any manual grouping.

### Scatter Plot
`sns.scatterplot()` shows the relationship between two numeric columns. The `hue` option colours the points by pickup borough.

### Correlation and Heatmap
`corr()` gives the correlation between numeric columns, and `sns.heatmap()` colours the matrix so strong relationships stand out.

### Pair Plot
`sns.pairplot()` draws a scatter plot for every pair of variables, coloured by pickup zone. Only the five busiest zones are used to keep the legend readable.

### Violin Plot
`sns.violinplot()` shows the full shape of a distribution. It is used to compare fares across payment methods.

### Titles, Labels and Layout
`plt.title()`, `plt.xlabel()`, `plt.ylabel()` and `plt.tight_layout()` make each chart easy to read.

### print() Function
Displays labelled output for readability.

## Running the Code

You need Python with Pandas, Matplotlib and Seaborn installed. These come installed with Anaconda. Otherwise, install them with:

```bash
pip install pandas matplotlib seaborn
```

The dataset is downloaded when the notebook runs, so an internet connection is needed the first time.

Open the notebook in Jupyter Notebook or JupyterLab and run the cells in order.

To run it from a terminal instead, execute the notebook with:

```bash
jupyter nbconvert --to notebook --execute "Data_Visualization_Taxis_Dataset.ipynb"
```
