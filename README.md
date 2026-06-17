# Amazon-Product-Analysis

## Introduction
Amazon is a multinational e-commerce company and has experienced a 41% decline in product purchases during its Prime Day event in 2025 compared to the previous year. As a result, both the Marketing and Sales departments at Amazon are looking to improve their customer experience. They seek the help of the Lead Data Analyst to provide them with a comprehensive product report which will examine the products carried by Amazon. The Marketing department will use this information to deliver product-specific digital promotion while the Sales department will use this information to suggest a range of products most suitable for every customer. 

## Research Questions
A product analysis will be performed for the marketing and sales departments with a focus on answering the following research questions.

### Question 1
How does the price, rating and discount compare for products belonging to different categories?
#### Purpose
Obtain an overview of the products sold by Amazon to make it easier to implement guided marketing and sales strategies.
#### Impact Hypothesis
When a sales employee is making efforts to sell a product to a future customer, the employee will have sufficient knowledge to answer any questions about the product, including questions relating to pricing and potential discounts.

### Question 2
How can the product characteristics be used to predict the product category?
#### Purpose 
Classify new products to ensure appropriate marketing and sales strategies are applied for market success. 
#### Impact Hypothesis
A member of the Marketing team is asked to curate digital content to promote a new product. In this case product category classifier models can be used to identify the already existing digital materials prepared for products belonging to the same category.

### Question 3  
How can product descriptions be used to identify similar products?
#### Purpose
Match new products to existing products for segmentation and recommendation strategies.
#### Impact Hypothesis 
A sales employee needs to find products similar to the one described by a customer using the product information retrieval models.

## Data
The Amazon Sales Dataset will be the primary source of data for this project. The dataset contains over 1000 authentic Amazon product records scraped using Python. The dataset contains 16 features, and Figure 1 provides an overview of the relevant characteristics of the dataset.

### Figure 1: Overview of Features

| Feature | Description | Name |
| ------------- | ------------- |-------------|
| product_name  | String containing product name  | Text |
| category  | Pipe separated string containing product categories  | Text |
| discounted_price  | Discounted price of product in Indian Rupees (INR)  | Numerical with units |
| actual_price  | Price of product in INR  | Numerical with units |
| discount_percentage  | Percentage discount on product  | Numerical with units |
| rating  | Rating of product from 1 to 5  | Ordinal, categorical |
| rating_count  |  Number of individuals who voted for a product rating | Numerical |
| about_product  | Description of product  | Text |

## Methodology

### Preliminary Analysis
Extract descriptive statistics such as means and frequencies. Compute correlations to observe potential relationships between variables. Visualize variable distributions to observe general trends and outliers using boxplots and histograms.

### Classification Models
Based on the results of the preliminary analysis, construct three different product category classifiers: a linear multinomial logistic regression model, and two non-linear classifiers: a k-nearest neighbours model and a decision tree model. Compare the three models using evaluation metrics such as accuracy, precision and recall.

### Information Retrieval Models
Construct multiple product information retrieval models using different text preprocessing techniques (stopword removal, lemmatization, etc.). Use TF and TD-IDF statistical weight measures to evaluate importance of words in both unigram and bigram models. Calculate accuracy, precision and recall to evaluate search relevance.
