# 📊 Google Play Store Analytics

## Interactive Business Intelligence & Predictive Analytics

A comprehensive data analytics project that analyzes Google Play Store applications to identify trends in ratings, installs, reviews, revenue proxies, user sentiment, and application success.

The project combines:

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Statistical Analysis
- Sentiment Analysis
- Success Score Analysis
- Predictive Machine Learning
- Interactive Business Intelligence Dashboard

---

## 🎯 Project Objective

The objective of this project is to analyze Google Play Store application data and identify the factors associated with application performance and user ratings.

The project answers questions such as:

- Which categories receive the most installs?
- Which categories generate the highest estimated revenue?
- How do free and paid applications differ?
- What is the relationship between reviews and ratings?
- What is the overall user sentiment?
- Which applications have the highest Success Score?
- Can an application's rating group be predicted?
- Which features contribute most to predicting rating groups?
  

🛠️ Technologies Used
Technology	Purpose
Python	Data analysis and machine learning
Pandas	Data manipulation
NumPy	Numerical computing
Matplotlib	Visualization
Seaborn	Statistical visualization
Plotly	Interactive visualization
SciPy	Statistical testing
Scikit-learn	Machine learning
NLTK / VADER	Sentiment analysis
Jupyter / Google Colab	Development environment
📊 Dataset

The project uses Google Play Store application data and user review data.

Application Dataset

Important variables include:

App
Category
Rating
Reviews
Size
Installs
Type
Price
Content Rating
Genres
Last Updated
Current Version
Android Version
Review Dataset

User reviews are analyzed to determine sentiment.

🧹 Data Cleaning

The following preprocessing steps were performed:

Removed duplicate applications
Removed invalid ratings
Converted Reviews to numeric format
Converted Installs to numeric format
Converted Price to numeric format
Converted application Size to MB
Converted Last Updated to datetime
Extracted Year
Handled missing values
Prepared categorical variables
⚙️ Feature Engineering

Several analytical features were created.

Log Installs
Log_Installs = log1p(Installs)
Log Reviews
Log_Reviews = log1p(Reviews)
Rating Group

Applications were categorized into:

Top rated
Above average
Average
Below average
Estimated Revenue
Revenue = Price × Installs

This value is treated as a revenue proxy because the original install values represent installation ranges.

Success Score
Success_Score = Rating × log1p(Reviews)

The Success Score is a custom analytical metric created for this project.

📈 Exploratory Data Analysis

The project analyzes:

Category distribution
Application type
Rating distribution
Install distribution
Review distribution
Revenue proxy
Genres
Content rating
Year-wise trends
Paid vs Free applications
Category performance
💬 Sentiment Analysis

User reviews were analyzed using VADER sentiment analysis.

Reviews were categorized into:

Positive
Neutral
Negative

This provides insight into overall user perception of applications.

📐 Statistical Analysis

An independent two-sample Welch's t-test was used to investigate whether the average ratings of paid and free applications differ significantly.

Null Hypothesis

There is no significant difference between the ratings of paid and free applications.

Alternative Hypothesis

There is a significant difference between the ratings of paid and free applications.

A significance level of:

α = 0.05

was used.

🤖 Predictive Analytics

A Random Forest Classifier was developed to predict:

Rating_Group
Features

The model uses characteristics such as:

Category
Reviews
Size
Installs
Price
Type
Content Rating
Genres
Year

The actual Rating variable is excluded from the predictive features to avoid target leakage.

📊 Model Evaluation

The model is evaluated using:

Accuracy
Precision
Recall
F1 Score
Confusion Matrix
Feature Importance
📊 Interactive Dashboard

The project includes an interactive HTML dashboard.

Dashboard features include:

KPI cards
Category filter
App type filter
Content rating filter
Year filter
Install filter
Rating range filter
Installs by category
Estimated revenue by category
Rating distribution
Reviews vs rating
User sentiment
Rating groups
Top performing applications
Success Score
Predictive feature importance

Open:

dashboard/Google_Play_Store_Interactive_Dashboard.html
🏆 Key Insights

Final insights are generated from the actual analysis and stored in:

results/final_insights.txt

Examples of questions addressed include:

Which categories dominate the Play Store?
Which categories have the highest installations?
Which categories have the highest estimated revenue?
How do paid and free apps compare?
What is the overall sentiment of users?
Which applications have the highest Success Score?
What factors contribute to predicting rating groups?
📄 Project Report

The detailed project report is available at:

report/Google_Play_Store_Analytics_Report.pdf
🚀 Future Scope

Possible future improvements include:

App recommendation system
Rating prediction using regression
Advanced NLP using transformer models
Time-series analysis
App success prediction
Deployment as a web application
Automated data pipeline
Real-time Play Store analytics

👨‍💻 Author
Yaseen Akthar Maniyar

B.Tech – Artificial Intelligence & Robotics

Dayananda Sagar University

Bengaluru, India

⭐ Acknowledgement

This project was developed as an academic data analytics and machine learning project to explore application performance, user sentiment, and predictive analytics using Google Play Store data.


```text
python
data-analysis
machine-learning
google-play-store
data-visualization
sentiment-analysis
random-forest
plotly
pandas
scikit-learn
business-intelligence
---

# 📂 Project Structure

```text
Google-Play-Store-Analytics/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── README.md
│   ├── Play Store Data.csv
│   └── User Reviews.csv
│
├── notebooks/
│   └── Google_Play_Store_Analytics.ipynb
│
├── dashboard/
│   └── Google_Play_Store_Interactive_Dashboard.html
│
├── results/
│   ├── figures/
│   └── final_insights.txt
│
└── report/
    └── Google_Play_Store_Analytics_Report.pdf
