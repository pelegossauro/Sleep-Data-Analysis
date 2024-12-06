README - Health Sleep Statistics Analysis
Overview
This project involves analyzing a dataset containing health and sleep statistics. The dataset includes information about individuals' sleep quality, physical activity levels, dietary habits, and sleep disorders. The primary goal of this analysis is to uncover insights related to sleep quality, how it relates to different factors like age, physical activity, sleep duration, and more.

The analysis covers various techniques such as correlation analysis, data visualization, linear regression, and hypothesis testing.

Dataset Description
The dataset Health_Sleep_Statistics.csv contains the following columns:

User ID: A unique identifier for each user.
Age: The age of the individual.
Gender: The gender of the individual (m for male, f for female).
Sleep Quality: A rating (1-10) of the individual's sleep quality.
Bedtime: The time the individual goes to bed, in HH:MM format.
Wake-up Time: The time the individual wakes up, in HH:MM format.
Daily Steps: The number of steps the individual takes per day.
Calories Burned: The number of calories the individual burns per day.
Physical Activity Level: The individual's physical activity level (low, medium, high).
Dietary Habits: The individual's dietary habits (healthy, unhealthy, medium).
Sleep Disorders: Whether the individual suffers from sleep disorders (yes or no).
Medication Usage: Whether the individual uses medication (yes or no).
Steps Involved in the Analysis
1. Data Loading and Overview
The dataset is loaded using pandas read_csv() function. After loading, we display the first few rows, shape, and column names to understand the structure of the data.

2. Data Cleaning
Handling Missing Data: There are no missing values in the dataset as confirmed by isna().sum().
Removing Duplicate Entries: The dataset does not contain duplicates as confirmed by duplicated().sum().
Dropping Irrelevant Columns: The "User ID" column is dropped since it does not contribute to the analysis.
3. Exploratory Data Analysis (EDA)
Descriptive Statistics: We generate summary statistics using df.describe() to understand the distribution of numerical features such as age, sleep quality, daily steps, and calories burned.
Categorical Distributions: Visualize distributions of categorical features like gender, physical activity level, and sleep disorders.
Correlation Analysis: Correlation heatmaps are used to analyze relationships between numerical features.
4. Key Analyses
Age vs Sleep Quality
We analyze the relationship between Age and Sleep Quality using correlation and linear regression. A strong negative correlation (-0.85) is found between age and sleep quality, suggesting that older individuals tend to report lower sleep quality.

Physical Activity vs Sleep Quality
The physical activity level is mapped to numerical values (low = 1, medium = 2, high = 3) and visualized to observe its relationship with sleep quality. Higher physical activity levels tend to correlate with better sleep quality.

Gender and Sleep Quality
We test whether there is a significant difference in sleep quality between males and females using hypothesis testing (t-test). The result shows that there is a significant difference in sleep quality, with females tending to have higher sleep quality.

Sleep Duration vs Sleep Quality
We calculate the sleep duration (difference between wake-up time and bedtime) and analyze its relationship with sleep quality. A positive correlation is found, suggesting that longer sleep duration is associated with higher sleep quality.

Sleep Disorders vs Sleep Quality
A boxplot is used to analyze the impact of sleep disorders on sleep quality. Individuals with sleep disorders tend to have lower sleep quality.

5. Predictive Modeling
Linear regression models are used to predict sleep quality based on different factors:

Age: A regression model predicts sleep quality based on age.
Sleep Duration: A regression model predicts sleep quality based on the number of hours of sleep.
6. Hypothesis Testing
Sleep Quality vs Gender: A t-test is performed to check if there is a statistically significant difference between males and females in terms of sleep quality.
Physical Activity vs Gender: A t-test is also performed to see if physical activity levels differ significantly between genders.
7. Data Visualization
Various visualizations are used to explore the data:

Barplots for categorical variables like gender and physical activity level.
Scatter plots for numerical variables like age and sleep quality.
Heatmaps to visualize correlations between numerical features.
Insights & Findings
Age and Sleep Quality: As individuals age, their sleep quality tends to decline.
Physical Activity: Higher physical activity levels are associated with better sleep quality.
Sleep Duration: Longer sleep durations are linked to higher sleep quality.
Gender: Females tend to report better sleep quality than males.
Sleep Disorders: Individuals with sleep disorders generally report lower sleep quality.
Conclusion
This analysis provides valuable insights into the factors that affect sleep quality. By understanding these relationships, individuals can make informed decisions about improving their health and sleep habits.

Requirements
Python 3.x
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
How to Run
Install the required libraries:

Copiar código
pip install pandas numpy matplotlib seaborn scikit-learn scipy
Load the dataset by specifying the path to the Health_Sleep_Statistics.csv file.

Run the analysis script in a Python environment such as Jupyter Notebook.

License
This project is licensed under the MIT License.
