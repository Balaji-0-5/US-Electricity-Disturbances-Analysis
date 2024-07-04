# US Electricity Disturbances Analysis (2019 - 2023)

## Overview
This repository contains two Jupyter notebooks focusing on the analysis of US electricity disturbances from 2019 to 2023. The data is sourced from the [US Department of Energy](https://www.oe.netl.doe.gov/OE417_annual_summary.aspx). The first notebook focuses on data cleaning, while the second notebook performs exploratory data analysis (EDA) to uncover insights and patterns in the data.

## Notebooks

## 1. Data Cleaning
**File**: `Data_Cleaning_US_Electricity_Disturbances.ipynb`

This notebook outlines the process of cleaning the dataset to ensure it is ready for analysis. Key steps include:

- **Importing Necessary Libraries**: Libraries such as `pandas`, `numpy`, and others are imported to handle data operations and manipulations.
- **Loading the Dataset**: The raw dataset is loaded into a pandas DataFrame.
- **Standardizing Data Formats**: Ensuring consistency in data formats, such as dates and categorical variables.
- **Removing Duplicates**: Duplicate entries are identified and removed to avoid skewed results.
- **Ensuring Data Consistency**: Additional checks are performed to ensure data integrity and consistency.
- **Add or remove columns**: Add additional columns or remove existing columns based on the scope of the anlysis.
- **Save to CSV**: Saved the cleaned data frame to `electricity_disturbance_data.csv`



## 2. Exploratory Data Analysis (EDA)
**File**: `EDA_US_Electricity_Disturbances.ipynb`

This notebook provides a comprehensive analysis of the cleaned dataset to uncover trends, patterns, and insights. Key analyses include:

### **Initial Analysis**
- **Distribution**: ![Distribution of Numerical columns](/content/Plots/histograms.png)
  - **General Observations:**
    - **Skewness:** All three variables show a high degree of positive skewness, indicating that extreme values (high demand loss, many customers affected, and long event duration) are less frequent.
    - **Central Tendency:** The central tendency (mean or median) for all three variables is likely to be low due to the skewness.
    - **Variability:** There is a wide range in values for all three variables, suggesting a lot of variability in the impact of electrical disturbances.

- **Correlations**:
    [![Correlation Heatmap](/content/Plots/correlation_heatmap.png)](/content/Plots/correlation_heatmap.png)
  - **Demand Loss (MW) and Number of Customers Affected:**
     - **Correlation Coefficient:** 0.45
     - **Interpretation:** There is a moderate positive correlation between demand loss (MW) and the number of customers affected. This suggests that as the demand loss increases, the number of customers affected tends to increase as well, but the **relationship is not very strong**.
   - **Number of Customers Affected and Event Duration (hours):**
     - **Correlation Coefficient:** 0.34
     - **Interpretation:** There is a moderate positive correlation between the number of customers affected and the event duration. This indicates that events affecting more customers tend to last longer, although the relationship is moderate and **other factors may also play a significant role**.
   - **Demand Loss (MW) and Event Duration (hours):**
     - **Correlation Coefficient:** 0.15
     - **Interpretation:** There is a weak positive correlation between demand loss (MW) and event duration. This suggests that the relationship between the amount of demand loss and the duration of the event is weak, implying that **factors other than the duration of the event are likely more significant** in determining the extent of demand loss.
 
      
- **Distribution of Disturbances Over the Years**:
  - **Question**: How have the number of electrical disturbances changed over the years from 2019 to 2023?
  - **Analysis**: We visualize the number of disturbances reported each year to identify any trends or significant changes over time. This helps understand if disturbances are becoming more frequent, less frequent, or remaining consistent.
  - **Graph**: ![Distribution of Disturbances Over the Years](path/to/your/graph1.png)

- **Analysis of Disturbance Causes**:
  - **Question**: What are the most common causes of electrical disturbances?
  - **Analysis**: By categorizing and counting the causes of disturbances, we can determine the primary factors contributing to electrical issues. This can inform mitigation strategies and policies to address the most prevalent causes.
  - **Graph**: ![Analysis of Disturbance Causes](path/to/your/graph2.png)

- **Geographical Distribution of Disturbances**:
  - **Question**: Which regions in the US are most affected by electrical disturbances?
  - **Analysis**: Mapping the disturbances geographically allows us to identify hotspots and regions that are more prone to electrical issues. This spatial analysis can guide infrastructure improvements and targeted interventions.
  - **Graph**: ![Geographical Distribution of Disturbances](path/to/your/graph3.png)

- **Trend Analysis**:
  - **Question**: Are there any noticeable patterns or trends in the disturbances data over the selected period?
  - **Analysis**: We examine the data for patterns such as seasonal trends, correlations with external factors (e.g., weather events), and other recurring themes. This deeper analysis helps in understanding underlying causes and potential predictive factors.
  - **Graph**: ![Trend Analysis](path/to/your/graph4.png)



## How to Use

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/US_Electricity_Disturbances.git
    cd US_Electricity_Disturbances
    ```

2. **Install Required Packages**:
    Ensure you have Python 3.x installed. You can install the required packages using pip:
    ```bash
    pip install pandas numpy matplotlib seaborn plotly scipy jupyter
    ```

3. **Open the Notebooks**:
    Use Jupyter Notebook or JupyterLab to open and run the notebooks:
    ```bash
    jupyter notebook
    ```
    Navigate to the cloned repository folder and open the desired notebook.

4. **Run the Notebooks Sequentially**:
    - Start with `Data_Cleaning_US_Electricity_Disturbances.ipynb` to clean the data.
    - Proceed to `EDA_US_Electricity_Disturbances.ipynb` for exploratory data analysis.

## Requirements
- Python 3.x
- `pandas` for data manipulation
- `numpy` for numerical operations
- `matplotlib` and `seaborn` for static data visualization
- `plotly` for interactive data visualization
- `scipy` for statistical analysis
- Jupyter Notebook or JupyterLab for running the notebooks

## Data Source
The dataset used in this analysis is obtained from the [US Department of Energy](https://www.oe.netl.doe.gov/OE417_annual_summary.aspx). The data includes information on electrical disturbances reported across the US from 2019 to 2023, including the causes, locations, and impacts of these disturbances.

## Project Structure
- `Data_Cleaning_US_Electricity_Disturbances.ipynb`: Jupyter notebook containing the data cleaning process.
- `EDA_US_Electricity_Disturbances.ipynb`: Jupyter notebook containing the exploratory data analysis.

## License
This project is licensed under the MIT License.
