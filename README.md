Stock Movement Analysis Based on Social Media Sentiment
This repository comprehensively analyzes stock price movements based on sentiment extracted from Reddit discussions. Using advanced natural language processing techniques, the project combines sentiment analysis with stock market data to predict stock price trends and movement directions.

Project Structure
reddit_stock_raw.csv
Contains raw scraped data from Reddit, including discussion text and timestamps. Ensure the file is placed in the repository's root directory or update the path in the reddit_csv_path variable.

Required Columns:
Datetime: The timestamp of the Reddit post.
Discussion: The content of the discussion or post.
scraping_reddit_data.ipynb
A Jupyter Notebook that provides the code to scrape Reddit data for stock-related discussions. Use this notebook to collect fresh data from Reddit.

STOCK_MARKET_CLASS_AND_REGG.ipynb
The main Jupyter Notebook containing the core implementation for:

Preprocessing Reddit data.
Conducting sentiment analysis.
Merging sentiment data with stock price data.
Training machine learning models to predict stock price trends and directions.
Features
Sentiment Analysis
Utilizes two sentiment analysis approaches:

VADER Sentiment Analysis: Extracts polarity scores from the Reddit discussions.
Transformer-based Sentiment Analysis: Uses Hugging Face's pre-trained models to classify sentiment as Positive or Negative.
Stock Data Integration
Fetches historical stock price data using the yfinance library, incorporating technical indicators like SMA, EMA, RSI, and volatility.

Machine Learning Models

Regression: Predicts future stock prices.
Classification: Predicts stock price movement direction (up or down).
Visualization

Sentiment distribution.
Discussion trends over time.
Actual vs. predicted stock prices and directions.
Installation and Setup
Prerequisites
Ensure the following tools and libraries are installed:

Python 3.8+
Jupyter Notebook
Python libraries: pandas, numpy, nltk, yfinance, scikit-learn, xgboost, matplotlib, transformers
Install missing libraries using pip:

bash
Copy code
pip install pandas numpy nltk yfinance scikit-learn xgboost matplotlib transformers
Steps to Run
Clone the Repository
Clone this GitHub repository to your local machine:

bash
Copy code
git clone https://github.com/your-username/Stock-Movement-Analysis-Based-on-Social-Media-Sentiment.git
cd Stock-Movement-Analysis-Based-on-Social-Media-Sentiment
Prepare NLTK Data
The script automatically downloads the VADER lexicon during runtime. Ensure you have an active internet connection.

Prepare Reddit Data
Save your Reddit discussion data in a CSV file named reddit_stock_raw.csv and place it in the repository's root directory. The data should contain:

Datetime (timestamp): The date and time of the post.
Discussion (text): The content of the Reddit post.
Run the Scraping Notebook (Optional)
If you want to scrape fresh Reddit data, open the scraping_reddit_data.ipynb notebook and execute the cells.

Run the Analysis Notebook
Open the STOCK_MARKET_CLASS_AND_REGG.ipynb notebook in Jupyter Notebook or Jupyter Lab. Follow the instructions in the notebook to:

Preprocess Reddit data.
Conduct sentiment analysis.
Train and evaluate machine learning models.
View Results
The notebook outputs:

Metrics for regression and classification models.
Visualizations comparing actual vs. predicted stock prices and directions.
Sentiment distribution graphs.
