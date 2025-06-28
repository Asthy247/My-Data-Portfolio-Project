
# My-Data-Portfolio-Project
Welcome to my comprehensive data science and analytics portfolio! This repository serves as a centralized collection of my projects, demonstrating my skills in data analysis, machine learning, visualization, and more.
## Projects Included:
### Machine Learning
* **Automated Sentiment Analysis using R:** [View Original Repository](https://github.com/Asthy247/Automated-Sentiment-Analysis-using-R)
    * **Description:** This project analyzes customer reviews of Temu products to understand overall sentiment in RStudio...
    
    * **Key Learnings:** Sentiment analysis, R programming, text mining, data visualization.


### 2. [Your Next Project Title Here]
* **Description:** [Brief description of your next project]
* **Location:** [Link to its folder, e.g., `[next-project-folder-name/`](next-project-folder-name/README.md)`]
* **Key Learnings:** [List 2-3 key skills demonstrated]

---

## About Me:

[Add a short bio about yourself and your skills]

---

## Contact:

[Your contact information, e.g., LinkedIn, personal website]
# Automated-Sentiment-Analysis-using-R


# Project Goal

To develop a sentiment analysis model to classify customer reviews as positive, negative, or neutral, using a dataset of Temu customer reviews.


# Data Collection and Preprocessing

# Data Source

**Web Scraping:** Utilized libraries like BeautifulSoup or Scrapy to extract reviews from Temu's website.

**API Access**: Used Temu's API to directly access review data.


# Introduction

Sentiment analysis, a subfield of natural language processing (NLP), involves the automated identification and 

categorization of sentiments expressed in text. By analyzing text data, sentiment analysis can determine whether 

the sentiment is positive, negative, or neutral. This technique has widespread applications across various industries, including:


**Social Media Monitoring**: Tracking public opinion about brands, products, or services.

**Customer Service:** Identifying customer complaints and feedback to improve customer satisfaction.

**Market Research:** Analyzing customer reviews and product feedback to inform business decisions.

**Financial Analysis:** Gauging market sentiment and predicting stock prices.


# How Sentiment Analysis Works

**Text Preprocessing:**

**Cleaning**: Removing noise, such as HTML tags, punctuation, and stop words.

**Tokenization**: Breaking down text into individual words or tokens.

**Stemming/Lemmatization**: Reducing words to their root form.


# Feature Extraction:

**Bag-of-Words**: Representing text as a bag of words, ignoring word order.

**TF-IDF:** Assigning weights to words based on their frequency and importance.

**Word Embeddings**: Representing words as dense vectors, capturing semantic and syntactic relationships.


**Model Training:**

# Machine Learning Models

Naive Bayes

Support Vector Machines (SVM)

Random Forest

**Deep Learning Models:**

Recurrent Neural Networks (RNNs)

Long Short-Term Memory (LSTM) networks

Transformer-based models (e.g., BERT, RoBERTa)


**Sentiment Classification:**

The trained model classifies new text into positive, negative, or neutral categories.


# Word Cloud for Overall Sentiment

![image](https://github.com/user-attachments/assets/ca2d2b9b-a9f7-4e04-ac66-cb0781b31b61)


The word cloud provides a visual representation of the most frequent words in the dataset. The larger the word, the more frequently it appears in the reviews.


**Positive Sentiment:**

The word cloud highlights several positive sentiments, such as "great," "amazing," "happy," "love," "fantastic," and "perfect."


Terms like "recommend," "highly," and "expected" suggest customer satisfaction.


Words like "quality," "product," and "service" indicate that customers are focusing on these aspects of their experience.



**Negative Sentiment:**

Words like "disappointed," "issues," "poor," and "wasn't" suggest negative experiences.


Terms like "took" and "delivery" might indicate issues with shipping or delivery times.


**Neutral Sentiment:**

Words like "okay," "good," and "expected" represent neutral sentiments.

Overall, the word cloud suggests a mix of positive and negative sentiments. 

Customers are generally satisfied with the product quality, shipping, and customer service. However, there are also 

instances of negative experiences related to product quality, shipping delays, and customer service issues.


# Model Building and Training

# Model Selection for Random Forest

![image](https://github.com/user-attachments/assets/5de31786-bd63-45e0-a97a-7babe16d7e13)


**Interpreting the Random Forest Model Output**

**Model Summary**

**Type of random forest:** Classification. This indicates the model is designed to predict categorical outcomes.

**Number of trees**: 500. A larger number of trees generally improves the model's accuracy and stability.

**No. of variables tried at each split: 15.** This parameter controls the complexity of each tree. A higher number can lead to overfitting, while a lower number may underfit.

**Out-of-Bag (OOB) Error Rate:**

**52.83%**: This is the estimated error rate of the model. It's calculated by predicting the class of each training observation using the trees that didn't include that observation in their 

training set. A lower OOB error rate indicates a better-performing model.

**•	Diagonal Elements**: These represent correct predictions. For example, 3 negative instances were correctly classified as negative.

**•	Off-Diagonal Elements:** These represent incorrect predictions. For example, 17 negative instances were incorrectly classified as positive.

**•	Class Error Rate:** This is the proportion of incorrect predictions for each class.


**Interpretation:**

•	The model is struggling with classification accuracy, especially for negative and neutral classes.

•	The high OOB error rate further supports this.


# Random Forest (Resampling)

![image](https://github.com/user-attachments/assets/a3cab8ea-fdb8-46cf-858a-990183feefd1)



**Model Summary**

•	**Sample Size**: The model was trained on 53 samples.

•	**Predictors**: 226 features were used to make predictions.

•	**Classes**: The model is designed to predict three classes: 'negative', 'neutral', and 'positive'.

**Resampling Method:**

•	Cross-Validated (10-fold): The data was divided into 10 folds. The model was trained on 9 folds and tested on the remaining fold. 

This process was repeated 10 times, with each fold serving as the test set once.   

**Performance Metrics:**

**•	Accuracy**: 0.4833333 

o	This indicates that the model correctly predicted the class of 48.33% of the observations.

•	**Kappa:** 0.08517544 

o	Kappa is a statistical measure of inter-rater agreement. In this case, it measures the agreement between the predicted 

classes and the actual classes. A value of 0 indicates no agreement, while 1 indicates perfect agreement.

A low Kappa value suggests that the model's predictions are not much better than random chance.

**Tuning Parameter:**

•	**mtry**: This parameter controls the number of variables randomly selected at each split in the decision trees. 

It was held constant at 15 during the model training.

**Interpretation:**

The model's performance, as measured by accuracy and Kappa, is relatively low. This suggests that the model 

is not very accurate in predicting the sentiment of the reviews.

# Confusion Matrix

![image](https://github.com/user-attachments/assets/bfecd559-6de4-4c82-bf61-d73783e800ae)


The confusion matrix provides a breakdown of correct and incorrect predictions for each class.


•	**True Positives (TP**): 2 (correctly predicted as negative)

•	T**rue Negatives (TN):** 2 (correctly predicted as positive)

•	**False Positives (FP)**: 2 (incorrectly predicted as positive)

•	**False Negatives (FN**): 0 (incorrectly predicted as negative or neutral)



**Overall Statistics**

•	**Accuracy:** 0.6667 

o	This indicates that the model correctly predicted 66.67% of the instances.



•	**95% CI:** (0.3489, 0.9008) 

o	This is the 95% confidence interval for the accuracy. It suggests that the true accuracy of the model lies within this range with 95% confidence.


•	**No Information Rate**: 0.5 

o	This is the accuracy that would be achieved by always predicting the majority class.


•	**P-Value [Acc > NIR]**: 0.1938 

o	This p-value tests the null hypothesis that the model's accuracy is no better than the no-information rate. 

A p-value greater than 0.05 suggests that the model's performance is not significantly better than random chance.


•	**Kappa**: 0.3684 

o	Kappa is a statistical measure of inter-rater agreement. A higher Kappa value indicates better agreement between the predicted and actual classes. 

In this case, the Kappa value suggests moderate agreement.

**•	McNemar's Test P-Value:** NA 

o	McNemar's test is used to compare the marginal frequencies of a 2x2 contingency table. 

Since our confusion matrix is not a 2x2 table, this test is not applicable.



**Statistics by Class**

**•	Sensitivity (Recall)**:

o	**Negative**: 0.50 (50% of actual negative cases were correctly identified)

o	**Neutral**: 0.00 (None of the actual neutral cases were correctly identified)

o	**Positive**: 1.00 (All actual positive cases were correctly identified)



•	**Specificity**: 

o	**Negative**: 1.00 (All instances that were not actually negative were correctly classified as not negative)

o	**Neutral**: 1.00 (All instances that were not actually neutral were correctly classified as not neutral)

o	**Positive**: 0.3333 (33.33% of instances that were not actually positive were correctly classified as not positive)



•	**Positive Predictive Value (Precision)**:

o	**Negative**: 1.00 (All instances predicted as negative were actually negative)

o	**Neutral**: NaN (No instances were predicted as neutral)

o	**Positive**: 0.60 (60% of instances predicted as positive were actually positive)


•	**Negative Predictive Value:**

o	**Negative**: 0.80 (80% of instances predicted as not negative were actually not negative)

o	**Neutral**: 0.8333 (83.33% of instances predicted as not neutral were actually not neutral)

o	**Positive**: 1.00 (All instances predicted as not positive were actually not positive)


**Overall Interpretation:**

The model shows moderate accuracy, particularly in predicting positive cases. However, 

it struggles with identifying neutral and negative cases. The class-wise statistics provide a detailed breakdown 

of the model's performance for each class.

# Optimized Model Accuracy

0.6666667

Interpreting Optimized Model Accuracy: 0.6666667

An accuracy of 0.6666667 means that the model correctly predicted the class of 66.67% of the samples in the dataset. 

In other words, for every 100 data points, the model was able to correctly classify 67 of them.

**To put this into perspective:**

•	**Good Accuracy**: A model with an accuracy of 0.8 or higher is generally considered good, especially in domains with complex decision boundaries.

•	**Moderate Accuracy**: An accuracy between 0.6 and 0.8 is considered moderate, indicating that the model is better than random guessing but still has room for improvement.

•**Poor Accuracy**: An accuracy below 0.6 suggests that the model's predictions are not reliable and may be worse than random guessing.

# Word Cloud for Overall Sentiment

![image](https://github.com/user-attachments/assets/7d37a5e3-490f-4d15-a5d0-0511c079e1ce)


The word cloud suggests a predominantly positive sentiment towards Temu. The larger the word, the more frequently it appears in the reviews, indicating its significance.

**Key Themes:**

**Product Quality and Satisfaction:**

Words like "quality," "product," and "great" highlight customer satisfaction with the products.

Terms like "exactly" and "arrived" suggest accurate product descriptions and timely delivery.


**Customer Service**:

The word "customer" is prominent, indicating a focus on customer experience.

"Service" suggests that customers are satisfied with the customer support and assistance provided.

**Positive Shopping Experience**:

Words like "recommend," "buy," and "shopping" imply that customers are likely to shop on Temu again.

"Fast" and "delivery" might indicate quick shipping times.


In summary, the word cloud suggests that customers are generally satisfied with Temu's product quality, customer service,

and shipping times. The platform seems to be delivering on its promises and providing a positive shopping experience.


# Word Cloud for Overall Sentiment


![image](https://github.com/user-attachments/assets/23723560-b76c-4f0f-af54-e6f701344928)


**Interpreting the Word Cloud**

This word cloud provides a visual representation of the most frequent words in a dataset of customer reviews, likely related to Temu.

**Key Insights**:

**Negative Sentiment:**

The prominence of words like "disappointed" and "wasn't" suggests that a significant portion of the reviews expresses negative sentiment.

Terms like "product" and "item" indicate that these are often the focus of the negative feedback.


**Customer Experience:**

Words like "service," "customer," and "experience" highlight that customers are concerned about their overall experience with Temu.


"Ordered" and "arrived" suggest issues related to order fulfillment and delivery.

Overall, the word cloud indicates that while customers might be using Temu, there are some areas of concern, particularly 

regarding product quality and customer experience.

# Word Cloud for Overall Sentiment

![image](https://github.com/user-attachments/assets/aa28e543-413e-495f-aaca-3bd0d3913c0b)


**Interpreting the Word Cloud**

**Key Takeaways**:

This word cloud suggests a neutral to slightly positive sentiment towards Temu. Here's a breakdown:

**Product Focus**:

"Product" is the largest word, indicating a strong focus on the products themselves.

"Service" is also prominent, suggesting that customers are evaluating the overall service provided by Temu.


**Neutral Sentiment**:

The word "okay" suggests a neutral sentiment. It implies that customers are neither overly satisfied nor dissatisfied.


**Shipping and Delivery**:

"Shipping" is a prominent word, indicating that customers are paying attention to delivery times and shipping processes.


Overall, the word cloud suggests that while customers are generally satisfied with Temu's products and services, 

there's room for improvement in certain areas, such as shipping speed and customer support.


# Recommendations

**Maintain Product Quality**:

Continue to prioritize product quality and ensure that products meet customer expectations.

Implement strict quality control measures to minimize defective products.


**Improve Shipping and Delivery**:

Optimize shipping processes to reduce delivery times and improve reliability.

Provide accurate shipping information and timely updates to customers.


**Enhance Customer Service**:

Invest in customer support resources to provide timely and effective assistance to customers.

Train customer service agents to handle customer inquiries and complaints professionally.


**Leverage Sentiment Analysis:**

Continuously monitor customer reviews and feedback using sentiment analysis tools.

Identify trends and patterns in customer sentiment to proactively address issues.

Use sentiment analysis to measure the impact of marketing campaigns and product launches.

**Data-Driven Decision Making:**

Utilize data analytics to gain insights into customer behavior and preferences.

Use these insights to inform product development, marketing strategies, and customer service initiatives.

By implementing these recommendations, Temu can enhance customer satisfaction, improve brand reputation, and drive business growth.


# Conclusion

Based on the analysis of the word clouds and the random forest model, we can draw the following conclusions:


**Key Insights from the Word Clouds:**

**Product Quality and Customer Service:** These are consistently mentioned across the word clouds, 

indicating that they are significant factors in customer satisfaction.


**Shipping and Delivery**: Shipping speed and reliability seem to be important considerations for customers.


**Mixed Sentiments**: The word clouds reveal a mix of positive and negative sentiments, suggesting that 

while Temu has satisfied many customers, there are also areas for improvement.
>>>>>>> sentiment_analysis_history
