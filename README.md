# 📰 News Sentiment Database  
### A Django + PostgreSQL + Django REST Framework + Sentiment Analysis Project  
Track, store, analyze, and visualize sentiment across global news sources.

---

## 📌 Overview

The **News Sentiment Database** is a full-stack, data-driven platform that collects news headlines from multiple sources, performs sentiment analysis (using classical NLP or AI models), stores the results in a structured database, and presents the insights in a clean, interactive dashboard.

This project solves real-world problems such as:
- Understanding media bias  
- Tracking sentiment trends over time  
- Monitoring industry, political, or economic narratives  
- Doing research for markets, cybersecurity, or public opinion  

It is built for:
- Portfolio showcasing  
- Data engineering practice  
- Django backend mastery  
- Dashboard & API development  

---

## 📂 Project Architecture

news_sentiment/
│
├── backend/
│ ├── manage.py
│ ├── config/ # Django project settings (split: base/dev/prod)
│ │ ├── base.py
│ │ ├── dev.py
│ │ ├── prod.py
│ │ └── init.py
│ ├── api/ # Django REST Framework API
│ │ ├── serializers.py
│ │ ├── views.py
│ │ ├── urls.py
│ │ └── tests.py
│ ├── sentiment/ # Sentiment analysis engine
│ │ ├── analyzer.py
│ │ ├── helpers.py
│ │ ├── pipeline.py
│ │ └── model/ # Optional ML/LLM models
│ ├── database/ # DB models + migrations
│ │ ├── models.py
│ │ └── migrations/
│ ├── collector/ # Web scrapers & API clients
│ │ ├── rss_scraper.py
│ │ ├── newsapi_client.py
│ │ └── scheduler.py
│ └── requirements.txt
│
├── frontend/ # Django template dashboard or React SPA
│ ├── static/
│ ├── templates/
│ ├── components/
│ └── package.json
│
├── docs/ # Documentation
│ └── system_architecture.md
│
├── .env.example
├── .gitignore
└── README.md


---

## ⭐ Features

### 🔍 **1. News Scraping & Collection**
- RSS Feed scraper  
- Optional NewsAPI integration  
- Scheduled data collection with CRON / Celery  
- De-duplicates headlines  

### 🧠 **2. Sentiment Analysis Engine**
Supports multiple modes:
- **TextBlob / Vader** → fast classical NLP  
- **HuggingFace Transformers** → advanced accuracy  
- **OpenAI/LLM API (optional)**  

Classifies sentiment as:
- Positive  
- Negative  
- Neutral  
- Compound score  

### 🗄️ **3. PostgreSQL Structured Database**
Stores:
- headline  
- source  
- category  
- publication date  
- sentiment + confidence  
- scraped timestamp  

### 📊 **4. Interactive Dashboard**
- Line charts (sentiment trends)  
- Bar charts by category/source  
- Filters: date range, sentiment type, category  
- Responsive UI  

### 🔌 **5. Full REST API (Django REST Framework)**
Endpoints:
- `/api/headlines/`
- `/api/sentiment/trends/`
- `/api/categories/`
- `/api/sources/`

Supports filtering, search, pagination, and ordering.

---

## 🚀 Getting Started (Local Development)

### **1. Clone the repository**
```bash
git clone https://github.com/<your-username>/news-sentiment-database.git
cd news-sentiment-database
