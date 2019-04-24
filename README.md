# Learning-to-Rank---Machine-Learning-and-Search-Queries

Class: Information Retrieval

Kaggle Competition for predicting relevance of search queries involving Home Depot products.

Each row of the data is a product-query pair along with an average relevance rating
For Example:
Product: Litton Lane 13 in. Gray Ceramic Rounded Decorative Vase (Set of 3)
Search Query: decorative vases
Relevance: 2.8

The rating signifies how relevant the search query is to the product:
3 - Highly Relevant
2 - Moderately Relevant
1 - Not Relevant

The goal of this project was to predict the relevance of a product-query pair.

This was very much a FEATURE ENGINEERING problem. Some features we created included the cosine similarity between the 
product name and the search query, word matches, number of words, brand matches, word count ratios, Jaccard Similarity, etc.

The machine learning portion involved a lot of hyperparameter tuning. We ended up using Gradient Boost as it gave us the highest 
accuracy on the test data.

Important Files:
- train_new : training data
- test_new : test data
- descriptions_new : full descriptions of all products
- attributes_new : attributes of all products including Brand names
- inverted_index_builder.ipynb : creates the inverted index for all products in the train/test sets
- Data Builder_revised.ipynb : This is where we create all of our data and features. The resulting table is exported to an excel spreadsheet.
- Model_evaluation.ipynb : This is where all of the machine learning takes place. We import our data table and try a bunch of different algorithms.