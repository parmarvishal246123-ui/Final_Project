# Air Quality Analysis (Jupyter Notebook)

A step-by-step data analysis project on an air quality dataset, built with Python, Pandas, Matplotlib and Seaborn in a Jupyter Notebook.

* * *

## Project Description

This project analyzes an air quality dataset using a Jupyter Notebook. The dataset contains pollution readings (such as PM2.5, PM10, NO2, SO2, CO and O3) for different locations, along with weather factors such as temperature, humidity, wind and pressure.

The notebook is divided into six cells, one for each step of the analysis:

1. Loading the dataset
2. Exploring the dataset
3. Cleaning the dataset
4. Analyzing the most and least polluted locations
5. Finding correlations between pollution and weather
6. Visualizing the results with charts

Every step runs by simply executing the cells in order. No user input is needed, so the whole analysis can be repeated with one click.

### About the Dataset

The dataset is stored in `air_quality.csv`. The notebook finds the columns it needs automatically:

| Column type | Example column names                          | Description                                  |
|-------------|-----------------------------------------------|----------------------------------------------|
| Location    | City, Station, Location, Area, Region         | Place where the reading was taken            |
| Pollutant   | PM2.5, PM10, NO2, SO2, CO, O3, NOx, NH3, AQI  | Pollution level measured                     |
| Weather     | Temperature, Humidity, Wind, Pressure         | Weather condition at the time of the reading |

If your column names are different, edit the `pollutant_pattern` and the keyword lists in Cell 1.

* * *

## Features

| Cell | Feature               | Description                                                                                                  |
|------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| 1    | Load the dataset      | Imports the libraries, reads the CSV file and detects the pollutant, location and weather columns            |
| 2    | Explore the dataset   | Shows the first rows, number of rows and columns, data types, summary statistics and missing values          |
| 3    | Clean the dataset     | Handles missing values by dropping rows or filling with mean, median or mode, and removes duplicate rows     |
| 4    | Analyze the dataset   | Finds the most and least polluted locations, and the highest and lowest locations for each pollutant         |
| 5    | Correlation analysis  | Calculates the correlation between each pollutant and each weather factor                                    |
| 6    | Visualize the dataset | Creates bar charts, scatter plots and a correlation heatmap                                                  |

### Details of Each Cell

**Cell 1 - Load the dataset**

- Imports Pandas, NumPy, Matplotlib and Seaborn.
- Reads the CSV file from the path stored in `file_path`.
- Removes extra spaces from the column names.
- Prints a success message, or the error if the file cannot be read.
- Detects the pollutant, location and weather columns.

**Cell 2 - Explore the dataset**

- Displays the first 5 rows of the data.
- Prints the number of rows and columns.
- Lists every column with its data type.
- Shows summary statistics such as count, mean, minimum and maximum.
- Shows the number of missing values in each column.

**Cell 3 - Clean the dataset**

- Shows the missing values in each column.
- Compares four ways of handling them: drop rows, fill with mean, fill with median and fill with mode.
- Removes duplicate rows and reports how many were removed.
- Applies the final cleaning: numeric columns are filled with the mean and text columns with the mode.

**Cell 4 - Analyze the dataset**

- Calculates the average pollution of every location.
- Lists the most polluted and least polluted locations (5 each, or fewer if the dataset has only a few locations).
- Prints the most polluted and least polluted location.
- Shows the 5 highest and 5 lowest locations for each pollutant.

**Cell 5 - Correlation analysis**

- Prints the correlation between every pollutant and every weather factor.
- Shows the correlations as a table.
- Reports the strongest relationship found.

**Cell 6 - Visualize the dataset**

- Bar charts of the most and least polluted locations (up to 10 each).
- Scatter plots of average pollution against each weather factor.
- Heatmap showing the correlation between pollutants and weather factors.

* * *

## Technologies Used

| Technology           | Purpose                                                              |
|----------------------|----------------------------------------------------------------------|
| **Git**              | Version control for tracking changes in the project                  |
| **GitHub**           | Hosting the project repository                                       |
| **VS Code**          | Code editor used to write and run the notebook                       |
| **Python**           | Programming language used for the whole project                      |
| **Jupyter Notebook** | Running the code cell by cell and showing the output below each cell |
| **Pandas**           | Data loading, cleaning and analysis                                  |
| **NumPy**            | Numerical operations                                                 |
| **Matplotlib**       | Plotting scatter plots and charts                                    |
| **Seaborn**          | Bar charts and the correlation heatmap                               |

* * *

## Concepts Used

| Concept                             | Description                                                                                  | Where it is used                                      |
|-------------------------------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| DataFrames                          | A table-like structure in Pandas that stores the dataset in rows and columns                 | Loading and working with the CSV data                 |
| Exception handling (`try / except`) | Catches errors so the program does not crash if the file cannot be read                      | Loading the dataset                                   |
| Handling missing values             | Detecting blank values and fixing them by dropping rows or filling with mean, median or mode | Cleaning the dataset                                  |
| Removing duplicates                 | Finding and deleting repeated rows                                                           | Cleaning the dataset                                  |
| Grouping data                       | Combining rows by location and calculating the mean of each group                            | Average pollution of each location                    |
| Sorting and selecting data          | Ordering rows by a column and picking the top or bottom few                                  | Most and least polluted locations                     |
| Descriptive statistics              | Summary values such as count, mean, minimum and maximum                                      | Exploring the dataset                                 |
| Correlation                         | A number between -1 and +1 showing how strongly two columns are related                      | Correlation analysis and heatmap                      |
| Data visualization                  | Showing data as charts to make patterns easy to see                                          | Bar charts, scatter plots, heatmap                    |

* * *

## How to Run / Installation

### Prerequisites

- Python 3.8 or higher
- Git (to clone the repository)
- VS Code with the Python and Jupyter extensions, or Jupyter Notebook

### Steps

1. Install Python 3 from [python.org](https://www.python.org/downloads/).
2. Clone the repository:
   ```
   git clone <repository-url>
   cd <repository-folder>
   ```
3. Install the required libraries:
   ```
   pip install pandas numpy matplotlib seaborn jupyter
   ```
4. Open `air_quality_analysis.ipynb` in VS Code (with the Jupyter extension) or start Jupyter Notebook:
   ```
   jupyter notebook
   ```
5. In the first cell, check that `file_path` points to the dataset (`air_quality.csv`).
6. Run the cells from top to bottom (**Run All**, or press **Shift + Enter** on each cell).

### Notes

- Run the first cell before any other cell, because it loads the dataset that all the other cells use.
- If you restart the kernel, run the first cell again.

* * *

## Project Structure

```
│
├── air_quality.csv
├── main.ipynb
└── README.md
```

* * *

## Conclusion

This project shows how Python, Pandas and Jupyter Notebook can be used to load, clean, analyze and visualize a real-world dataset step by step. The notebook covers the complete data analysis process, from reading the raw CSV file to presenting the results as charts.

It identifies the most and least polluted locations and measures how pollution levels relate to weather factors such as temperature, humidity and wind, and the charts make these relationships easy to see. (Add your own findings here after running the notebook on your dataset.)

Through this project, the key skills of loading data, handling missing values and duplicates, grouping, sorting and selecting data, finding correlations and creating visualizations were practiced using Pandas, Matplotlib and Seaborn.

* * *

## Author

**[YOUR NAME]**