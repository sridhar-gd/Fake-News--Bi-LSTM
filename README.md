<p align="center"><img width=100% src="https://github.com/sridhar-gd/sridhar-gd/blob/main/Banner.png"></p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Python](https://img.shields.io/badge/python-v3.11+-blue.svg)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


# FAKE NEWS DETECTION

The objective of this project is to accurately identify and filter out misleading or false information from reliable sources. This is crucial in maintaining the integrity of news dissemination and preventing the spread of misinformation. By utilizing deep learning techniques and NLP, we can analyze text data, understand context, and classify news articles as either real or fake


## Table of Contents

1. Data Description
2. Data Preprocessing
3. Model Architecture
4. Model Training
5. Model Evaluation
6. Deployment
7. License


## Data Description

The dataset consists of 23,196 news titles and the target variable indicating whether the news is fake or not.
- title: title of the article.
- news_url: URL of the article.
- source domain: web domain where article was posted.
- tweet_num: number of retweets for this article.
- real: label column, where 1 is real and 0 is fake.


## Data Preprocessing

- Removing punctuations, stop words, and converting the upper case letters to lower case letters.
- Stemming was implemented using NLTK to reduce the words to their root forms.
- One-hot representations were used to convert the textual data into numerical form for model training.
- Padding to ensure that all the indexes were of equal length.


## Model Architecture

The model architecture used in this project is a Bidirectional Long Short-Term Memory (Bi-LSTM) neural network. Bi-LSTMs are capable of capturing long-term dependencies in sequential data by processing input sequences in both forward and backward directions. This architecture is particularly effective for tasks such as text classification and sentiment analysis.
The model consists of an embedding layer followed by a Bidirectional LSTM layer with 100 units. A dropout layer is added to prevent overfitting, and a dense layer with a sigmoid activation function is used for binary classification. The model is compiled with a Huber loss function and Adam optimizer.


## Model Training
X represented the independent variables (i.e., the headlines) and y represented the target/dependent variable (i.e., the kind of news)
The model was trained using the training dataset with the following specifications:

- Loss function: Huber
- Optimizer: Adam
- Callbacks: Learning rate scheduler
- Epochs: 100
- Batch size: 32


## Model Evaluation

The accuracy of the model was evaluated on both the training and testing datasets. The accuracy achieved on the training dataset was 94.2%, while on the testing dataset, it was 80.25%.


## Deployment

Taking the model from development to deployment, Flask - a powerful web framework for Python - was utilized.


## License

MIT License

Copyright (c) 2024 Sridhar GD

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
