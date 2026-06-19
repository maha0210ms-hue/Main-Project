# RetailIQ – Retail Sales Analytics Dashboard

## Description

RetailIQ is a data analytics project focused on transforming raw retail transaction data into actionable business insights. The project uses Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn for data cleaning, preprocessing, exploratory data analysis (EDA), and visualization. The processed data is then used to build an interactive Power BI dashboard that helps stakeholders monitor key business metrics and identify trends.

The project analyzes sales performance, customer purchasing behavior, product popularity, city-wise revenue contribution, and customer satisfaction ratings. Through various visualizations and KPI tracking, RetailIQ enables data-driven decision-making and provides valuable insights for business growth and operational optimization.

## Getting Started

### Dependencies

* Python 3.10 or above
* Jupyter Notebook or Google Colab
* Power BI Desktop
* Windows 10/11, macOS, or Linux
* Pandas
* NumPy
* Matplotlib
* Seaborn

### Installing

* Clone the repository from GitHub:

```bash
git clone https://github.com/yourusername/RetailIQ.git
```

* Navigate to the project directory:

```bash
cd RetailIQ
```

* Install required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

* Download the retail sales dataset and place it inside the project's data folder.

* Open the Jupyter Notebook or Google Colab notebook provided in the repository.

### Executing program

* Import the required libraries.
* Load the retail sales dataset.
* Perform data cleaning and preprocessing.
* Conduct exploratory data analysis.
* Generate business insights through visualizations.
* Export the cleaned dataset.
* Import the dataset into Power BI and create dashboards.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv("retail_sales.csv")

# Display first five rows
df.head()

# Check missing values
df.isnull().sum()

# Remove duplicates
df.drop_duplicates(inplace=True)

# Convert date column
df['Date'] = pd.to_datetime(df['Date'])

# Create day and month features
df['Day'] = df['Date'].dt.day_name()
df['Month'] = df['Date'].dt.month_name()

# Save cleaned data
df.to_csv("cleaned_retail_data.csv", index=False)
```

## Help

Any advice for common problems or issues.

### Missing Values

```python
df.isnull().sum()
```

### Duplicate Records

```python
df.drop_duplicates(inplace=True)
```

### Date Format Issues

```python
df['Date'] = pd.to_datetime(df['Date'], errors='coerce')
```

### Check Data Types

```python
df.info()
```

### Power BI Visual Labels Appear Blurry

* Increase visual size.
* Increase font size in formatting options.
* Export reports using higher resolution settings.
* Enable responsive visuals where applicable.

## Authors

Mahalakshmi

* GitHub: https://github.com/maha0210ms-hue
* LinkedIn: https://linkedin.com/in/mahalakshmi-s-192a46121/

## Version History

* 1.0
    * Completed RetailIQ Retail Sales Analytics Dashboard
    * Added data cleaning and preprocessing pipeline
    * Performed exploratory data analysis
    * Developed business KPIs and visualizations
    * Created interactive Power BI dashboard

* 0.2
    * Added feature engineering
    * Added city-wise, product-wise, and customer analysis
    * Improved visualizations and reporting

* 0.1
    * Initial Release
    * Dataset exploration and project setup

## Acknowledgments

Inspiration, documentation, and learning resources used throughout the project.

* [Pandas Documentation](https://pandas.pydata.org/)
* [NumPy Documentation](https://numpy.org/)
* [Matplotlib Documentation](https://matplotlib.org/)
* [Seaborn Documentation](https://seaborn.pydata.org/)
* [Microsoft Power BI Documentation](https://learn.microsoft.com/power-bi/)
