# scraper-curation


This script is a component of a larger webscraper and content curation project focused on **automating news collection, evaluation, and ranking** using modern NLP techniques.

**What It Does**

- **Scrapes Google News** for the latest articles on a given topic.
- **Extracts** key information: title, snippet, source, date, and link.
- **Calculates semantic similarity** between all articles using TF-IDF and cosine similarity.
- **Ranks articles** by their average similarity to the rest—identifying the most “central” or “hot” stories in the news cluster.

## **Key Libraries Used**

- `requests` — HTTP requests for web scraping
- `beautifulsoup4` — HTML parsing and extraction
- `scikit-learn` (`TfidfVectorizer`, `cosine_similarity`) — NLP vectorization and similarity computation
- `numpy` — Numeric operations

## **Main Functions**

- `scrape_google_news(query, num_results=20)`:  
  Scrapes Google News for a given search query and returns a list of articles with their metadata.

- **TF-IDF Similarity Calculation:**  
  Prepares article texts, vectorizes them, computes pairwise cosine similarity, and calculates the average similarity for each article.

- **Ranking:**  
  Attaches the average similarity score to each article and sorts the articles by this score in descending order.

## **How to Use**

1. Set your topic in the script (e.g., `"artificial intelligence"`).
2. Run the script.  
   It will print out a ranked list of news articles, with those most similar to the cluster at the top.

