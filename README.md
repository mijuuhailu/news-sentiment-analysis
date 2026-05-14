# 📈 Financial News Sentiment Analysis and Stock Market Trends

## Project Overview

This project presents a comprehensive exploratory data analysis (EDA), natural language processing (NLP), and financial sentiment analysis study using the Financial News and Stock Price Integration Dataset (FNSPID).

The project combines qualitative financial news data with quantitative stock market data to investigate how financial news sentiment relates to stock market performance.

The analysis includes:
- Exploratory data analysis of financial news headlines
- Publisher and temporal trend analysis
- Keyword extraction and topic modeling
- Sentiment analysis of financial headlines
- Daily stock return computation
- Correlation analysis between sentiment and stock price movement
- Visualization of sentiment-return relationships

The project focuses on selected technology companies:
- AAPL (Apple)
- AMZN (Amazon)
- GOOGL (Google)
- NVDA (NVIDIA)
- TSLA (Tesla)

---

#  Objectives

The objectives of this project are to:

- Perform data cleaning and preprocessing
- Handle mixed datetime formats and timezone inconsistencies
- Conduct exploratory data analysis (EDA) on financial news data
- Analyze headline length distributions and publication trends
- Identify the most active publishers and covered stocks
- Extract common keywords and recurring financial themes
- Apply NLP techniques including:
  - CountVectorizer
  - TF-IDF
  - Latent Dirichlet Allocation (LDA)
- Perform sentiment analysis on financial headlines
- Calculate daily stock returns from historical market data
- Measure the relationship between sentiment and stock performance
- Visualize sentiment-return correlations
- Prepare the dataset for predictive financial modeling

---

# 📂 Dataset Description

The project uses two integrated datasets.

---

# 1. Financial News Dataset

| Column | Description |
|---|---|
| headline | Financial news article headline |
| url | Link to the original article |
| publisher | Article publisher or author |
| date | Publication timestamp |
| stock | Stock ticker symbol |

The dataset contains financial news related to:
- earnings announcements
- analyst upgrades/downgrades
- stock price target changes
- mergers and acquisitions
- FDA approvals
- market outlook reports

---

# 2. Historical Stock Price Dataset

Historical stock price data was retrieved using the YFinance Python library.

| Column | Description |
|---|---|
| Date | Trading day date |
| Open | Opening stock price |
| High | Highest stock price |
| Low | Lowest stock price |
| Close | Closing stock price |
| Volume | Number of shares traded |

The stock dataset was used for:
- daily return calculations
- stock performance analysis
- sentiment-return correlation analysis

---

#  Methodology

# 1. Data Cleaning and Preprocessing

The preprocessing stage involved:
- loading and inspecting datasets
- checking for missing values and duplicates
- converting timestamps into datetime format
- normalizing timezone inconsistencies
- aligning news dates with trading days
- filtering selected technology stocks

Headline text preprocessing included:
- lowercasing text
- punctuation removal
- stopword removal

---

# 2. Exploratory Data Analysis (EDA)

## Descriptive Analysis

The following analyses were performed:
- headline length distribution
- most frequently mentioned stocks
- top publishers
- publication frequency trends

## Temporal Analysis

Time-series analysis included:
- daily publication volume
- hourly publication patterns
- weekday trends
- spikes in news activity

## Publisher Analysis

Publisher activity analysis identified:
- dominant financial news sources
- contribution distribution
- organizational publication patterns

---

# 3. Text Analysis and Topic Modeling

## Keyword Extraction

NLP techniques applied:
- CountVectorizer
- TF-IDF

These methods identified common financial terms such as:
- earnings
- shares
- revenue
- analyst ratings
- acquisitions
- price targets

## Topic Modeling

Latent Dirichlet Allocation (LDA) was used to identify recurring financial themes including:
- earnings reports
- analyst upgrades
- pharmaceutical approvals
- mergers and acquisitions
- market forecasts

---

# 4. Sentiment Analysis

Sentiment analysis was performed using the NLTK VADER sentiment analyzer.

VADER was selected because:
- it performs well on short text
- it is optimized for sentiment polarity detection
- it is suitable for financial headlines and news snippets

Each headline received a compound sentiment score ranging from:
- -1 → very negative
- 0 → neutral
- +1 → very positive

Daily average sentiment scores were then computed for each stock.

---

# 5. Daily Stock Return Calculation

Daily stock returns were computed using percentage change in closing prices:

\[
\text{Daily Return} = \frac{Close_t - Close_{t-1}}{Close_{t-1}} \times 100
\]

Where:
- \( Close_t \) is the current closing price
- \( Close_{t-1} \) is the previous closing price

---

# 6. Correlation Analysis

The Pearson correlation coefficient was used to measure the linear relationship between:
- average daily sentiment scores
- daily stock returns

Scatter plots and bar charts were generated to visualize the relationship.

---

#  Key Findings

## Exploratory Data Analysis Findings

- Financial headlines are concise and information-dense
- Publication volume fluctuates during major financial events
- A small number of publishers dominate financial reporting
- Certain stocks receive significantly more media coverage
- Most articles are published during active market hours

---

#  NLP and Topic Modeling Findings

The NLP analysis revealed strong thematic concentration around:
- earnings announcements
- stock upgrades
- analyst recommendations
- acquisitions
- market forecasts
- stock price movements

TF-IDF and LDA successfully identified recurring financial narratives across the dataset.

---

# 📈 Sentiment and Stock Return Findings

The sentiment analysis and correlation study produced the following results:

- Pearson Correlation Coefficient: **0.092**
- P-value: **2.98 × 10⁻¹⁵**

The results indicate:
- a weak positive correlation between news sentiment and stock returns
- statistically significant relationship due to the extremely low p-value

Positive sentiment days generally produced higher average stock returns, while negative sentiment days were associated with lower returns.

The scatter plot demonstrated a broad dispersion of points, suggesting that:
- sentiment influences stock prices only modestly
- many additional market factors contribute to price movement

---

# 📉 Visualizations Included

The project includes the following visualizations:
- Headline Length Distribution
- Top Publishers Bar Chart
- Daily News Volume Time Series
- Word Cloud
- Publishing Hour Distribution
- Stock Coverage Distribution
- Sentiment vs Stock Return Scatter Plot
- Average Return by Sentiment Category Bar Chart

---

#  Limitations

Several limitations were identified:
- Headlines alone may not fully capture article sentiment
- Market reactions may occur with time delays
- External macroeconomic factors affect stock prices
- Correlation does not imply causation
- Intraday market effects were not considered

---

# 🔧 Tools & Technologies

The project was implemented using:
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- NLTK
- WordCloud
- SciPy
- YFinance
- Jupyter Notebook
- Git & GitHub
- GitHub Actions

---

#  Future Work

Future improvements may include:
- using transformer-based NLP models (e.g., FinBERT)
- incorporating full article text instead of headlines only
- applying lagged sentiment analysis
- building predictive machine learning models
- integrating technical indicators
- developing sentiment-driven trading strategies

---

#  Conclusion

This project successfully combined exploratory data analysis, natural language processing, sentiment analysis, and financial market analysis to investigate the relationship between financial news and stock price movement.

The results demonstrated that financial news sentiment has a statistically significant but weak positive relationship with stock returns. While sentiment alone is not a strong predictor of market behavior, it provides useful insights into investor psychology and market dynamics.

Overall, the project establishes a strong foundation for future research in financial NLP, sentiment-driven investing, and predictive market analytics.