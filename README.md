# 🎬 Netflix Review Sentiment Analysis

A data analytics project analyzing Netflix customer reviews using Python, Natural Language Processing (NLP), Excel, and Power BI — built to understand how customer sentiment shifted around Netflix's March 2026 price increase.

---

## 🎯 Project Objective

Understand whether Netflix's March 2026 price increase measurably affected customer sentiment, and identify the specific themes driving negative reviews — combining Python for text analysis, Excel for quick validation, and Power BI for an interactive stakeholder-facing dashboard.

The project demonstrates an end-to-end data analytics workflow:
- Data collection
- Data processing & cleaning
- Sentiment analysis
- Dataset preparation
- Data visualization
- Interactive dashboard development
- Data-driven interpretation

---

## 📊 Key Findings

- Analyzed **157,624** Netflix app reviews (2018–2026) using Python and TextBlob-based sentiment analysis.
- Overall sentiment split: **58.5% positive**, **22.6% negative**, **18.9% neutral**.
- Negative sentiment share was **23.0%** in the years before Netflix's March 2026 price increase, compared to **15.7%** in the ~6 months after — a **decrease** of 7.3 percentage points. The price increase did not measurably worsen overall customer sentiment.
- Predicted sentiment matched each review's actual star rating in **56.0%** of cases — used as a validation check against the model rather than trusting it blindly.
- Negative reviews are dominated by recurring complaints — **"app," "netflix," "account," "issue," "movie," "show"** — appearing consistently both before and after the price hike, suggesting these are chronic product issues rather than reactions to pricing specifically.
- Two words — **"bad" and "worst"** — enter the top 10 negative-review words only in the post-price-hike period, suggesting sharper language among the smaller group who *are* upset, even though the overall negative share dropped.

---

## 🖼️ Dashboard Preview


**Power BI — Before vs After Price Hike**

<img width="1284" height="717" alt="dashboard 2" src="https://github.com/user-attachments/assets/531664e6-7528-450a-aa89-5cdf075e29e3" />

<img width="1281" height="716" alt="dashboard 3" src="https://github.com/user-attachments/assets/d3bf880a-58bf-4dca-b53d-11a1dbe5d9c7" />

**Python — Key Metrics & Sentiment Distribution**

<img width="1485" height="1184" alt="key_metrics_and_donut" src="https://github.com/user-attachments/assets/dea68c6f-77ea-4d70-bb0e-c1d17aa5f31c" />


**Python — Weekly Sentiment Trend & Review Volume**

<img width="1484" height="1184" alt="weekly_trend_and_volume" src="https://github.com/user-attachments/assets/5000a423-0c28-4407-af42-ea8ecadde525" />


**Python — Sentiment by Star Rating & Top Negative Keywords**

<img width="1785" height="1184" alt="rating_and_keywords" src="https://github.com/user-attachments/assets/e27a6af4-29dc-438c-998e-3428ad54a9d2" />


**Python — Most Common Words in Negative Reviews**

<img width="1370" height="735" alt="wordcloud" src="https://github.com/user-attachments/assets/9b389bba-3534-4b8d-8006-7e0798f2d90e" />


**Excel — Pivot Table Validation (Before vs After)**

<img width="1854" height="575" alt="pivot chart 1" src="https://github.com/user-attachments/assets/a90e58aa-04d3-49f1-b114-22da5708d42f" />

<img width="1859" height="625" alt="pivot chart 3" src="https://github.com/user-attachments/assets/a51ceb54-1ec8-4a39-8107-173db531e976" />


---

## 🗂️ Dataset

### Original Dataset Source
[View Netflix Reviews Dataset on Kaggle](https://www.kaggle.com/datasets/ashishkumarak/netflix-reviews-playstore-daily-updated)

> **Important:** The source dataset is updated regularly. The analysis in this repository was performed using the dataset version downloaded on **03-09-2026**. The current dataset available at the source may contain newer data and differ from the version used in this project.

### Data

The original dataset contains Netflix application review information such as:
- Review ID
- User name
- Review content
- Rating
- Thumbs-up count
- Review-created version
- Review date and time
- App version

The processed dataset adds the following sentiment-related fields:
- **Period** — Before / After the March 2026 price hike
- **Predicted Sentiment Score** — TextBlob polarity score
- **Predicted Sentiment Label** — positive / neutral / negative
- **Subjectivity Score** — how opinion-based vs. factual a review is (0–1)
- **Expected From Rating** — the sentiment implied by the review's star rating, used to validate the model

---

## 🧠 Methodology Notes

- Sentiment was scored using **TextBlob** rather than a deep-learning model, prioritizing speed and interpretability for a business-facing analysis rather than a research benchmark.
- Predicted sentiment is **cross-validated against each review's actual star rating** rather than taken at face value — reported as the "Model Agreement" metric (56.0%).
- Reviews are split into a **Before/After** period at the price hike date to isolate its effect. Because the "Before" period spans several years while "After" spans only ~6 months (the hike is recent), all comparisons use **percentage share within each period**, not raw counts, to keep the comparison fair.
- Date parsing required explicit day-first handling (`dayfirst=True`), since the source data uses DD-MM-YYYY formatting — without this, most dates failed to parse correctly.

---

## 🛠️ Tools & Technologies

- Python
- Jupyter Notebook
- Google Colab
- Pandas
- Natural Language Processing (NLP)
- Sentiment Analysis (TextBlob)
- Microsoft Power BI
- Microsoft Excel
- CSV

---

## 💻 Google Colab

The Python analysis notebook is also available on Google Colab for easy access and execution.

[Open the Notebook in Google Colab](https://colab.research.google.com/drive/1xYp7gcj4CHg5aNv4E9xBJF4TgBe6yqij?usp=sharing)

---

## 🔄 Project Workflow

```
Raw Netflix Reviews
        ↓
Data Processing & Cleaning
        ↓
Sentiment Analysis using Python
        ↓
Processed Sentiment Dataset
        ↓
Excel Pivot Table Validation
        ↓
Power BI Interactive Dashboard
        ↓
Data-Driven Insights
```

---

## 📁 Repository Contents

| File | Description |
|---|---|
| `netflix_sentiment.ipynb` | Python notebook — sentiment analysis, keyword extraction, and visualizations |
| `netflix_sentiment.csv` | Processed dataset with sentiment labels and scores |
| `netflix_sentiment_final.xlsx` | Excel workbook with pivot tables and charts |
| `netflix review.pbix` | Power BI interactive dashboard |
| `README.md` | This file |

---

## ✍️ Author

**Mayank Raj** · [LinkedIn](https://www.linkedin.com/in/mayankraj01/)
