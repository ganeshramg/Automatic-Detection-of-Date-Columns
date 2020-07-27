# Automatic-Detection-of-Date-Columns
This project focuses on finding the presence of Date Columns in an unstructured data, with different date formats, and creates new columns that contains the difference in number of days between date columns, while taking two at a time.

## The logic:
1. Increments/Decrements the possibility of a column being a date column by trying out different methods like, looking for the presence of any month it, or presence of two '/' or dots, or '-' or even spaces. This also tries splitting the string using these delimiters.

2. Notices for column names, gets non_numerical columns, and continues with the first step for every column

3. After confirming the date columns based on the possibilities obtained, using **REGEX** every entry of a column in validated.

4. Finally the difference columns are created. If we have two dates, D1 and D2, we can get a column D2-D1 which gives us the difference in number of days. If we have 5 date columns, we get 10 difference columns, taking two at a time.

## Advantages:
1. Any invalid entry is not taken into consideration, and the correspoding row of the difference column becomes np.nan or NaT, which can then be dropped using pd.dropna() method.

2. Various date formats can be updated in a single regex expression to automate more unstructured data.

## How to run it:
1. Download the .ipynb file
2. Open it in Jupyter Notebook/Google Colab
3. Run all cells

## Requirements:
1. Anaconda 3 for Jupyter Notebook

# Thank You
