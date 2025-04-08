# BBC News Article Analysis and Summarization

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![NLTK](https://img.shields.io/badge/NLTK-3.7-green.svg)
![Hugging Face](https://img.shields.io/badge/HuggingFace-Transformers-yellow.svg)
![WordCloud](https://img.shields.io/badge/WordCloud-1.8.2-orange.svg)

## 📋 Project Overview

This project addresses the need to efficiently analyze and summarize textual information by developing a comprehensive document analysis and summarization system for BBC news articles. The system processes 500 BBC news articles across five categories, extracting valuable insights through statistical analysis, text mining, and automated summarization.

## 🔍 Features

- **Statistical Text Analysis**: Calculates metrics like word/sentence counts, average word/sentence lengths
- **Content Insights**: Identifies common words and phrases in each article
- **Automated Summarization**: Generates concise summaries using Facebook's BART model
- **Visual Representations**: Creates word clouds to visualize word frequency distributions
- **Comprehensive Output**: Exports all analysis results to a structured CSV file

## 🛠️ Technical Implementation

The system leverages Python's ecosystem of text processing libraries:

- **NLTK**: For text tokenization, stopword removal, and linguistic analysis
- **Pandas**: For efficient data manipulation and CSV processing
- **Hugging Face Transformers**: For implementing BART-based text summarization
- **WordCloud**: For generating word frequency visualizations 
- **Matplotlib**: For creating and displaying plots

The workflow includes:
1. Text preprocessing
2. Statistical metrics calculation
3. Word frequency analysis
4. Phrase extraction
5. Word cloud generation
6. Text summarization
7. Results compilation

## 📊 Sample Output

The analysis produces a comprehensive CSV with the following columns:
- `category`: News article category (business, politics, tech, etc.)
- `filename`: Original file identifier
- `title`: Article title
- `content`: Article text content
- `num_sentences`: Count of sentences in the article
- `num_words`: Count of words in the article
- `avg_word_length`: Average character length of words
- `avg_sentence_length`: Average number of words per sentence
- `common_words`: Most frequent words (excluding stopwords)
- `common_phrases`: Most common multi-word expressions

## 📁 Project Structure

```
├── NewsAnalysis.ipynb     # Main notebook with all code
├── bbc-news-data.csv      # Input dataset (tab-separated)
├── bbc_news_analysis.csv  # Output analysis results
└── README.md              # Project documentation
```

## 🔧 Usage

1. Clone the repository
2. Install required dependencies:
   ```
   pip install nltk pandas wordcloud matplotlib transformers
   ```
3. Download required NLTK resources:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   ```
4. Run the Jupyter notebook:
   ```
   jupyter notebook NewsAnalysis.ipynb
   ```

## 🧩 Core Components

### DocumentAnalyzer Class

The central engine of the system with methods for:
- Text statistics calculation
- Common word and phrase extraction
- Word cloud generation
- Text summarization using BART
- DataFrame processing

### Testing Suite

A comprehensive testing framework that validates all system components:
- Basic statistics calculation
- Common words and phrases extraction
- Text summarization functionality
- DataFrame processing operations
- Word cloud generation
