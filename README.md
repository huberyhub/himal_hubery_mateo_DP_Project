# GPT-Based Sentiment Analysis for Predicting Dow Jones Trends

### Contributors
- **Hubery Jiarui Hu**
- **Himal Pandey**
- **Mateo Velarde**

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Sentiment Analysis](#sentiment-analysis)
3. [Datasets](#datasets)
4. [Technical Approach](#technical-approach)
5. [Objective](#objective)
6. [Training and Evaluation](#training-and-evaluation)
7. [New Project: DJIA Prices Integration and Trend Analysis](#new-project-djia-prices-integration-and-trend-analysis)
8. [Related Work](#related-work)
9. [License](#license)
10. [Acknowledgements](#acknowledgements)

---

## Project Overview

This project leverages the power of AI, particularly GPT-based sentiment analysis, to predict the trends of the Dow Jones Industrial Average (DJIA). By analyzing the sentiment conveyed in historical news headlines, we aim to uncover correlations between public sentiment and stock market movements, providing insights into potential future trends of the DJIA.

---

## Sentiment Analysis

Sentiment analysis involves determining the sentiment or emotion expressed in a piece of text, such as customer feedback or social media posts. In this project, we enhance sentiment analysis predictions by integrating labeling done through the ChatGPT language model, leveraging its advanced understanding of natural language to improve the accuracy and reliability of sentiment predictions for our dataset.

---

## Datasets

### News Data
- **Source**: Historical news headlines crawled from the Reddit WorldNews Channel (/r/worldnews).
- **Period**: June 8, 2008, to July 1, 2016.
- **Details**: The dataset includes the top 25 headlines for each date, ranked by Reddit users' votes, presenting the most relevant news items of the day.

### Stock Data
- **Metric**: Dow Jones Industrial Average (DJIA).
- **Period**: August 8, 2008, to July 1, 2016.
- **Source**: Data sourced directly from Yahoo Finance.

### Data Files
1. **RedditNews.csv**
   - Columns: Date, News Headlines.
   - Contains the top 25 headlines for each date, ranked by popularity.

2. **DJIA_table.csv**
   - Comprehensive stock market data sourced from Yahoo Finance.

3. **Combined_News_DJIA.csv**
   - A merged dataset with 27 columns: Date, Label (indicating stock market movement), followed by columns Top1 to Top25 representing ranked news headlines.

---

## Technical Approach

### Data Preprocessing
- **Data Concatenation and Cleaning**: Headlines are concatenated and cleaned to provide clear textual data for analysis.
- **Vectorization**: Text data is transformed into numerical data using CountVectorizer, with a limit of 5000 features to capture the most relevant words.
- **Label Encoding and Scaling**: Stock movement labels are encoded numerically, and data is scaled using MaxAbsScaler to maintain the sparsity of the dataset.

---

## Objective

The primary goal of this project is to demonstrate the potential of advanced sentiment analysis in predicting stock market trends. By correlating sentiment derived from global news headlines with the movements of the Dow Jones Industrial Average, we aim to provide a novel approach to understanding market dynamics.

---

## Training and Evaluation

- **GPT-Based Model**: Leveraging the Hugging Face Transformers library, we implemented a GPT-2 model for sequence classification, fine-tuned on our dataset to predict stock market trends based on news headline sentiment.

- **Training and Evaluation**: The models are trained on a split dataset and evaluated using accuracy and classification report metrics to understand their performance.

- **Data processing, training, and evaluation**: All steps are detailed in the file `TrainedModel.ipynb`.

---

## Final Project: DJIA Prices Integration and Trend Analysis

### Major Updates

1. **Integration of DJIA Prices in Training**:
   - Incorporates DJIA price information directly into the training process to improve the model's predictive capabilities by combining both news sentiment and actual stock prices.

2. **Incorporation of Long-term and Short-term Trends**:
   - Considers both long-term and short-term trends of the DJIA, allowing the model to capture broader market movements as well as immediate reactions for more accurate and nuanced predictions.

### Project Files

- **DeepLearning_FinalProject_Pt.2.ipynb**: This Jupyter notebook contains the updated model implementation, including data processing steps, training routines, and evaluation methods for the enhanced model integrating DJIA prices and trends. Run the code in sequence to train, execute, and evaluate the model. The code was completed in Colab.

### Objectives

- **Enhanced Predictive Accuracy**: By combining sentiment analysis with historical stock prices, the model aims to deliver more accurate predictions of stock market trends.
- **Comprehensive Market Analysis**: Incorporating both long-term and short-term trends provides a more complete analysis of market dynamics.

### Future Work

- **Further Fine-tuning**: Continue fine-tuning the model with additional data and hyperparameter adjustments to optimize performance.
- **Feature Expansion**: Explore the inclusion of other financial indicators and alternative data sources to further enrich the model's input.

---

## Related Work

This project is informed by several key studies that provide foundational insights into the relationship between public sentiment, as expressed through various media, and stock market movements:

1. **Bollen, J., Mao, H., & Zeng, X.** (2011). "Twitter mood predicts the stock market." Journal of Computational Science.
2. **Li, X., et al.** (2014). "News impact on stock price return via sentiment analysis." Knowledge-Based Systems.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgements

- **Data sourced from Kaggle**: Stock Market Predictions (https://www.kaggle.com/datasets/tanishqdublish/stock-market-predictions).
- **Models and tools**: Provided by OpenAI's Transformers.

---
