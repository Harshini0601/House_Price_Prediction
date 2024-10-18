# House_Price_Prediction and Visualization Project

This project involves exploratory data analysis (EDA) on a housing dataset using Python. The main objective is to understand the structure of the dataset, perform data processing, and visualize the relationships between different features to derive insights about house prices.

## Project Structure

- **`Housing.csv`**: The dataset used for the analysis, containing details about houses such as location, price, number of bedrooms, bathrooms, floors, etc.
- **`analysis.py`**: The main Python script where the data is processed and visualized.

## Dependencies

This project uses the following Python libraries:

- `pandas`: For data manipulation and analysis
- `matplotlib`: For generating plots and visualizations
- `seaborn`: For creating aesthetically pleasing statistical plots
- `numpy`: For numerical operations
- `scikit-learn`: For label encoding and other preprocessing

You can install these libraries by running:
```bash
pip install pandas matplotlib seaborn numpy scikit-learn
```

## Steps in the Analysis

### 1. **Data Loading and Overview**

- The dataset is loaded from a CSV file using `pandas`.
- First 5 records of the dataset are displayed using `dataset.head()`.
- The dimensions of the dataset are examined with `dataset.shape`.
- The types of variables (categorical, integer, float) are identified.

### 2. **Data Preprocessing**

- Categorical variables are identified using their data types.
- The dataset is one-hot encoded to convert categorical variables into numerical format for better analysis.
- The numerical dataset is extracted for correlation analysis.

### 3. **Exploratory Data Analysis (EDA)**

- **Heatmaps**: Correlation matrices are visualized using heatmaps to identify the relationships between features, including one-hot encoded features.
  
- **Bar Plots**: 
  - A bar plot shows the number of unique values in each categorical feature.
  - Another bar plot visualizes the distribution of the top categories for selected categorical features.
  
- **Histograms**: 
  - Distribution of house prices is shown using a histogram.
  
- **Scatter Plot**: Relationship between house area and other features is shown (needs minor correction, see "Issues & Fixes").
  
- **Pie Chart**: A pie chart displays the distribution of house locations in the dataset.
  
- **Box Plot**: House price distribution based on the number of bedrooms is shown using a box plot.

### 4. **Visualizations**

- **Heatmaps**: Show correlations between numerical features.
- **Bar Plots**: Visualize categorical feature distributions.
- **Histograms**: Plot the distribution of house prices.
- **Scatter Plot**: Shows the relationships between variables (e.g., area vs price).
- **Pie Chart**: Shows category distribution of locations.
- **Box Plot**: Displays house price distribution by the number of bedrooms.

## Issues & Fixes

### 1. **Scatter Plot Error**: 
In the line:
```python
sns.scatterplot(dataset['Area'], color='blue', marker='*')
```
The scatter plot requires two variables for plotting. It should be fixed like this:
```python
sns.scatterplot(x=dataset['Area'], y=dataset['Price'], color='blue', marker='*')
```

## How to Run

1. Clone this repository.
2. Ensure that all dependencies are installed using `pip`.
3. Place the `Housing.csv` file in the same directory as the script.
4. Run the script:
```bash
python analysis.py
```

## Future Improvements

- Use advanced machine learning algorithms for house price prediction.
- Perform feature engineering to improve model performance.
- Add more visualizations for deeper insights into feature interactions.

## License

This project is licensed under the MIT License.

--- 

