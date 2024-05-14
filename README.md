# GPT-Based Sentiment Analysis for Predicting Dow Jones Trends

### Contributors
- Hubery Hu
- Himal Pandey
- Mateo Velarde

### Currently, all codes are in the file TrainedModel.ipynb. Everything can be runned block by block in the jupyter notebook file.
We decide to keep everything in file at this point because it is the most convenient way to keep everything in place and push/pull through git.
We try to store model in the file but it is too big to push

## Project Overview

This project aims to harness the capabilities of AI, particularly GPT-based sentiment analysis, to predict the trends of the Dow Jones Industrial Average (DJIA). By analyzing the sentiment conveyed in historical news headlines, we seek to uncover correlations between public sentiment and stock market movements, thereby providing insights into potential future trends of the DJIA.

## Sentiment Analysis

Sentiment analysis is a computational task where the goal is to determine the sentiment or emotion expressed in a piece of text. This can range from customer feedback to social media posts. In this project, we aim to enhance sentiment analysis predictions by integrating labeling done through the ChatGPT language model. This leverages ChatGPT's advanced understanding of natural language to improve the accuracy and reliability of sentiment predictions for our dataset.

## Datasets

The project utilizes two primary channels of data:

### News Data
- **Source:** Historical news headlines crawled from the Reddit WorldNews Channel (/r/worldnews).
- **Period:** June 8, 2008, to July 1, 2016.
- **Details:** The dataset includes the top 25 headlines for each date, ranked by Reddit users' votes. The headlines are presented in a format that prioritizes the most relevant news items of the day.

### Stock Data
- **Metric:** Dow Jones Industrial Average (DJIA).
- **Period:** August 8, 2008, to July 1, 2016.
- **Source:** Data was sourced directly from Yahoo Finance.

### Data Files
Three .csv files are provided to facilitate the analysis:

1. **RedditNews.csv**
   - Columns: Date, News Headlines.
   - Each date includes the top 25 headlines, ranked based on their popularity.

2. **DJIA_table.csv**
   - Sourced from Yahoo Finance for comprehensive stock market data.

3. **Combined_News_DJIA.csv**
   - A merged dataset with 27 columns: Date, Label (indicating stock market movement), followed by columns Top1 to Top25 representing ranked news headlines.
   - This dataset is designed to simplify analysis for researchers, providing both news sentiment and stock market data in a single file.

## Technical Approach

### Data Preprocessing**
- **Data Concatenation and Cleaning:** Headlines are concatenated and cleaned to provide clear textual data for analysis.
- **Vectorization:** Text data is transformed into numerical data using CountVectorizer, with a limit of 5000 features to capture the most relevant words.
- **Label Encoding and Scaling:** Stock movement labels are encoded numerically, and data is scaled using MaxAbsScaler to maintain the sparsity of the dataset.

## Further Exploration: DJIA Prices Integration and Trend Analysis

This section covers the additional updates and enhancements made to the original project.

### Major Updates

1. **Integration of DJIA Prices in Training**:
   - The new project incorporates DJIA price information directly into the training process. This enhancement aims to improve the model's predictive capabilities by providing more comprehensive input data, combining both news sentiment and actual stock prices.

2. **Incorporation of Long-term and Short-term Trends**:
   - The model now considers both long-term and short-term trends of the DJIA. This dual approach allows the model to capture broader market movements as well as immediate reactions, potentially leading to more accurate and nuanced predictions.

### Project Files

- **Further_Implementation_of_Deep_Learning_Final_Project.ipynb**: This Jupyter notebook contains the updated model implementation. It includes data processing steps, training routines, and evaluation methods for the enhanced model that integrates DJIA prices and trends.


## Objective
The primary goal of this project is to demonstrate the potential of advanced sentiment analysis in predicting stock market trends. By correlating sentiment derived from global news headlines with the movements of the Dow Jones Industrial Average, we aim to provide a novel approach to understanding market dynamics.

## Training and Evalution

- **GPT-Based Model:** Leveraging the Hugging Face Transformers library, we implemented a GPT-2 model for sequence classification. This model is fine-tuned on our dataset to predict stock market trends based on news headline sentiment.

- **Training and Evaluation:** The models are trained on a split dataset and evaluated using accuracy and classification report metrics to understand their performance.

- **Data processing, training, and evaluation are all in the file TrainedModel.ipynb**  

## Related Work

This project is informed by several key studies that provide foundational insights into the relationship between public sentiment, as expressed through various media, and stock market movements.:

1. **Bollen, J., Mao, H., & Zeng, X.** (2011). "Twitter mood predicts the stock market." Journal of Computational Science.
2. **Li, X., et al.** (2014). "News impact on stock price return via sentiment analysis." Knowledge-Based Systems.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgement

- Data sourced from Kaggle: Stock Market Predictions (https://www.kaggle.com/datasets/tanishqdublish/stock-market-predictions).
- Models and tools provided by OpenAI's Transformers.
