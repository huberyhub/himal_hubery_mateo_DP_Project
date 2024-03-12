## GPT-Based Sentiment Analysis for Predicting Dow Jones Trends

# Hubery Hu, Himal Pandey

# Project Overview

This project aims to harness the capabilities of AI, particularly GPT-based sentiment analysis, to predict the trends of the Dow Jones Industrial Average (DJIA). By analyzing the sentiment conveyed in historical news headlines, we seek to uncover correlations between public sentiment and stock market movements, thereby providing insights into potential future trends of the DJIA.

# Sentiment Analysis

Sentiment analysis is a computational task where the goal is to determine the sentiment or emotion expressed in a piece of text. This can range from customer feedback to social media posts. In this project, we aim to enhance sentiment analysis predictions by integrating labeling done through the ChatGPT language model. This leverages ChatGPT's advanced understanding of natural language to improve the accuracy and reliability of sentiment predictions for our dataset.

# Datasets

The project utilizes two primary channels of data:

News Data
Source: Historical news headlines crawled from the Reddit WorldNews Channel (/r/worldnews).
Period: June 8, 2008, to July 1, 2016.
Details: The dataset includes the top 25 headlines for each date, ranked by Reddit users' votes. The headlines are presented in a format that prioritizes the most relevant news items of the day.
Stock Data
Metric: Dow Jones Industrial Average (DJIA).
Period: August 8, 2008, to July 1, 2016.
Source: Data was sourced directly from Yahoo Finance.
Data Files
Three .csv files are provided to facilitate the analysis:

RedditNews.csv
Columns: Date, News Headlines
Each date includes the top 25 headlines, ranked based on their popularity.
DJIA_table.csv
Sourced from Yahoo Finance for comprehensive stock market data.
Combined_News_DJIA.csv
A merged dataset with 27 columns: Date, Label (indicating stock market movement), followed by columns Top1 to Top25 representing ranked news headlines.
This dataset is designed to simplify analysis for researchers, providing both news sentiment and stock market data in a single file.
Objective

Source: https://www.kaggle.com/datasets/tanishqdublish/stock-market-predictions

The primary goal of this project is to demonstrate the potential of advanced sentiment analysis in predicting stock market trends. By correlating sentiment derived from global news headlines with the movements of the Dow Jones Industrial Average, we aim to provide a novel approach to understanding market dynamics.

