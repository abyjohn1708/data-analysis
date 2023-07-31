# data-analysis
Title: Analysis of Employee Data in ABC Company

Introduction:
The dataset used in this analysis consists of employee information for ABC Company, with 458 rows and 9 columns. The goal of this analysis is to provide a detailed report and insights about the employees in each team, as well as address specific questions related to team distribution, positions, age groups, salary spending, and the correlation between age and salary.

Data Preprocessing:
- The dataset was loaded using pandas, and its dimensions were verified with `df.shape`.
- Missing values were checked for using `df.isnull().sum()`, revealing no missing values.
- To enhance data integrity, the 'Height' column was modified with random numbers between 150 and 180 using `np.random.randint()`.

Analysis of Employee Data:
1. Number of Employees in Each Team and Percentage Splitting:
   - The count of employees in each team was calculated using `df['Team'].value_counts()`.
   - The percentage splitting of employees in each team was derived by dividing the team counts by the total number of employees (`len(df)`) and multiplying by 100.
   - The results were displayed in a table format using `pd.concat()` and printed.

2. Employees Segregated by Positions:
   - The count of employees based on different positions was obtained using `df['Position'].value_counts()`.
   - The results were printed to provide an overview of the employee distribution across positions.

3. Most Common Age Group:
   - The age group with the highest number of employees was determined by finding the mode (most frequently occurring value) in the 'Age' column using `df['Age'].value_counts().idxmax()`.
   - The result was displayed as the most common age group.

4. Team and Position with High Salary Spending:
   - The team and position with the highest salary spending were identified by finding the row index with the maximum salary using `df['Salary'].idxmax()`.
   - The team and position information were extracted from the corresponding row using `df.loc[]`, and the result was printed.

5. Correlation between Age and Salary:
   - The correlation between age and salary was analyzed by creating a scatter plot using `plt.scatter()` with 'Age' on the x-axis and 'Salary' on the y-axis.
   - The plot was displayed with appropriate labels and a title using `plt.xlabel()`, `plt.ylabel()`, and `plt.title()`.

Conclusion:
In this analysis of the employee dataset for ABC Company, several insights were derived. The distribution of employees across teams was determined, along with the percentage splitting. The employees were also segregated based on different positions. The most common age group among employees was identified. Additionally, the team and position with the highest salary spending were determined. Finally, the correlation between age and salary was visualized. These findings provide valuable insights into the employee landscape within ABC Company, which can aid in decision-making and resource allocation.

Note: Please replace the file name `'PROJECT.csv.csv'` in the code with the correct file name/path for the dataset you are using.
