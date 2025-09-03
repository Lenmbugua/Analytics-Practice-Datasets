# 🧑‍💻 Data Professional Survey Analysis (Python)

> A clean, end-to-end data analysis project using Python and Jupyter Notebook.  
> This project explores a real survey of data professionals, uncovering salary trends, gender pay gaps, career switching patterns, and education insights — all documented with visualizations, code, and conclusions.


## 📄 Overview
This project analyzes survey data from data professionals to uncover trends in salaries, demographics, career transitions, and education. Using **Python**, **pandas**, **matplotlib**, and **seaborn**, we cleaned and explored the dataset to answer key business questions and present actionable insights.


## 🎯 Goals
- Understand salary patterns across job titles, education, and gender.
- Investigate how people break into data careers (career switching trends).
- Explore demographic distributions (gender, education, roles).
- Create clear, professional visualizations to communicate findings.



## 🛠️ Tools & Libraries
- Python 
- pandas
- matplotlib
- seaborn
- Jupyter Notebook



## 📂 Dataset
- **File**: Professional Survey Data.xlsx
- **Records**: ~603 survey responses
- **Columns of interest**:
  - Q1 - Which Title Best Fits your Current Role?
  - Q2 - Did you switch careers into Data?
  - `Q3 - Current Yearly Salary (in USD)
  - `Q9 - Male/Female?
  - `Q12 - Highest Level of Education
  - (plus other demographic and career-related fields)


## 🧹 Data Cleaning
- Removed empty/unnecessary columns.
- Handled missing values and inconsistent labels.
- Converted salary ranges (e.g., `106k-125k`) to average numeric salaries.
- Split role titles to remove trailing descriptors (e.g., "Data Scientist: ML/AI"` → `"Data Scientist"`).


## ❓ Questions Answered & Functions Used

Below are the key questions explored, along with the main pandas/matplotlib/seaborn functions we used:

1  What is the average, median, and count of salaries by job title? -used the function; groupby()`, `agg(['mean','median','count']) 
2 How does salary differ by education level? -used the function; groupby()`, `mean()`, `plt.bar`, `plt.barh 
3 Is there a gender pay gap controlling for role? -used the function; (['Role','Gender'])`, `mean()`, pivoting, `plt.bar`, `plt.pie 
4 What percentage of respondents switched careers into data? -used the function; value_counts(normalize=True)`, `plt.pie (donut) 
5 Which roles or backgrounds made entry easier or harder? -used the function; pd.crosstab()`, `sns.heatmap 
6 What is the distribution of salaries per role?  -used the function; sns.boxplot 
7 How does highest level of education vary across roles? -used the function; groupby()`, `count()`, stacked `plt.bar 
8 What is the gender distribution across data roles? -used the function; groupby()`, `size()`, `plt.bar`, `plt.pie 
9 Which industries or organization types employ the most data professionals? -used the function; value_counts()`, `plt.bar 
10 Are there regional differences in pay or roles? -used the function; groupby(['Country'])`, `mean()`, `plt.bar

### 🧰 Function Highlights
- **Data Cleaning**
  - drop()`, `dropna()`, `fillna()` — remove or replace missing values.
  - duplicated()`, `drop_duplicates()` — identify and remove duplicate rows.
  - str.replace()`, `str.split()` — clean and transform text fields.
  - pd.to_numeric(errors='coerce')` — safely convert strings to numbers.

- **Data Aggregation**
  - groupby()`, `agg()` — group data and compute summary stats.
  - value_counts(normalize=True)` — get counts or percentages for categories.
  - crosstab()` — build cross-tabulations for two categorical variables.

- **Visualization**
  - **Matplotlib**: plt.bar`, `plt.barh`, `plt.pie`, `plt.stem`, `plt.figure`, `plt.title`, `plt.xticks`, `plt.show`
  - **Seaborn**: sns.boxplot`, `sns.heatmap`, `sns.countplot`


## 📊 Key Analyses & Visualizations
1. **Salary Insights**
   - Average, median, and distribution of salaries by role.
   - Salary differences by education level.
   - Gender pay gap analysis controlling for role.
   - **Charts used**: bar charts, boxplots.

2. **Career Switching Trends**
   - Percentage of professionals who switched into data.
   - Entry difficulty compared across education levels and roles.
   - **Charts used**: donut charts, stacked bars.

3. **Demographics**
   - Gender distribution by role.
   - Highest education level by role.
   - Industry/organization type representation.
   - **Charts used**: horizontal bars, pie/donut charts.

4. **Combined Insights**
   - Roles with highest and lowest pay.
   - Education backgrounds associated with higher salaries.
   - Trends indicating easier vs. harder career transitions.


## 🧠 Insights
- Certain job titles (e.g., Data Scientists) consistently have higher average salaries.
- A noticeable gender pay gap exists in some roles, though it varies.
- Many professionals successfully transitioned into data from other careers.
- Higher education levels tend to correlate with higher salaries, but experience also plays a role.




