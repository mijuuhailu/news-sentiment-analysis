# 📈 Financial News Sentiment Analysis and Stock Market Trends

## Project Overview

This project presents a comprehensive exploratory data analysis (EDA) and text analytics study of the Financial News and Stock Price Integration Dataset (FNSPID).

The dataset combines qualitative financial news data with quantitative stock market data to support sentiment-driven stock market analysis and predictive modeling.

The primary objective of this project is to analyze financial news headlines, identify recurring market themes, and explore how news publication patterns may influence stock market behavior.

The analysis focuses on:

* Financial news headline characteristics
* Publisher activity and coverage patterns
* Temporal trends in news publication
* Keyword and topic extraction using NLP techniques
* Time-series analysis of news volume
* Preparation for future sentiment analysis and stock-price correlation modeling

---

# Objectives

* Perform data cleaning and preprocessing
* Handle mixed datetime formats and timezone inconsistencies
* Conduct exploratory data analysis (EDA) on financial news data
* Analyze headline length distributions and publication trends
* Identify the most active publishers and covered stocks
* Extract common keywords and recurring financial themes
* Apply NLP techniques such as:

  * CountVectorizer
  * TF-IDF
  * Latent Dirichlet Allocation (LDA)
* Visualize time-series news publication patterns
* Prepare data for future sentiment analysis and predictive modeling

---

# Dataset Description

The project uses two integrated datasets:

## 1. Financial News Dataset

| Column    | Description                              |
| --------- | ---------------------------------------- |
| headline  | News article headline                    |
| url       | Link to the full article                 |
| publisher | Author or publisher of the article       |
| date      | Publication timestamp including timezone |
| stock     | Stock ticker symbol                      |

The headlines often contain financial events such as:

* earnings announcements
* analyst upgrades
* price target revisions
* mergers and acquisitions
* FDA approvals
* market outlook updates

---

## 2. Historical Stock Price Dataset

| Column    | Description                    |
| --------- | ------------------------------ |
| Date      | Trading day date               |
| Open      | Opening stock price            |
| High      | Highest stock price of the day |
| Low       | Lowest stock price of the day  |
| Close     | Closing stock price            |
| Adj Close | Adjusted closing price         |
| Volume    | Number of traded shares        |

The stock dataset serves as the quantitative foundation for future return calculations and sentiment-price correlation analysis.

---

# 🛠️ Methodology

# 1. Data Cleaning and Preprocessing

* Loaded and inspected financial news data
* Checked for missing values and duplicates
* Converted mixed-format publication timestamps into UTC datetime format
* Extracted:

  * publication date
  * hour
  * weekday
* Cleaned headline text by:

  * converting to lowercase
  * removing punctuation
  * removing stopwords

---

# 2. Exploratory Data Analysis (EDA)

## Descriptive Statistics

* Headline character length distribution
* Most frequently mentioned stocks
* Most active publishers
* Daily article publication counts

## Time Series Analysis

* News publication frequency over time
* Hourly publication patterns
* Weekday publication trends
* Detection of spikes in news activity

## Publisher Analysis

* Identification of dominant financial news publishers
* Analysis of organizational contribution patterns
* Extraction of email domains where applicable

---

# 3. Text Analysis and Topic Modeling

## Keyword Extraction

Applied:

* CountVectorizer
* TF-IDF

to identify the most important and frequently occurring financial terms.

Common themes included:

* earnings
* shares
* price target
* revenue
* acquisition
* analyst ratings

## Topic Modeling

Implemented Latent Dirichlet Allocation (LDA) to discover recurring financial topics such as:

* earnings reports
* stock upgrades
* FDA approvals
* mergers and acquisitions
* market forecasts

---

# Key Insights

* Financial headlines are generally concise and information-dense
* Significant spikes in article publication volume correspond to major market events
* A small number of publishers dominate financial news reporting
* Certain stocks receive substantially more media coverage than others
* Most financial news articles are published during market-related hours
* Common financial themes revolve around earnings, analyst ratings, and stock price movements

---

# Temporal Analysis Findings

### Publication Trends

* News volume fluctuates significantly over time
* Peaks often align with:

  * earnings seasons
  * economic announcements
  * major corporate events

### Publishing Hours

* Most articles are released before or during market trading hours
* This suggests publishers aim to influence investor sentiment during active trading periods

---

# NLP and Topic Modeling Findings

The NLP analysis revealed strong thematic concentration around:

* stock performance
* analyst recommendations
* earnings announcements
* acquisitions
* pharmaceutical approvals
* market expectations

TF-IDF and LDA successfully highlighted recurring financial narratives across the dataset.

---

# 🔧 Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* NLTK
* WordCloud
* Jupyter Notebook
* Git & GitHub
* GitHub Actions

---

# Visualizations Included

* Headline Length Distribution
* Top Publishers Bar Chart
* Daily News Volume Time Series
* Most Common Keywords Visualization
* Word Cloud
* Publishing Hour Distribution
* Stock Coverage Distribution

---

# Future Work

Future phases of the project will include:

* Sentiment analysis using NLP models
* Sentiment scoring of headlines
* Correlation analysis between news sentiment and stock returns
* Predictive modeling for stock movement forecasting
* Development of sentiment-driven investment strategies

---

# Conclusion

This project establishes a strong foundation for financial sentiment analysis by combining exploratory data analysis with NLP-based text analytics.

The insights extracted from financial news headlines and publication behavior provide valuable context for understanding market sentiment and preparing predictive financial models.
