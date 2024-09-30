<h2><span style="color: red;"> 🛑 Patients in the clinical trial </span></h2> 
- Summary<br>
- Address issues within the dataset combine and make documents<br>

### 1.🟨 Write a summary for your data 
- This is a dataset about 503 patients storing their records and also a treatment/treatment_cuts of which 280 + 70 = 350 patients participated in a clinical trial. 
- None of the patients were using Novodra (a popular injectable insulin) or Auralin (the oral insulin being researched) as their primary source of insulin before.
- All were experiencing elevated HbA1c levels(Sugar level in desi language).
- All 350 patients were treated with Novodra and Auralin to record the difference in change in start and end of the trails.
- Data about patients feeling some adverse effects after the trails were also recorded.

### 2.🟨 Colomn Description 
- **<span style="color: red;">💥 Table</span>** - `patients`<br>
1. **patient_id**: Unique identifier for each patient.
2. **assigned_sex**: Sex assigned to the patient at birth (e.g., male, female, other).
3. **given_name**: First name of the patient.
4. **surname**: Last name (family name) of the patient.
5. **address**: Street address where the patient resides.
6. **city**: City where the patient resides.
7. **state**: State or province where the patient resides.
8. **zip_code**: Postal code for the patient's address.
9. **country**: Country where the patient resides.
10. **contact**: Contact information for the patient, typically a phone number or email address.
11. **birthdate**: Date of birth of the patient.
12. **weight**: Weight of the patient, usually measured in kilograms or pounds.
13. **height**: Height of the patient, usually measured in centimeters or inches.
14. **bmi**: Body Mass Index (BMI) of the patient, a value derived from the weight and height.

- **<span style="color: red;">💥 Table</span>** - `treatments`<br>
1. **given_name**: First name of the patient.
2. **surname**: Last name (family name) of the patient.
3. **auralin**:  Dosage of the medication Auralin prescribed to the patient, measured in units (e.g., 22u - 30u).
4. **novodra**:  Dosage of the medication Novodra prescribed to the patient, measured in units (e.g., 22u - 30u).
5. **hba1c_start**: Initial HbA1c level (percentage) at the beginning of the monitoring period.
6. **hba1c_end**: Final HbA1c level (percentage) at the end of the monitoring period.
7. **hba1c_change**: Change in HbA1c level (percentage) from the start to the end of the monitoring period.

- **<span style="color: red;">💥 Table</span>** - `treatments_cuts`<br>
1. **given_name**: First name of the patient.
2. **surname**: Last name (family name) of the patient.
3. **auralin**:  Dosage of the medication Auralin prescribed to the patient, measured in units (e.g., 22u - 30u).
4. **novodra**:  Dosage of the medication Novodra prescribed to the patient, measured in units (e.g., 22u - 30u).
5. **hba1c_start**: Initial HbA1c level (percentage) at the beginning of the monitoring period.
6. **hba1c_end**: Final HbA1c level (percentage) at the end of the monitoring period.
7. **hba1c_change**: Change in HbA1c level (percentage) from the start to the end of the monitoring period.

- **<span style="color: red;">💥 Table</span>** - `adverse_reactions`<br>
1. **given_name**: First name of the patient.
2. **surname**: Last name (family name) of the patient.
3. **adverse_reaction**: Description of any negative or unintended reactions experienced by the patient, typically as a result of medication or treatment.

### 3.🟨 Add any additional information
- Insulin resistance varies person to person, which is why both starting median daily dose and ending median daily dose are required, i.e., to calculate change in dose.
- It is important to test drugs and medical products in the people they are meant to help. 
- People of different age, race, sex, and ethnic group must be included in clinical trials mmoreover this diversity is reflected in the patients table.

### 4.🟨 Issues with the dataset 🛑
#### ⭐️ Step 1 Dirty Data
- Duplicated data 
- Missing Data 
- Corrupt Data
- Inaccurate Data

## Documented Description 🌫️
- **<span style="color: red;">💥 Table</span>** - `patients`<br>
            1. Have no Duplicate rows and colomn.<br>
            2. Have 12 missing or null values data in following columns.<br>
                - `address`<br>
                - `city`<br> 
                - `state`<br>	 
                - `zip_code`<br>	
                - `country`<br>	
                - `contact`<br>
            3. Following Colomns have corrupted data entered.<br>
                - `zip_code` : Some time 4-digit of zip code is entered.<br>	
                - `contact` : Number and email address is provided combine(e.g formate : 951-719-9170email@gmail.com).<br>
                - `state` : State in some colomn provided as abreviated (e.g NewYork : NY).<br>
            4. Inacurrate data:<br>
                - `zip_code` : Wrong datatype for this colomn is selected.<br>
                - `weight` : The weight has not been entered accurately have outliers.<br>
                - `height` : The height has also not been entered accurately have outliers.<br>
            
- **<span style="color: red;">💥 Table</span>** - `treatments`<br>
            1. Have 1 Duplicate row.<br>
            2. Have 109 missing or null values data in following columns.<br>
                - `hba1c_change`<br>
            3. Following Colomns have corrupted data entered.<br>
                - `auralin` : Some times ( '-' ) is entered in place where patients dont use auralin.<br>
                - `novodra` : Some times ( '-' ) is entered in place where patients dont use novodra.<br>
            4. Inacurrate data:<br>
                - `auralin` : The dose of the medicine written with the unit `u`.<br>
                - `novodra` : The dose of the medicine written with the unit `u`.<br>

