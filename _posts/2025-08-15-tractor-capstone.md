---
title: "Preventing Store Cancellations Before They Even Happen Using Predictive Analytics"
permalink: /tractor-capstone-post/
date: 2025-08-15
categories: blog
layout: single
tags: [data science, portfolio, supply chain, retail]
excerpt: "My Machine Learning Capstone at Tractor Supply Co."
header:
  overlay_image: /assets/images/smartretail.jpg
  overlay_filter: 0.30
---

### Background
Imagine a scenario when you are shopping online for horse feed to feed your horses. You go online to check if your nearest rural supplier has some in stock so that you can buy a couple of units to pick up later during the day after work. Luckily, the website states that there are some units in stock, so you place your order, and you move on about your day. A couple of hours later you are sent a message saying that your order cannot be fulfilled any longer. This raises a problem with hurting revenue but also creates a bad experience with digital customers through the BOPIS (“Buy Online Pickup In Store”) channel. BOPIS has been a very popular fulfillment method in modern retail, and it is only continuing to grow and establish itself as the common mode of purchase. Therefore, a big emphasis must be put into making sure the BOPIS pipeline is streamlined and reliable to maximize margins and uphold a good customer shopping experience.

This problem is large in scale and needs a systematic solution. There are over 2,300 physical stores throughout the country, of various sizes and in different regions, being serviced by 10 different distribution centers. Moreover, a physical store comprises of over 30,000 unique products, from horse feed, powertools, pet food, to clothing and lawn care. Lastly, as Tractor Supply Company is a Fortune 500 company, the company stores over millions of sales data, which is good for model training but would require a clean, streamlined and scalable ETL process.

### Solution Proposal
As an Omni-channel Ops Intern, I was presented with the problem statement and was **tasked to implement a machine learning approach to help mitigate the loss of dollars** from BOPIS cancellations by predicting the probability that SKUs (or products) might get cancelled at any given store and at any given time. From this we can selectively hide certain store-item inventory in a buffering approach from the company’s website when the risk of a fulfillment failure is high, protecting them from a bad experience of cancelled orders. 

### Data ETL
Tractor Supply uses the Snowflake data lake to store its data. I quickly realized that because of the scale that tractor supply operates, it did not make sense to extract sales data to my local computer to train ML models locally, which would have been costly both in time and computing resources, not to mention a security risk. In my project setup phase, I realized the system had to somehow overcome this challenge. This is where I discovered snowflake ML, a library of scikit-learn wrappers which are capabilities within Snowflake that mimic ML methods under the scikit-learn banner. I also learned of the Snowpark API, a library in Snowflake that enables you to query and process data at scale within Snowflake using Python and SQL. By using these two libraries, I can **connect to the enterprise database tables and perform heavy data transformation and model training in the data cloud itself**. This increased overall productivity, upheld data security and enabled me to focus on the data science work.

### Data Science
This is the fun part. The core solution is a supervised learning model that predicted the probability that a given store-item will result in an inventory-related cancellation. The main goal of the machine learning model was to assign a risk probability for a particular SKU for a particular store and week. To do this, I trained a classifier model on both booked and cancelled sales data. The model then learned intricate patterns and trends, being able to distinguish between both. I defined early that **a well-trained classifier can then flag high-risk store-item pairs before an order is even placed**.

The machine learning engine I ended up working with is the XGBClassifier because of robustness, interpretability, and its good performance with class imbalance and tabular data. I also considered other models such as the LGBMClassifier and the CategoricalNB, but preliminary testing showed that both did not perform as well.

### Preprocessing and Training
The main features I used to train my models were temporal data, such as week number and season. I also used store information, such as region, the size of the sales floor, and store location. Lastly, SKU characteristics were used, such as what category it was in. Later down the model training process, I also feature engineered new features, such as flags for certain item groups and high velocity items.

Sampling is done through SQL scripts using Snowpark. Initial exploratory data analysis showed that successful sales dominated cancelled sales, so training data must reflect that imbalance. Training and evaluation sets were prepared with a ratio of 1:12 of roughly 1 million orders. During this stage, I ruled out fraud cancellations as noise, as it pertained more towards a customer’s purchasing power, not TSC’s intricate supply chain processes that might incite cancellations through the BOPIS channel. Hyperparameter tuning was also applied to determine the best combination of learning rate and number of boosters to further boost performance.

### Evaluation and Results
BOPIS cancellations are so rare compared to the volume of successful BOPIS orders, which introduced the problem of class imbalance in the dataset I used to train our model. Therefore, **I used the recall and F2 score to measure how well the model is learning from the data** to account for this problem. The best that we can make the recall score of the model against the testing set means that we have successfully trained a model that finds the intricate patterns to be able to distinguish between a normal sale and a BOPIS-cancel sale. When a model is good enough in this way, then we can be confident that the risk probabilities are grounded and reasonable (based on historical data).

After numerous trainings, feature engineering, implementing sampling, class imbalance, and adding hyperparameter tuning, my **best model had an accuracy of 71%, recall of 77%, and ROC-AUC of 81%**. The evaluation method randomly grabs 1,000 orders from the data lake, 150 of which are BOPIS cancellations. We have finally built a machine learning model that assigns a probability risk to a given SKU at a particular store in a particular week. But how do we translate these risk probabilities to buffers that prevent cancellations from happening on the website?

### Buffer System
The buffering system works by taking risk probabilities from the model and **assigns how many units are protected from being bought from the website for all 30,000 products across 2,300 stores**. This system treats risk differently depending on the item category. The system also treats risk differently based on the price of the item. This system is designed in a way to enable us to tweak how aggressive we want the buffering will be. Moreover, I've designed the system to be modular and open to new features as new needs are defined. At the conclusion of my internship, I was able to run my model and system through some simulated deployments with real-world data. Because this system is intended to be used conservatively, the implementation of this system has an **impact of up to $3M annually**.

Supply chain and retail can benefit greatly from the implementation of machine learning solutions. In this instance, I was able to implement a classic solution with a cloud computing twist that can be scalable and interpretable, coupled with a business impact of at most $3M. This project gave me a real-world opportunity to refine and enhance the tools that I’m already familiar with (Python and SQL) and introduced me to new ones that I can add to my career toolbox (Snowflake and Power BI). I also took my due diligence to learn about the company’s operations, as well as concepts in supply chain and retail, as I believe that for me to manipulate data to extract valuable insights, I had to be exposed to the very domain that they exist in. In this way I can deliver the solution with a driving impact. I am very much looking forward to taking these valuable skills to similar endeavors in the future. If you have any questions or thoughts about this project, I am happy to connect with you!

**Project Connection:** This blog post expands on my work during my [Tractor Supply Internship]({{ '/internships-tractor/' | relative_url }}).