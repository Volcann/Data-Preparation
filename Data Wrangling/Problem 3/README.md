<h2><span style="color: red;"> 🛑 Iris Dataset Analysis </span></h2>
- Summary<br>
- Address issues within the dataset combine and make documents<br>

### 1.🟨 Write a summary for your data 
- This is a dataset consisting of 150 records of iris flowers, with each record detailing the measurements of four features (sepal length, sepal width, petal length, and petal width) and the species of the iris flower.
- The dataset contains three species: Iris-setosa, Iris-versicolor, and Iris-virginica, with 50 records for each species.
- The data is commonly used for testing various machine learning algorithms and data visualization techniques.

### 2.🟨 Column Description 
- **<span style="color: red;">💥 Table</span>** - `iris`<br>
1. **sepal_length**: Length of the sepal, measured in centimeters.
2. **sepal_width**: Width of the sepal, measured in centimeters.
3. **petal_length**: Length of the petal, measured in centimeters.
4. **petal_width**: Width of the petal, measured in centimeters.
5. **species**: Species of the iris flower (Iris-setosa, Iris-versicolor, Iris-virginica).

### 3.🟨 Add any additional information
- The Iris dataset is well-structured and has no missing values.
- It is important for exploratory data analysis (EDA) and serves as a benchmark for machine learning models due to its simplicity and well-defined classes.
- The diversity of the species and the clear distinctions between the flower measurements make it ideal for classification problems.

### 4.🟨 Issues with the dataset 🛑
#### ⭐️ Step 1 Dirty Data
- Duplicated data
- Corrupt Data
- Inaccurate Data

## Documented Description 🌫️
- **<span style="color: red;">💥 Table</span>** - `iris`<br>
            1. **Duplicate Rows:**<br>
                - Ensure the table has no duplicate rows by using the Pandas function `drop_duplicates()`.<br>
            2. **Corrupted Data:**<br>
                - **`species`**: Ensure all species names are correctly labeled without typographical errors.<br>
            3. **Inaccurate Data:**<br>
                - **`sepal_length`, `sepal_width`, `petal_length`, `petal_width`**: Check for outliers that may indicate measurement errors or data entry mistakes.<br>

#### ⭐️ Step 2 Messy Data  
   - Structural issues, each variable forms a single column.
   - Each observation forms a row.
   - Each observational unit forms a table.

## Documented Description 🌫️
- **<span style="color: red;">💥 Table</span>** - `iris`<br>
            1. **Structural issues:**<br>
                - Verify that each column represents a single variable and each row represents a single observation.<br>

### 5.🟨 Providing solutions of issues within the dataset 🛑
- **<span style="color: red;">💥 Table</span>** - `iris`<br>
            1. **No Duplicate Rows:**<br>
                - Ensure the table has no duplicate rows by using the Pandas function `drop_duplicates()`.<br>
            2. **Corrupted Data:**<br>
                - **`species`**: Verify and correct species names if there are any typographical errors.<br>
            3. **Inaccurate Data:**<br>
                - **`sepal_length`, `sepal_width`, `petal_length`, `petal_width`**: Identify and handle outliers by using statistical methods such as Z-scores or IQR to filter out anomalous values.<br>