- **<span style="color: red;">💥 Table</span>** - `treatments_cut`<br>
            1. Have 0 Duplicate row.<br>
            2. Have 28 missing or null value in data.<br>
                - `hba1c_change`<br>
            3. Following Colomns have corrupted data entered.<br>
                - `auralin` : Some times ( '-' ) is entered in place where patients dont use auralin.<br>
                - `novodra` : Some times ( '-' ) is entered in place where patients dont use novodra.<br>
            4. Inacurrate data:<br>
                - `auralin` : The dose of the medicine written with the unit `u`.<br>
                - `novodra` : The dose of the medicine written with the unit `u`.<br>

- **<span style="color: red;">💥 Table</span>** - `adverse_reactions`<br>
            1. Have 0 Duplicate row.<br>
            2. Have 0 missing or null value in data.<br>
            3. No corrupted data entered.<br>
            4. No inacurrate data:<br>

#### ⭐️ Step 2 Messy Data  
   - Structural issues ,Each variable forms a single column.
   - Each observation forms a row.
   - Each observational unit forms a table.

## Documented Description 🌫️
- **<span style="color: red;">💥 Table</span>** - `patients`<br>
            1.  Structural issues:<br>
                - `contact` : Number and email address is provided combine(e.g formate : 951-719-9170email@gmail.com). <br>
                - `address`	,`city`	 ,`state` ,`country` can be in one separate table.<br>

- **<span style="color: red;">💥 Table</span>** - `treatments`<br>
            1.  Structural issues:<br>
                - `auralin` and `novodra` not in a single table.<br>
       
- **<span style="color: red;">💥 Table</span>**- `treatments_cut`<br>
            1.  Structural issues:<br>
                - `auralin` and `novodra` not in a single table.<br>

- **<span style="color: red;">💥 Table</span>** - `adverse_reactions`<br>

### 5.🟨 Providing solutions of issues within the dataset 🛑
- **<span style="color: red;">💥 Table</span>** - `patients`<br>
            1. **No Duplicate Rows and Columns:**<br>
                - Ensure the table has no duplicate rows and columns by using the Pandas functions `drop_duplicates()` for rows and checking column names for duplicates.<br>
            2. **Missing or Null Values:**<br>
                - Columns with missing values: `address`, `city`, `state`, `zip_code`, `country`, `contact`<br>
                - Handle missing values using methods like `fillna()` or `dropna()` based on the context.<br>
            3. **Corrupted Data:**<br>
                - **`zip_code`**: Ensure all zip codes are 5 digits long by applying a transformation to add leading zeros if necessary.<br>
                - **`contact`**: Split combined contact information into separate `phone_number` and `email` columns using string manipulation functions.<br>
                - **`state`**: Standardize state names by converting abbreviations to full state names using a mapping dictionary.<br>
            4. **Inaccurate Data:**<br>
                - **`zip_code`**: Correct the datatype by converting the column to string type using `astype(str)`.<br>
                - **`weight`**: Identify and handle outliers by using statistical methods such as Z-scores or IQR to filter out anomalous values.<br>
                - **`height`**: Similarly, identify and handle outliers using statistical methods to ensure accurate entries.<br>
 
- **<span style="color: red;">💥 Table</span>** - `treatments`<br>
            1. **Duplicate Row:**<br>
                - Remove duplicate rows using `drop_duplicates()`.<br>
            2. **Missing or Null Values:**<br>
                - Column with missing values: `hba1c_change`<br>
                - Handle missing values by either filling them with an appropriate statistic (mean, median) or removing the rows if it does not impact analysis significantly.<br>
            3. **Corrupted Data:**<br>
                - **`auralin`**: Replace ( - ) with `NaN` or `0` to indicate no usage.<br>
                - **`novodra`**: Replace ( - ) with `NaN` or `0` to indicate no usage.<br>
            4. **Inaccurate Data:**<br>
                - **`auralin`**: Remove the unit `u` from dosage values and ensure the column is numeric using string replacement and conversion.<br>
                - **`novodra`**: Similarly, remove the unit `u` from dosage values and ensure the column is numeric.<br>

- **<span style="color: red;">💥 Table</span>** - `treatments_cut`<br>
            1. **No Duplicate Rows:**<br>
               - Ensure the table has no duplicate rows.<br>
            2. **Missing or Null Values:**<br>
               - Column with missing values: `hba1c_change`<br>
               - Handle missing values using methods like `fillna()` or `dropna()` based on the context.<br>
            3. **Corrupted Data:**<br>
                - **`auralin`**: Replace ( - ) with `NaN` or `0` to indicate no usage.
                - **`novodra`**: Replace ( - ) with `NaN` or `0` to indicate no usage.
            4. **Inaccurate Data:**<br>
                - **`auralin`**: Remove the unit `u` from dosage values and ensure the column is numeric using string replacement and conversion.<br>
                - **`novodra`**: Similarly, remove the unit `u` from dosage values and ensure the column is numeric.<br>

- **<span style="color: red;">💥 Table</span>** - `adverse_reactions`<br>
            1. **No Duplicate Rows:**<br>
                - Ensure the table has no duplicate rows.<br>
            2. **No Missing or Null Values:**<br>
                - Verify that there are no missing or null values.<br>
            3. **No Corrupted Data:**<br>
                - Confirm that all data entries are correct and uncorrupted.<br>
            4. **No Inaccurate Data:**<br>
                - Verify the accuracy of all data entries.<br>
