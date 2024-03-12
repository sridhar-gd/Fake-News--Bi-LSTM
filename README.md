**`FAKE NEWS DETECTION`**

This project aims to detect fake news using a dataset obtained from Kaggle. The dataset consists of 23,196 news titles and the target variable indicating whether the news is fake or not.

**`DATA DESCRIPTION`**

1. **Source**: Kaggle
2. **Size**: 23,196 news titles
3. **Target Variable**: Indicates whether the news is fake (binary classification)

**`LIBRARIES USED`**

1. Pandas
2. NumPy
3. NLTK
4. Regular Expression (re)
5. Keras

**`PREPROCESSING`**

1. Stemming was implemented using NLTK to reduce the words to their root forms.
2. One-hot representations were used to convert the textual data into numerical form for model training.

**`MODEL ARCHITECTURE`**

The model architecture used in this project is a Bidirectional Long Short-Term Memory (Bi-LSTM) neural network. Bi-LSTMs are capable of capturing long-term dependencies in sequential data by processing input sequences in both forward and backward directions. This architecture is particularly effective for tasks such as text classification and sentiment analysis.
The model consists of an embedding layer followed by a Bidirectional LSTM layer with 100 units. A dropout layer is added to prevent overfitting, and a dense layer with a sigmoid activation function is used for binary classification. The model is compiled with a Huber loss function and Adam optimizer.

**`TRAINING`**

The model was trained using the training dataset with the following specifications:

1. Loss function: Huber
2. Optimizer: Adam
3. Callbacks: Learning rate scheduler
4. Epochs: 100
5. Batch size: 32

**`EVALUATION`**

The accuracy of the model was evaluated on both the training and testing datasets. The accuracy achieved on the training dataset was 94.2%, while on the testing dataset, it was 80.25%.

**`CONCLUSION`**

This project demonstrates the effectiveness of machine learning techniques in detecting fake news. Further optimizations and improvements can be made to enhance the model's performance.

**`LICENSE`**

MIT License

Copyright (c) Year Full name

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
