# Data Science Salary Analysis

![Data Analysis](https://img.shields.io/badge/Data-Analysis-green)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-blue)
![Python](https://img.shields.io/badge/Python-3.9-yellow)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📊 Project Overview

This project analyzes a comprehensive dataset of data science salaries to understand the factors affecting compensation in the field and to build a predictive model. The analysis explores correlations between salaries and various features such as job titles, experience levels, company size, location, and remote work status.

## 🔍 Dataset Description

The dataset (`salaries.csv`) contains over 44,000 unique data science job records (after removing duplicates) with the following attributes:

- **work_year**: Year the salary was paid (2020-2025)
- **experience_level**: Experience level in the job (EN, MI, SE, EX)
- **employment_type**: Type of employment (FT, PT, CT, FL)
- **job_title**: Role worked during the year
- **salary**: Salary amount in the local currency
- **salary_currency**: Currency of the salary paid
- **salary_in_usd**: Salary converted to USD
- **employee_residence**: Country of residence of the employee
- **remote_ratio**: Remote work percentage (0, 50, 100)
- **company_location**: Country of the employer
- **company_size**: Size of the employer company (S, M, L)

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.9 or higher
- Jupyter Notebook/Lab or Google Colab

### Required Libraries
```bash
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install scikit-learn
pip install catboost
pip install shap
pip install feature-engine
pip install autoviz
```

### How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/mviswan12/data-science-salary-analysis.git
   cd data-science-salary-analysis
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook:
   ```bash
   jupyter notebook Data_Science_Salary_Analysis.ipynb
   ```

## 📈 Analysis Performed

### Data Preprocessing
- Removed duplicate entries (44,858 duplicates identified)
- Verified no missing values across all columns
- Applied rare label encoding for categorical variables
- Standardized categorical columns for consistent analysis

### Exploratory Data Analysis (EDA)
1. **Distribution Analysis**
   - Employment type distribution
   - Salary distribution across different job roles
   - Remote work ratio analysis
   - Company size distribution

2. **Bar Plots**
   - Top 10 job titles by frequency
   - Top company locations for data science jobs
   - Company size distribution 
   - Highest paying job titles (2025)

3. **Salary Trends**
   - Distribution of salaries by year (violin plot)
   - Salary variations by experience level
   - Salary differences by company size
   - Remote work impact on compensation

4. **Correlation Analysis**
   - Relationship between original salary and USD conversion
   - Impact of company location on salary
   - Employment type correlation with compensation
   - Experience level influence on salary

### Predictive Modeling
- Built a CatBoost regression model to predict salaries in USD
- Processed categorical features with appropriate encodings
- Applied train-test split (50-50) for model validation
- Performed error analysis with residual plots
- Implemented SHAP analysis for model interpretation

## 🔑 Key Findings

1. **Salary Trends**:
   - The average predicted salary was $150,813.6 per year, closely matching the actual average of $151,901.9
   - Strong salary growth observed from 2020 to 2025
   - Director-level positions in Machine Learning and AI command the highest salaries

2. **Most Important Salary Factors**:
   - The original salary amount is the strongest predictor of USD salary (logical relationship)
   - Salary currency has significant impact on final compensation
   - Experience level plays a crucial role in determining pay
   - Company size has moderate influence on compensation

3. **Job Title Analysis**:
   - Data Scientist, Data Engineer, and Data Analyst are the most common roles
   - Director of Machine Learning, Head of AI, and specialized AI roles command premium salaries
   - Technical leadership positions show higher compensation than individual contributor roles

4. **Geographic Insights**:
   - US dominates the data science job market by a large margin
   - Remote work is increasingly common, with significant representation in the dataset
   - Company location has more impact on salary than employee residence

5. **Model Performance**:
   - The CatBoost model achieved an RMSE of 5,245.4 USD/year on test data
   - 93.2% improvement over the baseline prediction (mean value)
   - Error distribution shows high concentration near zero, indicating good model performance

## 📊 Visualizations

The project includes multiple visualization types:
- Employment type distribution plots
- Salary histograms by various factors
- Job title frequency bar charts
- Top company locations charts
- Highest paying job titles visualization
- Salary distribution by year (violin plots)
- Error distribution histograms
- SHAP value analysis plots for feature importance

## 🔄 Future Work

1. Include more historical data to better identify long-term salary trends
2. Incorporate industry-specific information to analyze salary variations by sector
3. Develop more granular geographic analysis (city-level instead of country-level)
4. Build interactive dashboards for exploring salary data by various dimensions
5. Analyze skill-based compensation differences by extracting skills from job titles
6. Create specialized models for different geographic regions or job categories
7. Incorporate economic indicators to adjust for cost of living differences
8. Analyze career progression paths and associated salary growth

## 🔗 References

- Glassdoor Salary Data Standards
- Bureau of Labor Statistics Occupational Employment Statistics
- Data Science Industry Compensation Reports

## 👤 Author

- Mega Viswanathan

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

For questions or feedback, please open an issue or contact me at [megavishy@gmail.com](mailto:megavishy@gmail.com).
