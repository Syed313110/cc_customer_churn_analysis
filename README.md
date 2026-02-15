# Credit Card Customer Churn Analysis

**Credit Card Customer Churn Analysis** project analyses a dataset of credit card customers to understand which factors contribute to customer churn (when a customer leaves the bank). The goal is to provide actionable insights that help financial institutions identify high-risk customers, predict churn, and implement retention strategies.

The analysis includes:

* Exploratory Data Analysis (EDA) to understand customer demographics and behaviour
* Hypothesis testing to validate patterns influencing churn
* Predictive modeling to estimate churn probability
* Interactive dashboards in Power BI to communicate insights to both technical and non-technical stakeholders

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
The dataset used in this project is the BankChurners.csv dataset from Kaggle:

https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers?select=BankChurners.csv

Dataset overview:

* Size: 10,127 customer records
* Columns: 23 features including demographics, credit card usage, tenure, credit limits, income categories, and churn status.
* Objective: Analyse factors contributing to customer churn and develop predictive insights to improve customer retention.
* Size & Complexity: Dataset is manageable for processing in Python and visualising in Power BI. Data is anonymised and requires minimal transformation.


## Business Requirements
I am a contracted a Business Analyst for the credit card company and my job is to utilise this project to address the following business requirements:

* Identify high-risk churn customers to enable proactive retention strategies.
* Analyse patterns and relationships between customer attributes and churn behaviour.
* Predict churn probabilities to support decision-making for targeted campaigns.
* Provide interactive dashboards for business stakeholders to explore customer trends dynamically.


## Hypothesis and how to validate?
### H1: Customer Tenure and Churn

* Research Hypothesis (H1):
Customers with shorter tenure (measured by Months_on_book) are more likely to churn compared to customers with longer tenure.

* Null Hypothesis (H0):
There is no statistically significant difference in tenure between customers who churn and those who remain.

* Rationale:
Customer tenure reflects relationship strength and engagement with the bank. Customers in the early stages of their lifecycle may not yet be fully integrated into the bank’s ecosystem, increasing their likelihood of attrition. Identifying this relationship allows the bank to improve onboarding and early retention strategies.

### H2: Credit Utilisation and Churn

* Research Hypothesis (H2):
Customers with lower credit utilisation ratios are more likely to churn than customers with higher utilisation ratios.

* Null Hypothesis (H0):
There is no statistically significant relationship between credit utilisation ratio and customer churn.

* Rationale:
Credit utilisation (calculated as Total_Revolving_Bal divided by Credit_Limit) measures the proportion of available credit being used. High utilisation may indicate financial stress or dependency on credit, meaning, their reliance on credit is much more needed hence they cannot break out of the borrowing-repaying-borrowing cycle. 

### H3: Income Category and Churn

* Research Hypothesis (H3):
Churn rates differ significantly across income categories.

* Null Hypothesis (H0):
There is no association between income category and customer churn.

* Rationale:
Income level may influence spending behaviour, credit dependency, and financial stability. Identifying income-based churn patterns allows the bank to design targeted retention campaigns tailored to different economic segments.


## Project Plan
###High-level Steps:

Data Collection:
* Download dataset from Kaggle.

ETL Pipeline:

Extract: 
* Load CSV in Python (Pandas).

Transform: 
* Handle missing values and duplicates.
* Encode categorical variables (e.g., Gender, Income_Category).
* Feature engineering: churn label binarisation, credit utilisation ratio, transaction averages.

Load: 

* Cleaned data exported for analysis and Power BI dashboarding.
* Exploratory Data Analysis (EDA):
* Descriptive statistics, correlations, distributions, outliers.

Hypothesis Testing:

* Statistical tests (t-tests, chi-square) to validate assumptions.

Machine Learning:

* Predict churn with Logistic Regression, Decision Trees, Random Forest.
* Evaluate models (Accuracy, F1-score, ROC-AUC).

Interactive Dashboard Development:

* Visualisation of key metrics, segmentation, churn probabilities.

Interpretation & Recommendations:

* Provide business insights with narrative storytelling.

Research Methodology Justification:

* EDA helps understand patterns in data before modelling.
* Statistical tests provide validation of hypotheses.
* Classification algorithms are suitable for churn prediction (binary target).
* Interactive dashboards allow non-technical stakeholders to explore the data.

## The rationale to map the business requirements to the Data Visualisations
To effectively address the business requirements of this project, each visualisation was carefully chosen to provide clear insights into customer churn patterns.

