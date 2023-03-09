# Instacart-Basket-Analysis

![alt text](https://camo.githubusercontent.com/b2d93cc7b403e328b2b51fbee979b9efdff25330ab0781da01ad9933012fbfc2/68747470733a2f2f7777772e696e63696d616765732e636f6d2f75706c6f616465645f66696c65732f696d6167652f393730783435302f67657474795f3531383530343432365f323030303139363932303030393238303934315f3331393937362e6a7067)




# INTRODUCTION

Instacart aims to make it easy to do the shopping online with the touch of a button. Back in 2017, the company announced its first public dataset release, which is anonymized and contains a sample of over 3 million grocery orders from more than 200,000 Instacart users.



# PROBLEM STATEMENT

The task at hand for Instacart is two fold.



   1. Customer Profiling - Understanding the different customer segments and how their behaviour patterns differ from each other.

   2. Customer Targetting - Which segments to target to maximise profitability?

   3. Product Recommendations - Once target customers have been identified, what products to recommend?

# APPROACH AND CONCEPTS

**Data merging and data matrix creation** - Joined multiple tables to get final dataframe at a customer level with all individual product aisles as columns and values under those columns represeting the number of times customer bought from those aisles

**PCA** - Reduced data across 134 columns to 6 principal components explaining 51% of the original variance

**K-means clustering** - Used pc's to cluster segments into 3 distinct clusters backed by business intution and elbow plot

**Association based Recommender System 1** - Implemented the apriori algorithm using python generator functions, setting min support to 0.01 and filtering for lift values more than 10

**Recommender System 2**- Created a heuristic recommendation based on a products repeat ordering frequency from the ideal customer segment. Suggesting such products to target customers buying products with less repetition

# RESULTS

Target customers make up to 81% of the customer population and buy 3 times less often with half the basket size of the ideal customer

Recommender System 1 - Suggested complimentary products based on lift scores. Limitation - over 31% of transactions were coming from 4 aisles only namely Fresh Fruits, Fresh Vegetables, Packed Veg and Fruits and Yogurt

# LEARNINGS

Unlike in toy examples, you'd rarely ever be able to capture about 90% variance of the high dimensional data in 4-5 components. Need to make sound judgement on how many to keep. Scree plot helps, but still is only an approximation

Number of clusters to choose depends on the problem at hand. What is important is to keep the business context in mind and relate it back to the cluster attributes.

Apriori algorithm is computationally expensive and python generator functions provide a neat trick to avoid memory and computation overload

# REPOSITORY DETAILS

Access -


1. EDA

2. PCA and kmeans

3. Association Rule Mining - Generators

4. Customer Segments
