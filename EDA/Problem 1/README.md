### 🚢 Univariate Exploratory Data Analysis (EDA) on Titanic Dataset

Univariate analysis involves examining each variable in the dataset individually. This analysis helps understand the basic structure and distribution of the data. In the Titanic dataset, we focus on the following key variables:

1. **Survived**: Distribution of survival (0 = No, 1 = Yes)
   - **📊 Summary**: We count the number of passengers who survived and who did not, providing an overall survival rate.
   - **📈 Visualization**: A bar chart or pie chart can be used to illustrate the proportion of survivors and non-survivors.

2. **Pclass (Passenger Class)**: Distribution of ticket classes (1st, 2nd, 3rd)
   - **📊 Summary**: We analyze the frequency of passengers in each class.
   - **📈 Visualization**: A bar plot shows the number of passengers per class.

3. **Age**: Distribution of passenger ages
   - **📊 Summary**: We calculate measures such as mean, median, and standard deviation of passenger ages.
   - **📈 Visualization**: A histogram or a kernel density plot displays the age distribution.

4. **Sex**: Distribution of genders
   - **📊 Summary**: We count the number of male and female passengers.
   - **📈 Visualization**: A bar chart illustrates the gender distribution.

5. **Fare**: Distribution of fare prices
   - **📊 Summary**: We calculate summary statistics like mean, median, and standard deviation of fare prices.
   - **📈 Visualization**: A histogram or box plot can show the distribution of fares.

6. **SibSp (Siblings/Spouses Aboard)**: Distribution of the number of siblings/spouses aboard
   - **📊 Summary**: We count the occurrences of each number of siblings/spouses.
   - **📈 Visualization**: A bar chart represents the distribution of siblings/spouses.

7. **Parch (Parents/Children Aboard)**: Distribution of the number of parents/children aboard
   - **📊 Summary**: We count the occurrences of each number of parents/children.
   - **📈 Visualization**: A bar chart shows the distribution of parents/children.

### 🌐 Multivariate Exploratory Data Analysis (EDA) on Titanic Dataset

Multivariate analysis examines relationships between two or more variables simultaneously. This analysis helps understand interactions and dependencies between variables in the Titanic dataset:

1. **Survival Rate by Passenger Class**
   - **🔍 Analysis**: We examine how survival rates differ across the three passenger classes.
   - **📊 Visualization**: A stacked bar chart or grouped bar chart illustrates survival rates by class.

2. **Survival Rate by Gender**
   - **🔍 Analysis**: We investigate the survival rates for male and female passengers.
   - **📊 Visualization**: A bar chart or grouped bar chart compares survival rates by gender.

3. **Survival Rate by Age**
   - **🔍 Analysis**: We explore the relationship between age and survival, potentially categorizing age into bins.
   - **📊 Visualization**: A box plot or violin plot shows the age distribution of survivors and non-survivors.

4. **Fare Distribution by Passenger Class**
   - **🔍 Analysis**: We analyze how fare prices vary across different classes.
   - **📊 Visualization**: A box plot or violin plot compares fare distributions for each class.

5. **Survival Rate by Family Size (SibSp + Parch)**
   - **🔍 Analysis**: We examine if family size impacts survival rates.
   - **📊 Visualization**: A bar chart represents survival rates for different family sizes.

### 🔗 Correlation Analysis on Titanic Dataset

Correlation analysis involves examining the relationships between numerical variables to understand how they change together. For the Titanic dataset, we focus on:

1. **Correlation Matrix**
   - **🔍 Analysis**: We compute the correlation coefficients between numerical variables such as Age, Fare, SibSp, and Parch.
   - **📊 Visualization**: A heatmap displays the correlation matrix, highlighting strong and weak correlations.

2. **Age and Fare Correlation**
   - **🔍 Analysis**: We investigate the correlation between age and fare to see if older passengers paid more for their tickets.
   - **📊 Visualization**: A scatter plot shows the relationship between age and fare, potentially with a trend line.

3. **SibSp and Parch Correlation**
   - **🔍 Analysis**: We explore the relationship between the number of siblings/spouses and parents/children aboard.
   - **📊 Visualization**: A scatter plot displays the correlation between SibSp and Parch.
