# 🍕 Tucson Pizza Review Analyzer

A full pipeline project for analyzing Tucson-based pizza restaurant reviews from Yelp using advanced NLP techniques. This solution covers Exploratory Data Analysis (EDA), Aspect-Based Sentiment Analysis using BERT, and automated summary generation using Claude via Amazon Bedrock.

A complete project overview: https://ugc.production.linktr.ee/ed6a0fce-8b3d-41f1-beca-3b6b4a622459_CIS-509---Final-Project.pdf

---

## ✨ Project Pipeline Overview

1. **EDA (`eda.ipynb`)** - Review structure & visualization  
2. **Aspect-Based Sentiment Analysis (`bert_sentiment_analysis.ipynb`)** - Deep review analysis with BERT  
3. **Summary Generation using Claude (`claude_summarization.ipynb`)** - Restaurant-level summary writing

---

## 📊 1. Exploratory Data Analysis (EDA)

**File:** `eda.ipynb`

- **Data Source:** Yelp Open Dataset (filtered for Tucson pizza restaurants)
- **Objectives:**
  - Clean raw review text
  - Generate WordCloud of top terms
  - Visualize sentiment distribution
  - Analyze star ratings and review interactions
  - Compute dataset statistics

**Highlights:**
- 🔍 Dominant keywords: *crust*, *cheese*, *service*, *location*
- ✅ Most reviews are positive
- ⭐ Star ratings show a bimodal distribution (1-star and 5-star)

---

## 🤖 2. Aspect-Based Sentiment Analysis with BERT

**File:** `bert_sentiment_analysis.ipynb`

- **Model:** [`nlptown/bert-base-multilingual-uncased-sentiment`](https://huggingface.co/nlptown/bert-base-multilingual-uncased-sentiment)
- **Goal:** Analyze each business based on 10 pizza-related aspects

### 🍕 Aspects Analyzed:

taste, crust, sauce, cheese, hygiene, delivery speed, service, price, environment, ambience


### 🔧 Core Features:
- Extracts aspect keywords from each review
- Predicts sentiment with BERT and converts star ratings (1–5) to scores (0–10)
- Computes average rating per aspect per business
- Generates:
  - Aspect frequency bar chart
  - Top 10 business ratings per aspect
  - Classification heatmap for 10 businesses

---

## 🧠 3. Summary Generation with Claude (Amazon Bedrock)

**File:** `claude_summarization.ipynb`

- **Service:** Claude 3 Sonnet via Amazon Bedrock
- **Objective:** Generate a short, engaging, and informative summary per business based on aspect ratings

### ✏️ What the summary includes:
- Overall impression (2–3 sentences)
- Top strengths and areas for improvement
- Value assessment (price vs. quality)
- Best use case (e.g., date night, quick lunch)

> Output: `pizza_restaurant_summaries.txt`

---

## 🛠️ Installation

Install all required dependencies:

pip install pandas seaborn matplotlib wordcloud transformers s3fs boto3

---

## ▶️ How to Run
Step 1: Run EDA

Step 2: Run Sentiment Analysis

Step 3: Generate Summaries with Claude

## 💡 Insights You Can Discover
Which restaurants have the best crust, cheese, or service?

Are some restaurants good for ambiance but poor in delivery speed?

What pizza qualities matter most to Tucson locals?

How would a summary look to a customer viewing the restaurant?

## 📂 Output Files
sentiment_analysis_results.csv – all review scores and sentiments

pizza_restaurant_summaries.txt – generated summaries

styled_table_big.png – formatted output table for presentation

## 📈 Future Improvements
Integrate OpenAI (ChatGPT) for summary comparison

Deploy as a Streamlit dashboard

Add real-time Yelp API integration

Interactive filtering by aspect

## 🗂️ Data Source
Yelp Open Dataset: https://www.yelp.com/dataset

## 🧑‍💻 Authors
Tsai-Yun Hsieh

Sarah Le

Delna Sophia Dsouza

Mary John

