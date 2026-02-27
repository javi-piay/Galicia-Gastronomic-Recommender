# 🍽️ Galicia Gastronomic Destination Recommendation System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![NLP](https://img.shields.io/badge/NLP-SBERT-orange)
![Recommender System](https://img.shields.io/badge/System-Hybrid-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Hybrid recommendation system designed to suggest gastronomic destinations in Galicia by integrating heterogeneous data sources and semantic modeling techniques.

---

## 📌 Project Overview

This project develops a **hybrid recommendation system** capable of suggesting personalized gastronomic destinations in Galicia.

The system combines:

- Web scraping (TripAdvisor)
- Google Places API enrichment
- Natural Language Processing (TF-IDF + SBERT embeddings)
- Contextual filters (geographic proximity & opening hours)
- Interactive visualization

Rather than building a simple similarity engine, the goal was to construct a **complete data pipeline**, from data acquisition to contextual recommendation and visualization.

---

## 🎯 Objective

To design and implement a hybrid recommender system that:

- Understands free-text user queries  
- Identifies semantically similar restaurants  
- Applies contextual filters (distance, price, rating, availability)  
- Provides structured and ranked recommendations  

---

## 🏗️ System Architecture

The system follows a structured pipeline:

1. **Data Acquisition**
   - TripAdvisor scraping (3,986 restaurants)
   - Google Places API enrichment

2. **Data Cleaning & Normalization**
   - Text normalization (accents, formatting, language unification)
   - Price harmonization (1–4 scale)
   - Duplicate detection & resolution
   - Translation and semantic homogenization

3. **Feature Engineering & Enrichment**
   - Category mapping
   - Dish detection
   - Contextual flags creation

4. **Hybrid Recommendation Engine**
   - TF-IDF (lexical similarity)
   - SBERT multilingual embeddings
   - Hybrid scoring mechanism (α-weighted)
   - Hierarchical filtering

5. **Contextual Filters**
   - Geographic proximity (Haversine + OpenRouteService API)
   - Opening hour validation (midnight crossing logic included)

6. **Visualization**
   - Interactive map (Folium)
   - Ranked result display

---

## 🧠 Recommendation Approach

The system integrates two complementary strategies:

### 🔎 Lexical Matching
- TF-IDF vectorization
- Fast and lightweight

### 🧬 Semantic Matching
- SBERT (paraphrase-multilingual-MiniLM-L12-v2)
- Captures synonyms and contextual meaning

### ⚙️ Hybrid Scoring

Final ranking combines:

- Text similarity
- Category matching
- User filters
- Distance (optional)
- Rating
- Number of reviews

---

## 🖥️ Recommendation Workflow Example

Below is an example of a simulated user query and system output.

The workflow illustrates:

- Application of categorical filters  
- Hybrid text similarity search (TF-IDF + SBERT)  
- Contextual filtering (price, rating, availability)  
- Final ranked recommendations  

### 🗺️ Interactive Map Output

The system generates an interactive map where users can:

- Visualize recommended restaurants  
- Navigate geographically  
- Access key information for each result  

👉 Example visualization available here:  
[View Interactive Output](https://stackblitz.com/edit/stackblitz-starters-uvkr8zuz?file=index.html)

---

## 📊 Dataset

- Initial restaurants scraped: **3,986**
- Final curated dataset: **3,356**
- 60+ structured variables
- Multilingual textual content normalized
- Enriched with:
  - Ratings
  - Reviews
  - Price level
  - Opening hours
  - Geolocation
  - Categories & tags

---

## ⚙️ Tech Stack

- Python
- Pandas / NumPy
- Scikit-learn
- Sentence-Transformers (SBERT)
- Google Places API
- OpenRouteService API
- Folium
- CRISP-DM methodology

---

## 📄 Project Summary Presentation

A concise executive summary of the project is available here:

[Download Presentation (PDF)](presentation/gastronomic_recommender_summary.pdf)

---

## 🚀 Key Contributions

- End-to-end recommender pipeline
- Multi-source data integration
- Semantic text modeling
- Context-aware filtering
- Practical implementation in tourism domain

---

## 📈 Future Improvements

- Domain-adapted semantic fine-tuning
- Demand prediction modeling
- Real-time API deployment
- User feedback integration (collaborative layer)

---

## 👤 Author

**Javier Piay**  
Industrial Engineer | Sports Data & AI  

🔗 Connect with me on [LinkedIn](https://www.linkedin.com/in/javier4piay)
