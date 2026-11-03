# Data-Science-Pipeline-Project


### Prerequisites
Use the following Python packages in a Jupyter Notebook environment to complete the code portion of this project:  
  - scikit-learn  
  - numpy  
  - pandas  
  - spacy

Local Machine Instructions

Before editing the starter notebook for your project, ensure you install the requirements necessary for the project. This can be done by first cloning the repository and then performing a pip install with the provided requirements.txt

For example:
```
# Install requirements
python -m pip install -r requirements.txt

# You may need to specify to use Python3
python3 -m pip install -r requirements.txt
```

Note: To install spaCy, it may be dependent on your machine (especially if using a Mac). It's possible that the `requirements.txt` file does not work for your setup. You will need to look up your machine type and use the appropriate pip install from spaCy's page: [spacy.io](https://spacy.io/usage)

For example, for a Mac M1 chip you would need to run:
```
python -m pip install 'spacy[apple]'
```

Then you should be able to use follow the above instructions forpip install -r requirements.txt

--------------------


### StyleSense Recommendation System
#### Project Overview

This project builds a machine learning pipeline to predict whether a customer would recommend a product based on their review, age, and product details. The pipeline automates the process of analyzing reviews and provides valuable insights for StyleSense.

#### Features

  - Handles numerical, categorical, and text data.
  - Extracts advanced NLP features (POS tags and named entities).
  - Includes a Streamlit dashboard for data exploration and predictions.

#### Installation

1. Clone the repository:  
  `git clone https://github.com/your-repo/dsnd-pipelines-project.git`


#### Files
- `starter.ipynb` - the main notebook file
- `data\reviews.csv` - review data file

--------------------

### Pipeline

Raw Data is first preprocessed by the Feature Engineering function to create `combined_text` and `review_length` features. Data is then passed to the ColumnTransformer which preprocess the data by type: numberical features, categorical features and text. it is then passed to the Logistic Regression model to fit and make predictions.


```text
|Raw Data
|    ↓
|Feature Engineering
|    ├─ review_length
|    └─ combined_text
|    ↓
|ColumnTransformer
|    ├─ Numerical Processing
|    ├─ Categorical Processing
|    └─ spaCy + TF-IDF
|    ↓
|Logistic Regression
|    ↓
|Prediction
```

### Scenario: Fashion Forward Forecasting

You've recently joined "StyleSense", a rapidly growing online women's clothing retailer, as a data scientist. StyleSense is known for its trendy and affordable fashion, and its customer base has exploded in recent months. This influx of new customers is fantastic for business, but it has created a challenge: a backlog of product reviews with missing data. Customers are still leaving valuable feedback in the text of their reviews, but they aren't always indicating whether they recommend the product.

Your first task at StyleSense is to leverage the existing data– those reviews with complete information – to build a predictive model.

This model will analyze the text of a review, the customer's age, the product category, and other relevant information to predict whether or not the customer would recommend the product. By automating this process, you'll help StyleSense gain valuable insights into customer satisfaction, identify trending products, and ultimately provide a better shopping experience for their growing customer base.

The future of fashion forecasting is in your hands!



