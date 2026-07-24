[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/D94-Q8ry)



# AI-Driven Financial News Sentiment & Stock Market Prediction

An end-to-end Machine Learning and NLP pipeline designed to analyze financial news sentiment and evaluate its impact on daily stock price movements and trade volume.

---

### Project Overview

In modern financial markets, stock movements are heavily influenced by news and investor sentiment. This project combines quantitative market indicators (Open, High, Low, Close prices, and Volume) with Natural Language Processing (NLP) embeddings of daily financial news articles to improve stock trend prediction and risk analysis.

---

### Importing Libraries

The project uses the following core stack:

* **Data Manipulation & Processing**: `pandas`, `numpy`, `scipy`
* **Visualization**: `matplotlib`, `seaborn`
* **NLP & Text Embeddings**: `gensim` (Word2Vec), `sentence-transformers`, `transformers`
* **Machine Learning**: `scikit-learn` (`RandomForestClassifier`, `train_test_split`, classification metrics)
* **Deep Learning**: `torch`, `tensorflow`, `keras` (`Sequential`, `Dense`, `Dropout`)

---

### Data Processing & Exploratory Analysis

* **Data Cleaning**: Verified zero null values and zero duplicate records across the dataset.
* **Temporal Formatting**: Converted string dates to `datetime64` for chronological sorting and time-series aggregation.
* **Feature Engineering**:
* Calculated news length (`news_length` in words) to measure headline verbosity.
* Aggregated monthly price averages and trade volumes (`YearMonth`).


* **Text Representation**: Encoded financial news text into dense vector representations using `Word2Vec` and `SentenceTransformers`.

---

### Model Details

The modeling architecture integrates tabular stock features with dense news embeddings:

1. **Random Forest Classifier**: Machine learning ensemble used for baseline multi-class sentiment and market feature classification.
2. **Dense Neural Network (DNN)**: Keras multi-layer perceptron utilizing `Dense` layers and `Dropout` regularization to prevent overfitting.
3. **Evaluation Metrics**: Models were evaluated using **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **Confusion Matrices**.

---

### Conclusion

* Combining news sentiment polarity (`-1`: Negative, `0`: Neutral, `1`: Positive) with technical market metrics provides superior market insight over price history alone.
* News sentiment spikes correlate directly with localized stock price volatility and trading volume spikes.
* Automated NLP feature extraction significantly reduces the time required for analysts to evaluate news impact.

---

### Future Scope

* **Domain-Specific LLMs**: Fine-tune financial Large Language Models such as **FinBERT** or **Llama-3-Financial** for deeper sentiment extraction.
* **Sequential Architectures**: Implement time-series models (**LSTM / GRU / Transformer**) to capture long-term temporal trends.
* **Real-Time Deployment**: Build a **FastAPI** pipeline connected to live news APIs (e.g., Alpha Vantage, NewsAPI) for real-time market inference.
