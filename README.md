# Amazon_Vine_Analysis

## Purpose:
Analyze Amazon reviews written by members of the Amazon Vine program, and determine if there is bias toward favorable reviews.

## Overview
1. Define big data and describe the challenges associated with it.
2. Define Hadoop and name the main elements of its ecosystem.
3. Explain how MapReduce processes data.
4. Define Spark and explain how it processes data.
5. Describe how NLP collects and analyzes text data.
6. Explain how to use AWS Simple Storage Service (S3) and relational databases for basic cloud storage.
7. Complete an analysis of an Amazon customer review.

## Process
#### We started by taking our pre-created SQL tables, filtering and filling in the info with our raw data, and then making them into dataframes.

Dataframe from Customers table:

![customers](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/customers%20df.png)


Dataframe from the Products table:

![products](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/products%20df.png)


Dataframe from the Review ID table:

![reviewid](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/review%20id%20df.png)


Dataframe from the Vine table:

![vine](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/vine%20df.png)


Then, we took the completed dataframes and converted them back into SQL tables.

![customert](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/customers%20table.png)
![productst](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/products%20table.png)
![reviewidt](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/review%20id%20table.png)
![vinet](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/vine%20table.png)


## Results
After the tables were created, we performed calculations to determine the number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews of both Vine and non-Vine members.

![code_for_counts](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/code%20for%20counts.png)

- Number of Vine reviews: 170
- Number of non-Vine reviews: 37,840
- Number of 5-star ratings for Vine reviews: 65
- Number of 5-star ratings for non-Vine reviews: 20,612
- Percentage of 5-star ratings for Vine reviews: 38%
- Percentage of 5-star ratings for non-Vine reviews: 54%

To determine if there was bias toward favorable Vine-member reviews, we looked at the percentages of 5-star reviews for both Vine and non-Vine members. 

38% of reviews by Vine members were 5-stars.

![vineyes](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/yes%20vine%20-%205star%20percent.png)

54% of reviews by non-Vine members were 5-stars.

![vineno](https://github.com/charlagarcia/Amazon_Vine_Analysis/blob/main/resources/no%20vine%20-%205star%20percent.png)

## Summary
Overall, the numbers don't support any kind of bias toward Vine member reviews.  In fact, there is a lower percentage of 5-star ratings from Vine members than there are from regular customers.

We could do the same analysis with 1-star ratings to see if there is a bias on the other side.
