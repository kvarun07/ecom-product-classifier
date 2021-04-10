# ecom-product-classifier
This repository was submitted for MIDAS Summer Internship Recruitment 2021 Task-3 (NLP).

[Varun Khurana](mailto:varun19124@iiitd.ac.in) \
CSE, Indraprastha Institute of Information Technology, Delhi

### Task
We are given a dataset containing information about some products sold on an e-commerce site. Our task is to predict product categories by extracting features from the product descriptions. In essence, it is a classification problem.

### Approach/Work Flow
- Cleaning the data
- Follow 'Bag of Words' model: Count Vectorisation followed by computing Term Frequency-Inverse Document Frequency.
- Different Classification algorithms tried to determine which one of them gave the highest accuracy when run on testing data.

#### Cleaning the data
1. Removing punctuation
2. Converting text data to lower case
3. Stripping leading and trailing whitespaces
4. Removing stopwords

After these steps, most frequent product categories are identified. Entries having other categories are removed due to lack of sufficent data.
The most common product categories can be visualised in the form of wordcloud as shown below:
![alt text](https://github.com/kvarun07/ecom-product-classifier/blob/main/assets/category_wordcloud.png)


