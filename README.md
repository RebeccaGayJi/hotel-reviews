# 📊 Luxury Hotel Review Analytics – Singapore

## Project Overview
This project applies **text mining, sentiment analysis, topic modelling, and predictive machine learning** to analyse online hotel reviews from **Booking.com**. It focuses on the **top 15 luxury hotels in Singapore**, with the objective of identifying key drivers of guest satisfaction and dissatisfaction, uncovering service gaps, and supporting **data-driven strategies to enhance guest experience and room revenue**.

Despite consistently high occupancy rates, Singapore’s luxury hotel segment has experienced a decline in room revenue. This study demonstrates how unstructured customer feedback can be transformed into actionable insights to support **revenue management, service quality improvement, and brand reputation protection**.

---

## Data Source
- **Platform:** Booking.com  
- **Data Type:** User-generated hotel reviews  
- **Scope:** Top 15 luxury hotels in Singapore (Guests’ Choice rankings)  
- **Dataset Size:** ~20,000 cleaned reviews  
- **Key Attributes:**  
  - Hotel name  
  - Review title, positive and negative text  
  - Rating  
  - Travel type  
  - Duration of stay  
  - Reviewer country  
  - Review posting date  

Reviews were collected using a **Python-based web scraper**, which was enhanced to support **batch scraping** and consolidation of multiple hotels into a single dataset.

---

## Data Preparation
Data preparation ensures consistency and quality for analysis:
- Removal of duplicate records and irrelevant attributes  
- Handling of missing values and date standardisation  
- Discretisation of numerical ratings into **positive, neutral, and negative** sentiment labels  
- Text pre-processing using **NLTK**, including:
  - Language filtering (English only)
  - Lowercasing and tokenisation
  - Removal of general and domain-specific stopwords
  - Part-of-speech tagging and lemmatisation

---

## Exploratory Data Analysis (EDA)
Exploratory analysis reveals that:
- Guest ratings are **heavily skewed towards positive sentiment**
- Core experience drivers include **location, staff service, room quality, and amenities**
- Reviews are dominated by travellers from Western countries
- Satisfaction remains consistently high across travel types and duration of stay

Visualisations include rating trends, histograms, word clouds, choropleth maps, box plots, and heatmaps.

---

## Sentiment Analysis
Two lexicon-based sentiment analysis techniques are employed:
- **TextBlob** – polarity and subjectivity scoring  
- **VADER** – sentiment intensity and compound scoring  

While TextBlob achieves slightly higher overall accuracy, **VADER is selected** for further analysis due to its stronger ability to identify **negative reviews**, which is critical for service recovery and reputation management.

---

## Topic Modelling
- **Latent Dirichlet Allocation (LDA)** is used to uncover latent themes within hotel reviews  
- Reviews are grouped into 10 topics representing key hotel service dimensions  
- **pyLDAvis** is used to visualise topic distributions and improve interpretability  
- **n-grams (bi-grams and tri-grams)** complement LDA by capturing contextual phrases

Findings indicate that dissatisfaction is primarily driven by **customer service lapses, perceived poor value, and room or facility-related issues**.

---

## Predictive Modelling
Three supervised machine learning models are trained to predict review sentiment:
- **Logistic Regression**
- **Random Forest**
- **XGBoost**

Key modelling steps include:
- TF-IDF vectorisation of review text  
- Class imbalance handling using **SMOTE**  
- Model evaluation using confusion matrices, ROC curves, precision, recall, and F1-score  

**Logistic Regression** is selected as the final model due to its balanced performance in detecting both positive and negative sentiments, high ROC-AUC, interpretability, and computational efficiency.

---

## Key Outcomes
- Identifies high-impact service areas influencing guest satisfaction  
- Demonstrates how sentiment analytics can support **early detection of service issues**  
- Provides a scalable framework for **automated hotel review analysis**  
- Supports strategic decision-making to enhance guest experience and drive revenue growth  

---
