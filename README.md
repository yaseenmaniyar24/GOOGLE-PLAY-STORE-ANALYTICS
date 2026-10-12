# 📊 Google Play Store Analytics

### Interactive Business Intelligence, Statistical Analysis & Predictive Machine Learning

An end-to-end data analytics project that explores Google Play Store applications through data cleaning, exploratory data analysis (EDA), sentiment analysis, statistical hypothesis testing, feature engineering, machine learning, and an interactive business intelligence dashboard.

**Developed by:** Yaseen Akthar Maniyar
**Program:** B.Tech — Artificial Intelligence & Robotics
**Institution:** Dayananda Sagar University, Bengaluru, India

---

## 📌 Table of Contents

* [Overview](#-overview)
* [Problem Statement](#-problem-statement)
* [Project Objectives](#-project-objectives)
* [Key Features](#-key-features)
* [Technology Stack](#-technology-stack)
* [Project Architecture](#-project-architecture)
* [Repository Structure](#-repository-structure)
* [Dataset Description](#-dataset-description)
* [Data Cleaning and Preprocessing](#-data-cleaning-and-preprocessing)
* [Feature Engineering](#-feature-engineering)
* [Exploratory Data Analysis](#-exploratory-data-analysis)
* [Sentiment Analysis](#-sentiment-analysis)
* [Statistical Analysis](#-statistical-analysis)
* [Predictive Analytics](#-predictive-analytics)
* [Model Evaluation](#-model-evaluation)
* [Interactive Dashboard](#-interactive-dashboard)
* [Installation and Setup](#-installation-and-setup)
* [How to Run the Project](#-how-to-run-the-project)
* [Results and Business Insights](#-results-and-business-insights)
* [Limitations](#-limitations)
* [Future Scope](#-future-scope)
* [Reproducibility](#-reproducibility)
* [Author](#-author)
* [Acknowledgements](#-acknowledgements)
* [License](#-license)

---

## 🔍 Overview

Mobile applications operate in a competitive ecosystem where ratings, user engagement, application categories, pricing, and customer feedback can influence product decisions.

This project analyzes Google Play Store application metadata and user reviews to understand application performance and user sentiment. It combines descriptive analytics, statistical methods, and predictive modelling in one workflow.

The project is designed to answer questions such as:

* Which application categories have the largest reported installation totals?
* How are app ratings distributed?
* What differences exist between free and paid applications?
* How do reviews and ratings relate to each other?
* What sentiment is expressed in user reviews?
* Which applications achieve a high custom Success Score?
* Can an application's rating group be predicted from its characteristics?
* Which features are most useful to the trained classification model?

The final output includes a Jupyter/Google Colab notebook, an interactive HTML dashboard, visualizations, and a detailed project report.

## 🎯 Problem Statement

How can application metadata and user reviews be analyzed to identify performance patterns, investigate differences between paid and free applications, summarize user sentiment, and predict application rating groups using machine-learning techniques?

## 🎯 Project Objectives

1. Clean and preprocess application metadata and user-review data.
2. Perform exploratory data analysis to identify distributions and relationships.
3. Analyze app ratings, reviews, installations, prices, categories, and update years.
4. Engineer useful analytical features, including log-transformed counts and a custom Success Score.
5. Apply sentiment analysis to user reviews.
6. Use statistical hypothesis testing to investigate rating differences between paid and free applications.
7. Train a Random Forest classifier to predict rating groups without using the actual rating as an input.
8. Evaluate model performance using classification metrics and a confusion matrix.
9. Identify important predictive features.
10. Build an interactive dashboard for data exploration and business reporting.

---

## ✨ Key Features

| Feature               | Description                                                                  |
| --------------------- | ---------------------------------------------------------------------------- |
| Data preprocessing    | Cleans missing, duplicated, and incorrectly typed values                     |
| Exploratory analysis  | Examines application ratings, categories, reviews, and installations         |
| Feature engineering   | Creates log-transformed variables, rating groups, and a custom Success Score |
| Sentiment analysis    | Classifies review polarity into positive, neutral, and negative categories   |
| Statistical testing   | Uses Welch's t-test to compare average ratings between paid and free apps    |
| Predictive modelling  | Uses Random Forest to predict application rating groups                      |
| Model evaluation      | Reports accuracy, precision, recall, F1-score, and confusion matrix          |
| Feature importance    | Ranks features according to their importance in the trained Random Forest    |
| Interactive dashboard | Provides filters, KPI cards, interactive charts, and a top-apps table        |
| Business insights     | Supports data-driven interpretation of application performance               |

---

## 🛠️ Technology Stack

| Technology            | Purpose                                      |
| --------------------- | -------------------------------------------- |
| Python                | Main programming language                    |
| Pandas                | Data manipulation and cleaning               |
| NumPy                 | Numerical computation                        |
| Matplotlib            | Data visualization                           |
| Seaborn               | Statistical visualization                    |
| Plotly                | Interactive charts and dashboard             |
| SciPy                 | Statistical hypothesis testing               |
| Scikit-learn          | Preprocessing, Random Forest, and evaluation |
| NLTK / VADER          | Lexicon-based sentiment analysis, where used |
| Jupyter Notebook      | Interactive analysis                         |
| Google Colab          | Cloud-based development and execution        |
| HTML, CSS, JavaScript | Interactive dashboard interface              |
| Git and GitHub        | Version control and project hosting          |

---

## 🏗️ Project Architecture

```text
                 GOOGLE PLAY STORE DATA
                           |
              +------------+------------+
              |                         |
              v                         v
       APPLICATION DATA           USER REVIEWS
              |                         |
              v                         v
       DATA CLEANING              TEXT PROCESSING
              |                         |
              v                         v
      FEATURE ENGINEERING        SENTIMENT ANALYSIS
              |                         |
              +------------+------------+
                           |
                           v
              EXPLORATORY DATA ANALYSIS
                           |
              +------------+-------------+
              |                          |
              v                          v
      STATISTICAL ANALYSIS       SUCCESS SCORE ANALYSIS
              |
              v
       PREDICTIVE ANALYTICS
              |
              v
        RANDOM FOREST MODEL
              |
              v
      MODEL EVALUATION & IMPORTANCE
              |
              v
      INTERACTIVE HTML DASHBOARD
              |
              v
       BUSINESS INSIGHTS & REPORT
```

---

## 📂 Repository Structure

```text
Google-Play-Store-Analytics/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── Google_Play_Store_Analytics.ipynb
│
├── dashboard/
│   └── Google_Play_Store_Interactive_Dashboard.html
│
├── results/
│   ├── figures/
│   │   ├── category_distribution.png
│   │   ├── installs_by_category.png
│   │   ├── revenue_by_category.png
│   │   ├── rating_distribution.png
│   │   ├── sentiment_distribution.png
│   │   ├── confusion_matrix.png
│   │   └── feature_importance.png
│   │
│   └── final_insights.txt
│
└── report/
    └── Google_Play_Store_Analytics_Report.pdf
```

**Note:** Add each file when it exists. The raw datasets are intentionally not assumed to be included. Review the dataset licensing and redistribution terms before uploading them.

---

## 📁 Dataset Description

The project uses two types of data.

### 1. Application Metadata

The application dataset includes fields such as:

| Column           | Description                                      |
| ---------------- | ------------------------------------------------ |
| `App`            | Application name                                 |
| `Category`       | Application category                             |
| `Rating`         | Application rating on a 0–5 scale                |
| `Reviews`        | Number of reported reviews                       |
| `Size`           | Application size                                 |
| `Installs`       | Reported installation count or range             |
| `Type`           | Free or paid classification                      |
| `Price`          | Listed application price                         |
| `Content Rating` | Content or audience classification               |
| `Genres`         | Application genre                                |
| `Last Updated`   | Date of the last reported update                 |
| `Current Ver`    | Reported current version                         |
| `Android Ver`    | Minimum or supported Android version information |

### 2. User Review Data

The review dataset supports sentiment analysis using available review text and associated sentiment fields.

Possible fields include translated review text, sentiment labels, polarity, subjectivity, and sentiment scores, depending on the source file and preprocessing performed.

### Dataset Source

**Add the verified dataset source URL here before publishing.**

Document the source, access date, and license or terms of use. Do not upload third-party data unless redistribution is permitted.

---

## 🧹 Data Cleaning and Preprocessing

The preprocessing workflow includes:

* Inspecting dataset structure, column types, and missing values.
* Identifying and removing duplicate application records where appropriate.
* Validating rating values.
* Converting review counts and installation counts to numeric values.
* Removing formatting characters and currency symbols from numeric fields.
* Converting application size to a consistent numeric unit.
* Parsing update dates and extracting the update year.
* Handling missing values appropriately.
* Preparing categorical features for machine learning.
* Checking the cleaned data before performing analysis.

The final notebook documents the transformations and should be used as the authoritative record of the executed workflow.

---

## ⚙️ Feature Engineering

### 1. Log-transformed review counts

```python
apps_df["Log_Reviews"] = np.log1p(apps_df["Reviews"])
```

This reduces the scale of highly skewed review counts and makes distributions easier to visualize.

### 2. Log-transformed installations

```python
apps_df["Log_Installs"] = np.log1p(apps_df["Installs"])
```

This helps examine installation patterns across applications with very different reported counts.

### 3. Rating groups

Applications are categorized using rating thresholds:

| Rating condition | Rating group  |
| ---------------- | ------------- |
| Rating ≥ 4       | Top rated     |
| 3 ≤ Rating < 4   | Above average |
| 2 ≤ Rating < 3   | Average       |
| Rating < 2       | Below average |

Missing ratings should be handled separately rather than automatically assigned to a rating group.

### 4. Estimated revenue proxy

```python
apps_df["Revenue"] = apps_df["Price"] * apps_df["Installs"]
```

This metric estimates a simple price-times-installation proxy.

**Important:** This is not actual developer revenue. Installation values may represent ranges, and the calculation does not account for paid conversion, refunds, platform fees, taxes, subscriptions, or in-app purchases. Results must be described as *estimated revenue proxy*.

### 5. Custom Success Score

```python
apps_df["Success_Score"] = (
    apps_df["Rating"] * np.log1p(apps_df["Reviews"])
)
```

The Success Score combines the app's rating and review volume into a custom ranking metric.

It is an analytical metric defined for this project, not an official Google Play metric. Since both variables appear directly in the formula, the score should not be treated as independent proof of business success.

---

## 📊 Exploratory Data Analysis (EDA)

The EDA stage examines the dataset using descriptive statistics, grouped summaries, and visualizations.

### Areas of analysis

* Application category distribution
* Free versus paid application distribution
* Rating distribution
* Review and installation patterns
* Application size distribution
* Category-wise installations
* Category-wise estimated revenue proxy
* Rating and review relationships
* Genre and content-rating distributions
* Application update-year patterns
* Top applications according to the custom Success Score

### Analytical questions

1. Which categories contain the most listed applications?
2. Which categories have the highest reported installation totals?
3. How are application ratings distributed?
4. Do paid and free applications show different rating distributions?
5. How does review volume relate to ratings?
6. Which categories rank highly using the estimated revenue proxy?
7. Which applications rank highest according to the Success Score?

Category totals should be interpreted alongside per-app averages or medians because larger categories may naturally have higher totals.

---

## 💬 Sentiment Analysis

Sentiment analysis examines the polarity expressed in available user reviews.

When VADER compound scores are used, the project can classify reviews with the following thresholds:

| Sentiment | Compound score         |
| --------- | ---------------------- |
| Positive  | ≥ 0.05                 |
| Neutral   | Between −0.05 and 0.05 |
| Negative  | ≤ −0.05                |

The sentiment analysis can help summarize the tone of user feedback and compare it with other application-level measures.

### Interpretation considerations

* Missing review text should not automatically be classified as neutral.
* Sentiment scores are not a definitive measure of customer satisfaction.
* Sarcasm, context, multilingual text, and domain-specific vocabulary can affect classification.
* The aggregation rule for app-level sentiment should be documented.

---

## 📐 Statistical Analysis

### Paid versus free application ratings

The project uses an independent two-sample Welch's t-test to investigate whether average ratings differ between paid and free applications.

**Null hypothesis (H₀):**

There is no difference in the population mean ratings of paid and free applications.

**Alternative hypothesis (H₁):**

The population mean ratings of paid and free applications differ.

**Significance level:**

```text
α = 0.05
```

### Statistical outputs

The analysis reports:

* Number of valid paid and free ratings
* Mean rating for each group
* Standard deviation for each group
* Welch's t-statistic
* P-value
* 95% confidence interval for the mean difference
* Effect size, such as Cohen's d

### Decision rule

* If `p < 0.05`, reject the null hypothesis.
* If `p ≥ 0.05`, fail to reject the null hypothesis.

The p-value should be interpreted alongside the confidence interval and effect size. Statistical significance alone does not imply a practically large difference.

**Results:** Insert the actual values from the executed notebook before publishing conclusions.

---

## 🤖 Predictive Analytics

### Objective

The machine-learning component predicts an application's `Rating_Group` using selected application characteristics.

### Target variable

```text
Rating_Group
```

### Planned input features

* Category
* Reviews
* Size
* Installs
* Price
* Type
* Content Rating
* Genres
* Year

Only columns available and appropriately prepared in the final dataset are included.

### Model

**Random Forest Classifier**

The pipeline includes:

1. Selecting input features and the target.
2. Splitting data into training and test sets.
3. Imputing missing numerical and categorical values.
4. Encoding categorical variables.
5. Training the Random Forest classifier.
6. Predicting rating groups on the held-out test set.
7. Evaluating model performance.
8. Analyzing feature importance.

### Preventing target leakage

The actual `Rating` column must be excluded from the input features because `Rating_Group` is directly derived from it.

The model therefore attempts to classify rating groups from other application characteristics rather than receiving the original rating as an input.

This is a retrospective classification task. It does not guarantee that the model can forecast an application's future rating.

---

## 📈 Model Evaluation

The Random Forest model is evaluated using the following metrics:

| Metric             | Purpose                                                    |
| ------------------ | ---------------------------------------------------------- |
| Accuracy           | Overall proportion of correct predictions                  |
| Precision          | Proportion of predicted class assignments that are correct |
| Recall             | Proportion of actual class cases correctly identified      |
| F1-score           | Harmonic mean of precision and recall                      |
| Confusion matrix   | Shows correct predictions and class-level errors           |
| Feature importance | Ranks features by their importance in the fitted model     |

The results should also be compared with a simple baseline, such as always predicting the most common class.

Feature importance indicates predictive usefulness in the fitted model; it does not establish causation.

### Results

Insert the actual accuracy, precision, recall, F1-score, confusion matrix, and feature-importance findings from the executed notebook.

---

## 📊 Interactive Business Intelligence Dashboard

The project includes a standalone HTML dashboard designed to make the analysis easier to explore.

**Dashboard file:**

`dashboard/Google_Play_Store_Interactive_Dashboard.html`

### Dashboard components

* KPI cards for total apps, average rating, reported installs, and estimated revenue proxy
* Category filter
* App type filter
* Content rating filter
* Update-year filter
* Minimum-install filter
* Rating-range filter
* Installs by category
* Estimated revenue proxy by category
* Rating distribution
* Reviews versus rating
* User sentiment distribution
* Rating-group distribution
* Top-performing apps table based on Success Score
* Predictive feature-importance chart when model results are available

The dashboard filters are intended to update the visible metrics and charts without a full-page refresh.

### How to open the dashboard

1. Open the repository.
2. Navigate to the `dashboard/` folder.
3. Download `Google_Play_Store_Interactive_Dashboard.html`.
4. Open it in a modern browser.

The provided HTML version loads Plotly from a CDN, so an internet connection may be required for charts to render. GitHub's file preview may not execute the interactive dashboard; download the file or host it through a suitable static site.

---

## 🚀 Installation and Setup

### Requirements

* Python 3.10 or a compatible Python version
* Jupyter Notebook or Google Colab
* Required Python libraries
* Access to the project datasets

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Google-Play-Store-Analytics.git
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Enter the project directory

```bash
cd Google-Play-Store-Analytics
```

### 3. Create a virtual environment (recommended)

```bash
python -m venv .venv
```

Activate it on macOS/Linux:

```bash
source .venv/bin/activate
```

On Windows:

```bash
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Prepare the datasets

Place the permitted source CSV files in the `data/` directory, or update the notebook paths to match their location.

Do not assume the datasets are included in the repository. Follow the documented source and license conditions.

---

## ▶️ How to Run the Project

### Option A: Google Colab

1. Open the notebook in the `notebooks/` directory.
2. Upload it to Google Colab or open the repository notebook in Colab.
3. Provide access to the required datasets.
4. Update file paths if necessary.
5. Run the notebook cells in order.
6. Review the generated plots, statistical results, and model metrics.
7. Run the dashboard-generation cell.
8. Download the generated HTML dashboard.

### Option B: Jupyter Notebook

Run:

```bash
jupyter notebook
```

Open:

```text
notebooks/Google_Play_Store_Analytics.ipynb
```

Run the cells sequentially after configuring the dataset paths.

---

## 🏆 Results and Business Insights

The project is designed to generate findings about:

* Application category distribution and reported installations
* Differences in rating distributions
* User-review sentiment
* Paid versus free rating comparisons
* Custom Success Score rankings
* Random Forest classification performance
* Important predictors of rating groups

### Final results summary

Complete this table using the actual output from the executed notebook.

| Analysis                                         | Result            |
| ------------------------------------------------ | ----------------- |
| Final number of applications                     | Add actual result |
| Average application rating                       | Add actual result |
| Highest-install category                         | Add actual result |
| Highest estimated-revenue category               | Add actual result |
| Paid versus free t-test p-value                  | Add actual result |
| Positive / neutral / negative review percentages | Add actual result |
| Random Forest accuracy                           | Add actual result |
| Weighted F1-score                                | Add actual result |
| Most important predictive feature                | Add actual result |

Do not publish placeholder values as final findings. The interpretation must be supported by the actual dataset and model outputs.

---

## ⚠️ Limitations

1. The dataset may be historical and may not represent the current Play Store.
2. Installation values may be ranges rather than exact counts.
3. Price multiplied by installs is only an estimated revenue proxy.
4. Ratings and review counts may be skewed or affected by selection bias.
5. Sentiment analysis may misinterpret sarcasm, context, and multilingual reviews.
6. Rating groups depend on the selected rating thresholds.
7. Predictive performance depends on data quality, class balance, and feature selection.
8. Feature importance does not demonstrate causality.
9. A single train/test split may produce unstable performance estimates.
10. Results should not be generalized beyond the dataset without further validation.

---

## 🔮 Future Scope

Possible improvements include:

* Comparing additional classification algorithms
* Applying cross-validation and hyperparameter tuning
* Evaluating feature importance using permutation methods
* Improving sentiment analysis with advanced NLP models
* Building an app recommendation system
* Exploring rating regression with careful leakage control
* Adding confidence intervals and more statistical tests
* Deploying the dashboard as a hosted web application
* Automating analysis and report generation
* Developing a more robust app-category opportunity analysis

---

## 🔁 Reproducibility

To reproduce the analysis:

1. Obtain the same permitted datasets.
2. Use the documented Python dependencies.
3. Run the notebook cells in order.
4. Confirm that the cleaning and feature-engineering steps complete successfully.
5. Re-run the statistical test and model evaluation.
6. Regenerate the dashboard and result figures.
7. Record the software versions and dataset source.

Exact dependency versions can be added to `requirements.txt` to make the environment more reproducible.

---

## 👨‍💻 Author

### Yaseen Akthar Maniyar

**B.Tech — Artificial Intelligence & Robotics**
Dayananda Sagar University
Bengaluru, Karnataka, India

Areas of interest: Data Analytics, Machine Learning, Artificial Intelligence, Robotics, and Data Visualization.

* GitHub: [https://github.com/yaseenmaniyar24?tab=overview&from=2026-10-01&to=2026-10-02]
* LinkedIn: [https://www.linkedin.com/in/maniyaryaseen2005/?isSelfProfile=true]
* Email: [maniyaryaseen67@gmail.com]

---

## 🙏 Acknowledgements

This project was developed as an academic and portfolio-oriented data analytics project to explore application performance, user sentiment, statistical analysis, and predictive modelling using Google Play Store data.

Acknowledgement and citation details for the original datasets should be added once their exact sources and license terms have been verified.

---

## 📄 License

The project code may be distributed under the license included in the repository.

A project-code license does not automatically grant rights to redistribute third-party datasets. Dataset reuse remains subject to the original source's licensing terms.

---

⭐ If you find this project useful, consider starring the repository and sharing feedback or suggestions for improvement.
