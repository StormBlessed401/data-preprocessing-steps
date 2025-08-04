# CSV Data Preprocessing Script

This repository contains a Python script for preprocessing CSV data before using it in machine learning or data analysis tasks. The script uses popular libraries like `pandas`, `numpy`, and `scikit-learn` to handle missing values, encode categorical features, scale numerical data, and prepare the dataset for modeling.

## What This Script Does

The preprocessing script covers the following steps:

1. **Load the Dataset**  
   Reads a CSV file into a pandas DataFrame.

2. **Basic Exploration**  
   Displays the shape, column names, data types, and summary statistics of the dataset.

3. **Handle Missing Values**  
   - Fills missing values with the column mean (can be changed to median or mode).
   - Optionally drops rows with missing data.

4. **Remove Duplicates**  
   Drops any duplicate rows from the dataset.

5. **Rename and Reorder Columns**  
   Renames columns and reorders them if needed.

6. **Change Data Types**  
   Converts columns to appropriate data types like `datetime` or `string`.

7. **Categorical Encoding**  
   - Label encodes a categorical column using `LabelEncoder`.
   - One-hot encodes another categorical column using `get_dummies`, with `drop_first=True` to prevent multicollinearity.

8. **Text Preprocessing**  
   Cleans a text column by:
   - Converting to lowercase
   - Removing non-letter characters
   - Removing extra spaces

9. **Scaling Numerical Features**  
   Applies standard scaling to numerical features using `StandardScaler`. This step transforms the features to have a mean of 0 and a standard deviation of 1.

10. **Train-Test Split**  
    Splits the dataset into training and testing sets using `train_test_split` from `sklearn`.

11. **Save Cleaned Data**  
    Exports the cleaned DataFrame to a new CSV file. The `index=False` argument ensures that row numbers are not saved as a separate column.

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn

Install dependencies using:

```bash
pip install pandas numpy scikit-learn
```

## How to Use

1. Replace `"your_file.csv"` in the script with the path to your actual CSV file.
2. Update column names (like `'age'`, `'gender'`, `'salary'`, `'target'`) to match those in your dataset.
3. Run the script using a Python IDE or terminal.
4. The cleaned dataset will be saved as `cleaned_dataset.csv` in the same directory.

## Notes

- This script is meant as a starting point. You may need to modify steps depending on your specific dataset and problem.
- Be careful when dropping missing values, especially if they are frequent.
- For more complex tasks like text classification, time series forecasting, or image data processing, additional preprocessing steps will be needed.
