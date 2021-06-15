# Amazon_Vine_Analysis

## Overview of the Analysis:

I have been asked with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, I will have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I will have to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I will use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset.

## Resources:

- Data Sources: challenge_schema.sql, Amazon Review dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Electronics_v1_00.tsv.gz
- Software: AWS RDS and S3, PostgreSQL 13 PGAdmin 4, Google Colaboratory, Python 3.83

## Results:

How many Vine reviews and non-Vine reviews were there?

There were a total of 50,753 reviews. Out of those only 1,080 were Vine and the rest (49,673) were non-Vine.

![total_vine_nonvine.png](https://github.com/DanielGandia/Amazon_Vine_Analysis/blob/main/Images/total_vine_nonvine.png)

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

There were 23,497 total reviews with 5 star rating. The vast majority (23,043) were non-Vine and only 454 were Vine.

![5_star_reviews.png](https://github.com/DanielGandia/Amazon_Vine_Analysis/blob/main/Images/5_star_reviews.png)

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- Percentage of 5-star reviews out of total Vine reviews: 42.04%

- Percentage of 5-star Vine out of all 5-star reviews: 1.93%

- Percentage of 5-star non-Vine out of total non-Vine reviews: 46.39%

- Percentage of 5-star reviews out of total non-Vine reviews: 98.07%

![percentage_of_vine_nonvine.png](https://github.com/DanielGandia/Amazon_Vine_Analysis/blob/main/Images/percentage_of_vine_nonvine.png)

## Summary:

After reviewing the results provided above, it would be concluded that there is a positivity bias in the Vine Program. There are quite a few more 5-star non-Vine reviews.

Another analysis that could be done with this dataset would be to find out what the percentage of the Vine and non_Vine are in relation to the verified_purchases column to see if there is a positivity bias.