To identify factors contributing to customer churn, correlation heatmaps and pairplots were used. These visualisations allow the team to observe relationships between numerical features, such as credit limit, tenure, and balance, and churn outcomes. By examining these correlations, potential predictors of churn can be highlighted for further analysis.

To assess churn rates across different demographic groups, bar charts and stacked bar charts were implemented. These charts provide a simple and intuitive way to compare churn percentages across categories like gender, marital status, education level, and credit card type, making patterns and trends easily interpretable by both technical and non-technical stakeholders.

The impact of customer tenure and transaction behaviour on churn was visualised using box plots and violin plots. These plots reveal the distribution of features like tenure, average transaction amount, and total transactions for churned versus retained customers, highlighting differences in customer behaviour that may influence churn.

Where temporal data was available, line charts and area charts were employed to visualise monthly or periodic trends in churn. These visualisations help to detect seasonality or specific time periods with higher churn, providing actionable insights for targeted interventions.

For customer segmentation and risk analysis, scatter plots and bubble charts were used. These visualisations combine multiple features, such as balance, credit utilization, and tenure, to identify clusters of high-risk versus low-risk customers, which is particularly useful for planning targeted retention strategies.

Finally, an interactive dashboard in Power BI was created to allow stakeholders to dynamically explore the data. Filters and slicers enable users to view predicted churn probabilities and explore patterns by age, card type, or region. This interactive approach ensures that insights are accessible to both business decision-makers and data analysts, making the findings actionable and aligned with the project’s core objectives.
## Analysis techniques used
Descriptive Statistics: 
* Mean 
* Median
* Standard deviation
* Percentiles

Visualisations: 

* Histograms
* Boxplots
* Scatterplots
* Bar charts 
* Heatmaps

Hypothesis Testing:

* Chi-square for categorical associations (e.g., income vs churn).
* T-tests for continuous variables (e.g., tenure, credit utilisation).

Machine Learning Models:

* Logistic Regression, Random Forest, Decision Tree (classification).

Evaluation metrics: Confusion matrix, F1-score, ROC-AUC.

Limitations & Alternatives:

* Imbalanced data handled with class weighting / SMOTE.
* Outliers and skewed distributions addressed with log transformation or winsorisation.

Generative AI Usage:
* Assisted with code snippets, visualisation templates, hypothesis ideas, and dashboard design.

## Ethical considerations
* Data is anonymised; no personal identifiers are exposed. 
* Bias potential exists in features such as Age, Income, Gender.

Mitigation:

* Feature selection ensures sensitive attributes are handled responsibly.

Transparency in model evaluation to avoid unfair bias.
## Dashboard Design
### Planned Dashboard Pages

#### 1. Overview Page:

* Total customers, churn rate, average credit limit.
* KPI cards with slicers for Gender, Income, Card Category.

#### 2. Demographics Page:
* Churn by age, income, education.
* Histograms, stacked bar charts.

#### 3. Credit Usage Page:

* Credit utilisation ratio vs churn.
* Boxplots and scatterplots.

#### 4. Transaction Analysis Page:

* Transaction patterns and churn correlation.
* Time series / bar charts of Total_Trans_Amt.

#### 5. Predictive Insights Page:

* Input filters for age, income, tenure, relationships.
* Display predicted churn probability using ML model.

#### Communication Strategy:

* KPIs for executives.
* Detailed charts for analysts.
* Clear legends, tooltips, and slicers for interactive exploration.

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
| Library      | Purpose                       | Example Usage                                                |
| ------------ | ----------------------------- | ------------------------------------------------------------ |
| Pandas       | Data cleaning, transformation | `df = pd.read_csv('BankChurners.csv')`                       |
| Numpy        | Calculations, arrays          | `np.log(df['Credit_Limit'])`                                 |
| Matplotlib   | Static plotting               | `plt.hist(df['Customer_Age'])`                               |
| Seaborn      | Advanced plots                | `sns.boxplot(x='Attrition_Flag', y='Credit_Limit', data=df)` |
| Scikit-learn | ML models                     | `LogisticRegression().fit(X_train, y_train)`                 |
| Power BI     | Dashboarding                  | Interactive visuals, slicers, KPIs                           |



## Credits 

* BankChurners dataset: Kaggle
* Code snippets from Scikit-learn and Seaborn documentation
* Dashboard design inspiration from Power BI online tutorials

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
Thanks to CI mentors, Slack community, and Kaggle contributors for guidance and dataset sharing.
