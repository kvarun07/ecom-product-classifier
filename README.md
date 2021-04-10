# ecom-product-classifier
This repository was submitted for [MIDAS IIIT-D](http://midas.iiitd.edu.in/) Summer Internship Recruitment 2021 Task-3 (NLP).

[Varun Khurana](mailto:varun19124@iiitd.ac.in) \
CSE, Indraprastha Institute of Information Technology, Delhi

## Task
We are given a dataset containing information about some products sold on an e-commerce site. Our task is to predict product categories by extracting features from the product descriptions. In essence, it is a classification problem.

## Approach/Work Flow
- Cleaning the data
- Follow ***'Bag of Words'*** model: Count Vectorisation followed by computing Term Frequency-Inverse Document Frequency.
- Different Classification algorithms tried to determine which one of them gave the highest accuracy when run on testing data.

### Cleaning the data
1. Removing punctuation
2. Converting text data to lower case
3. Stripping leading and trailing whitespaces
4. Removing stopwords

After these steps, most frequent product categories are identified. Entries having other categories are removed due to lack of sufficent data.
The most common product categories can be visualised in the form of wordcloud as shown below:
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/category_wordcloud.png)

### Perform Count Vectorisation followed by Term-Frequency and Inverse Document Frequency (TF-IDF)
- Here, our goal is to effectively extract features from the text product description so that a product category can be predicted.
- We first obtain the sentence vectors by applying count vectorisation.
- Thereafter, we compute the TF-IDF to get obtain weighted vectors such that more weight is given to particular words that form a distinguishing feature for a category.

### Applying different Classification Algorithms
1. Naive Bayes Classifier
2. Logistic Regression
3. Support Vector Machine
4. Classification with Neural Network

***Construction of Neural Network:*** 
- The NN contains 2 hidden layers.
- The ***ReLU (Rectified Linear Unit)*** is used as the activation function.
- The output layer consists of as many number of nodes as the number of product categories.
- In the output layer, the ***softmax function*** is used as the activation function so that each node gives the probability of a product belonging to that category. The category with the highest probability is selected as the predicted category.

Following are the ***Accuracy and Loss Curves*** obtained as the model was run for 15 epochs!
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/nnet_accuracy_curve.png)
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/nnet_loss_curve.png)

Here is the ***Confusion Matrix*** obtained for the NN model:
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/nnet_confusion_matrix.png)

## Results
| Classification Approach | Accuracy ( % ) |
| :-: | :-: |
| Naive Bayes | 81.31 |
| Logistic Regression | 94.17 |
| Support Vector Machine| 97.36 |
| **Neural Network** | ***97.58*** |


Clearly, the highest accuracy for predicting product categories is obtained by the ***Neural Network model***.
\
The relative performance of each classification model can be visualised as follows:
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/model_comparison.png)



