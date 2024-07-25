# Post Label Predictor

PostLabelPredicter is a machine learning model trained on the 20NewsGroups dataset. It predicts which of the 20 predefined labels an email or forum post belongs to. The model is designed as an educational resource to walk users through the process of building a text classification model using `scikitlearn`'s built-in tools and datasets.

## Background
The 20NewsGroups dataset is a popular dataset for text classification and clustering. It contains around 20,000 newsgroups posts, partitioned across 20 different newsgroups.

This project aims to utilize this dataset to build a limited text (forum post) classification model. The project is presented in a single Python notebook, making it easy to follow and understand the various stages of data preprocessing, model training, and evaluation.

## Usage
To explore the project, simply open the provided Jupyter notebook:

```
jupyter notebook PostLabelPredicter.ipynb
```

Follow the steps outlined in the notebook to understand the data preprocessing, model training, and evaluation process.

### Data Preprocessing
The dataset was preprocessed to clean and standardize the text data:

1. Removed stop words and symbols.
2. Separated each key-value pair in the text into corresponding row-columns.
3. Removed metadata fields (keywords and nntp_posting_host) to prevent skewing the classifier.

### Model Training
The notebook covers the following steps in model training:

1. Vectorizing each column using TF-IDF, then recombining vectors to achieve column-distinct weighting.
2. Training a classifier (e.g., XGBoost) on the preprocessed data.
3. Evaluating the model via hyperparameter tuning with GridSearchCV (in this case, 36 permutations were compared).

License
This project is licensed under the MIT License. See the LICENSE file for more details.
