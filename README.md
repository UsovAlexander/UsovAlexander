<div align="center">

# Hi, I'm Alexander Usov 👋

### ML Engineer · LLM & RAG · RecSys · Classic ML

I build ML systems end-to-end: from exploratory analysis and model training
to production services with APIs, Docker, and tests.

[![Email](https://img.shields.io/badge/Email-alexander.usoff%40gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:alexander.usoff@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-UsovAlexander-181717?logo=github&logoColor=white)](https://github.com/UsovAlexander)

</div>

---

## 🛠 Tech Stack

**Languages & Data**

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Polars](https://img.shields.io/badge/Polars-CD792C?logo=polars&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)

**ML / RecSys**

![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-90C53F?logoColor=white)
![CatBoost](https://img.shields.io/badge/CatBoost-FFCC00?logoColor=black)
![XGBoost](https://img.shields.io/badge/XGBoost-EB0028?logoColor=white)
![Optuna](https://img.shields.io/badge/Optuna-4C72B0?logoColor=white)
![implicit](https://img.shields.io/badge/implicit%20(ALS)-E8710A?logoColor=white)

**LLM / NLP**

![RAG](https://img.shields.io/badge/RAG-8A2BE2?logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?logo=qdrant&logoColor=white)
![Sentence Transformers](https://img.shields.io/badge/Sentence--Transformers-FFD21E?logo=huggingface&logoColor=black)
![Groq](https://img.shields.io/badge/Groq-F55036?logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK%20%2F%20spaCy-09A3D5?logoColor=white)

**Engineering**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![pytest](https://img.shields.io/badge/pytest%20%2B%20coverage-0A9EDC?logo=pytest&logoColor=white)
![Locust](https://img.shields.io/badge/Locust-3C9E44?logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![aiogram](https://img.shields.io/badge/aiogram%203-2CA5E0?logo=telegram&logoColor=white)

---

## 🌟 Featured Projects

### 🧭 [HR AI Scout — LLM-powered resume-to-vacancy matching with RAG](https://github.com/UsovAlexander/hr-ai-scout-with-rag)

A system that retrieves relevant resumes for a given vacancy from **20,845 candidates** and uses an LLM to explain why each candidate fits, highlighting skill gaps.

- Hybrid search: dense embeddings (LaBSE-en-ru) + BM25 with RRF fusion in **Qdrant**
- LLM pipeline: extraction → gap analysis → scoring on **Groq + instructor**
- Honest offline retrieval evaluation: custom implementation of **NDCG@k / MRR / Recall@k / Precision@k** on a labeled golden set
- Streamlit UI: pick a vacancy → top-K resumes → per-candidate breakdown

`Python` `Qdrant` `LaBSE` `BM25` `Groq` `instructor` `Streamlit`

### 🏆 [HSE × T-Bank RecSys Competition — Top-10 finish](https://github.com/UsovAlexander/recsys_competition_hse_t-bank)

Kaggle recommender systems competition: predict top-20 purchases from **11.4M interactions** of 348K users. **NDCG@20 = 0.1397** on the private leaderboard.

- Two-stage pipeline: candidate generators (**EASE · ALS · Item-KNN**) → **LGBMRanker** (lambdarank) on 47 features
- Temporal decay of interaction weights: **+67% NDCG@20** for EASE
- Optuna tuning with cross-validation over 3 time windows — hyperparameters that stay stable over time
- Validation on the least active users to shrink the val→LB gap

`Python` `Polars` `implicit` `LightGBM` `Optuna`

---

## 📂 All Projects

### 🤖 LLM & NLP

| Project | Description | Stack |
|---|---|---|
| [hr-ai-scout-with-rag](https://github.com/UsovAlexander/hr-ai-scout-with-rag) | RAG system for matching resumes to vacancies: hybrid search + LLM gap analysis + offline retrieval evaluation | Qdrant, LaBSE, BM25, Groq, Streamlit |
| [chat-groq](https://github.com/UsovAlexander/chat-groq) | LLM chat application powered by the Groq API | Python, Groq |
| [news-topics-competition-2025](https://github.com/UsovAlexander/news-topics-competition-2025) | News topic classification competition | Python, NLP |

### 🎯 Recommender Systems

| Project | Description | Stack |
|---|---|---|
| [recsys_competition_hse_t-bank](https://github.com/UsovAlexander/recsys_competition_hse_t-bank) | Top-10 finish in the HSE × T-Bank Kaggle competition: two-stage "candidates → ranking" pipeline, NDCG@20 = 0.1397 | Polars, implicit, LightGBM, Optuna |

### ⚙️ ML Engineering & Services

| Project | Description | Stack |
|---|---|---|
| [FastAPI_project](https://github.com/UsovAlexander/FastAPI_project) | URL shortener API service: containerization, unit tests with coverage, load testing | FastAPI, Docker Compose, pytest, Locust |
| [healthy_lifestyle_bot](https://github.com/UsovAlexander/healthy_lifestyle_bot) | Telegram bot for tracking water, calories, and workouts: daily norm calculation, progress charts, external API integrations | aiogram 3, SQLite, Docker |
| [open-weather-map](https://github.com/UsovAlexander/open-weather-map) | Historical temperature analysis and weather monitoring service: anomaly detection, seasonality, Polars vs Pandas and sync vs async benchmarks | Python, Polars, asyncio, OpenWeatherMap API |

### 📈 Classic ML

| Project | Description | Stack |
|---|---|---|
| [car-price](https://github.com/UsovAlexander/car-price) | Car price prediction service: EDA, linear models (Ridge/Lasso/ElasticNet), custom L0 regularization implementation | pandas, sklearn, phik |
| [choosing-the-location-for-the-well](https://github.com/UsovAlexander/choosing-the-location-for-the-well) | Choosing a drilling location: reserve volume regression, profit and risk estimation with Bootstrap | pandas, sklearn |
| [recovery-of-gold-from-ore](https://github.com/UsovAlexander/recovery-of-gold-from-ore) | Predicting the gold recovery rate from ore: EDA of the industrial process, custom sMAPE metric | pandas, sklearn, catboost |

---

<div align="center">

## 📊 GitHub Stats

<img src="https://github-readme-stats.vercel.app/api?username=UsovAlexander&show_icons=true&hide_border=true&theme=transparent" alt="GitHub Stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=UsovAlexander&layout=compact&hide_border=true&theme=transparent" alt="Top Languages" />

</div>
