<h2><span style="color: red;"> 🛑 Titanic dataset </span></h2> 
- Summary<br>
- Address issues within the dataset combine and make documents<br>

### 1. 🟨 Summary of data
- **The Titanic Tragedy Dataset**
- The RMS Titanic set sail on its maiden voyage in 1912, only to become infamous for its tragic sinking. This dataset provides insights into the passengers aboard the ill-fated ship.
- **Dataset Overview**: Contains information about 891 passengers, including their survival status.
- **Survival Statistics**: Of the 891 passengers, 549 did not survive, while 342 survived the disaster.
- **Passenger Information**: The dataset includes various details about the passengers, such as their age, class, and ticket information, providing a glimpse into the demographics and circumstances of those on board.

### 2. 🟨 Column Description
- **<span style="color: red;">💥 Table</span>** - `titanic_dataset`<br>
  - **PassengerId**: Unique identifier for each passenger.
  - **Survived**: Survival status (0 = No, 1 = Yes).
  - **Pclass**: Passenger class (1, 2, or 3), indicating the level of luxury and accommodation on the ship.
  - **Name**: Name of the passenger (first name ,last name ,nickname as well).
  - **Sex**: Gender of the passenger (male or female).
  - **Age**: Age of the passenger at the time of the voyage.
  - **SibSp**: Number of siblings or spouses aboard the Titanic.
  - **Parch**: Number of parents or children aboard the Titanic.
  - **Ticket**: Ticket number assigned to the passenger.
  - **Fare**: Amount paid for the ticket.
  - **Cabin**: Cabin number where the passenger stayed (if available).
  - **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

### 3. 🟨 Add any additional information
- **Survival Rate**: Provides insights into survival rates across different passenger classes and demographics.

### 4. 🟨 Issues with the Dataset 🛑
#### ⭐️ Step 1: Dirty Data
- **Duplicated Data**: 
  - The dataset may contain duplicate records, which can skew analysis and results.
- **Missing Data**: 
  - Some columns have missing values (e.g., `Age`, `Cabin`, `Embarked`), which need to be handled to ensure completeness.
- **Corrupt Data**: 
  - Entries like `NaN` in `Age`, `Cabin`, or `Embarked` might indicate data corruption or incomplete data collection.
- **Inaccurate Data**: 
  - Potential inaccuracies in fields like `Fare`, `Age`, or `Cabin` could impact the analysis.

#### ⭐️ Step 2: Messy Data
- **Structural Issues**: 
  - Ensure that each variable (column) is clearly defined and correctly placed in its respective column.
  - Each observation (row) should be distinct and correctly formatted.
  - The dataset should be organized into a single table where each column represents a specific variable, each row represents an observation, and the table contains the entire dataset.

### 5. 🟨 Providing Solutions to Issues within the Dataset 🛑
- **<span style="color: red;">💥 Table</span>** - `titanic_dataset`<br>
1. **Duplicated Data**:
   - **Solution**: Identify and remove duplicate rows. Use data processing tools to check for duplicates and eliminate them. In Python with Pandas, you can use:
     ```python
     titanic_dataset = titanic_dataset.drop_duplicates()
     ```

2. **Missing Data**:
   - **Solution**:
     - **Imputation**: Fill missing values with appropriate values (e.g., median for numerical columns, mode for categorical columns). For `Age`, you might use the median or mean of the column. For categorical data like `Embarked`, you could use the mode.
       ```python
       titanic_dataset['Age'].fillna(titanic_dataset['Age'].median(), inplace=True)
       titanic_dataset['Embarked'].fillna(titanic_dataset['Embarked'].mode()[0], inplace=True)
       ```
     - **Deletion**: Remove rows or columns with excessive missing data if imputation is not feasible or if it would introduce significant bias.


3. **Corrupt Data**:
   - **Solution**: Identify and address anomalies or incorrect values.
     - **Check and Correct Errors**: For columns like `Fare`, ensure there are no negative values or extreme outliers unless they are valid. 
       ```python
       titanic_dataset = titanic_dataset[titanic_dataset['Fare'] >= 0]
       ```
     - **Standardization**: Ensure consistent formatting (e.g., currency symbols removed from `Fare` values).

4. **Inaccurate Data**:
   - **Solution**: Validate data accuracy by cross-checking with reliable sources or domain knowledge.
     - **Consistency Checks**: Verify that values make sense in the context (e.g., `Age` should be within a reasonable range).
     - **Manual Review**: For critical columns, conduct a manual review or perform data validation checks to catch inaccuracies.

5. **Structural Issues**:
   - **Solution**:
     - **Ensure Proper Column and Row Structure**: Verify that each column represents a unique variable and each row represents a single observation.
     - **Normalization**: If any columns contain nested data or multiple values, normalize them into separate columns or tables as needed.
     - **Consistency**: Check for consistency in data types across columns and ensure no mixed types within a single column.
