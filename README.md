# Product Recommendation System

A hybrid product recommendation system built using Walmart e-commerce product data. The project combines **content-based filtering, collaborative filtering, and popularity-based recommendations** to generate relevant product suggestions.

## Overview

Recommendation systems help users discover products by analysing product characteristics, user preferences, and interaction patterns.

This project implements multiple recommendation approaches and combines them into a hybrid recommendation framework:

* **Content-Based Filtering** – Recommends products similar to a selected product based on product attributes.
* **Collaborative Filtering** – Uses user-item interactions to identify products based on similar user preferences.
* **Popularity-Based Recommendations** – Identifies trending or highly rated products based on product ratings and review information.
* **Hybrid Recommendations** – Combines recommendations from multiple approaches to generate relevant product suggestions.

## Dataset

The project uses Walmart e-commerce product data containing product information such as:

* Product ID
* Product Name
* Category
* Brand
* Product Description
* Product Rating
* Product Review Count
* Product URL

The product attributes are processed to create feature representations used for similarity-based recommendations.

## Methodology

### 1. Data Preprocessing

The dataset is cleaned by handling missing values and standardising relevant product attributes.

The following attributes are used for product representation:

* Category
* Brand
* Description

## 2. NLP-Based Feature Engineering

Natural Language Processing is applied using **spaCy** to preprocess product information.

The preprocessing pipeline includes:

* Text normalisation
* Tokenisation
* Stop-word removal
* Extraction of relevant textual tokens

The processed product attributes are combined to create a product feature representation.

## 3. Content-Based Filtering

Content-based recommendations are generated using:

* **TF-IDF Vectorization**
* **Cosine Similarity**

Product category, brand, and textual descriptions are transformed into TF-IDF representations. Cosine similarity is then used to identify products with similar attributes.

The system returns the most similar products for a selected item.

## 4. Collaborative Filtering

Collaborative filtering is implemented using a **user-item interaction matrix**.

The workflow includes:

1. Creating a user-item matrix.
2. Calculating similarity between users using cosine similarity.
3. Identifying users with similar interaction patterns.
4. Recommending products based on similar-user preferences.

## 5. Popularity-Based Recommendations

Products are ranked using available product ratings and review information to identify highly rated and popular products.

This provides recommendations for users without sufficient interaction history and can act as a baseline recommendation approach.

## 6. Hybrid Recommendation System

The hybrid recommendation system combines outputs from multiple recommendation approaches:

* Content-based recommendations
* Collaborative filtering recommendations
* Popularity-based recommendations

Duplicate products are removed before generating the final recommendation list.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* spaCy
* Matplotlib
* Seaborn
* SciPy

## Key Concepts Used

* Recommendation Systems
* Content-Based Filtering
* Collaborative Filtering
* Hybrid Recommendation Systems
* Natural Language Processing
* TF-IDF Vectorization
* Cosine Similarity
* User-Item Interaction Matrix
* Data Preprocessing

## Project Structure

```text
Product-Recommender-System-Walmart/
│
├── Untitled.ipynb
├── walmart_ca-ecommerce_product_details__20190101_20190208_sample.csv
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/s-chandra0420/Product-Recommender-System-Walmart.git
```

Navigate to the project directory:

```bash
cd Product-Recommender-System-Walmart
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn spacy scikit-learn scipy
```

Download the spaCy English language model:

```bash
python -m spacy download en_core_web_sm
```

Run the Jupyter Notebook:

```bash
jupyter notebook Untitled.ipynb
```

## Future Improvements

Potential improvements include:

* Using a larger product catalogue.
* Creating realistic user-product interaction data.
* Implementing weighted hybrid ranking.
* Evaluating recommendation quality using metrics such as Precision@K, Recall@K, and Hit Rate.
* Building an interactive web interface for product recommendations.
* Deploying the recommendation system as a web application.

## Author

**Shatakshi Chandra**

MBA – Business Analytics (BITS Pilani) | B.Tech – Information Technology (IIIT Bhubaneswar)

[LinkedIn](https://www.linkedin.com/in/shatakshi-chandra-6a034124a/)
