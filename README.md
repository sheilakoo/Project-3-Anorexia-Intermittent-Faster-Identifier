# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3 - Web APIs & NLP

## Introduction

Welcome to the Anorexia Nervosa Predictor Web App project! In today's digital age, where information is abundant and easily accessible, there is a growing need to leverage technology to address pressing issues related to mental health and wellness.

Our project is designed to address the critical concern of identifying posts on Reddit related to anorexia nervosa and healthy fasting practices. Anorexia Nervosa, a severe mental health disorder, and Intermittent Fasting, a popular health trend, represent two contrasting aspects of dietary behaviors and overall wellbeing.

In this README, we will explore the problem statement, background information on IF and AN, the datasets we've collected, and the key questions we aim to address with our project. Through our text classification tool, we aspire to provide a means for individuals and healthcare professionals to distinguish between posts indicative of "Healthy Fasting" and those signaling "Anorexia Nervosa."

Let's embark on this journey of using technology to make a meaningful impact on healthcare and mental wellbeing industries.

## Problem Statement

**Who We Are:**
A healthcare group with an online presence.

**Goal:**
Our goal is to successfully classify text-based posts into one of two classes: "Intermittent Fasting" or "Anorexia Nervosa."

**Target Customer:**
Our target customers include in-house services and our business partners.

**Objective:**
We aim to develop a text classification tool that serves as a predictor and self-diagnostic tool. This tool will help identify users' affiliation with either Intermittent Fasting or Anorexia Nervosa based on inputs gathered from two subreddit communities representing these groups.

## Key Questions

In the context of machine learning and text classification, we aim to address the following key questions:

1. How can we effectively classify text-based posts related to fasting behaviors into the categories of "Healthy Fasting" or "Anorexia Nervosa" using machine learning techniques?
2. What challenges do we encounter in accurately predicting and classifying posts that may indicate anorexia nervosa, given the sensitivity and complexity of the topic?

## Background

The Anorexia Nervosa Predictor Web App project explores the intersection of technology and mental health, focusing on two distinct aspects of dietary behaviors and overall wellbeing.

**Intermittent Fasting (IF):**
Intermittent Fasting is a popular health trend characterized by controlled fasting and eating patterns. It is often adopted for weight management and overall wellness. Individuals practicing IF alternate between periods of fasting and eating, with various methods and schedules available.

**Anorexia Nervosa (AN):**
Anorexia Nervosa is a severe mental health disorder marked by extreme dietary restriction, an intense fear of gaining weight, and a distorted body image. It is a life-threatening condition that requires specialized treatment and support.

In this project, we aim to harness the power of machine learning and Natural Language Processing (NLP) to differentiate between posts related to healthy fasting and those indicative of Anorexia Nervosa. By developing a text classification tool, we hope to provide valuable insights and support for individuals and healthcare professionals in the field of mental health and wellness.

Let's delve deeper into the problem statement, datasets, and key questions to understand the significance of this project.

## Datasets

### Data Collection
We obtained data for this project through the use of web scraping and Natural Language Processing (NLP) techniques. We collected Reddit posts related to anorexia nervosa from two subreddits:

1. [r/AnorexiaNervosa](https://www.reddit.com/r/AnorexiaNervosa/)
2. [r/intermittentfasting](https://www.reddit.com/r/intermittentfasting/)

We used the PRAW library and a custom Reddit scraper to collect the data.

### Data Dictionary

Here's a data dictionary for the key columns used in this project:

| Column                             | Datatype  | Explanation                                           |
| ---------------------------------- | --------- | ----------------------------------------------------- |
| **title**                          | object    | Title of the Reddit post                              |
| **post_text**                      | object    | Text content of the Reddit post                       |
| **id**                             | object    | Unique identifier for the post                        |
| **score**                          | int64     | Score or upvotes of the post                          |
| **total_comments**                 | int64     | Total number of comments on the post                  |
| **post_url**                       | object    | URL of the post                                        |
| **subreddit**                      | object    | Subreddit where the post was made                      |
| **post_type**                      | object    | Type or format of the post                             |
| **time_uploaded**                  | object    | Timestamp when the post was uploaded                   |
| **punctuation_removed_title_and_text**  | object    | Title and text content with punctuations removed        |
| **title_text_stemmed**             | object    | Title and text content after stemming                  |
| **title_text_lemmatized**          | object    | Title and text content after lemmatization             |

### PRAW and Workflow Process

1. **Data Collection**: Utilize web scraping techniques to extract data from specific sources, such as websites or online communities. In this project, we collected data from Reddit using the PRAW library and a custom Reddit scraper.

2. **Data Cleaning**: After data collection, the raw data needs to be cleaned:
   - Remove duplicate entries.
   - Handle missing values, if any.
   - Format timestamps for consistency.
   - Eliminate irrelevant or noisy data that doesn't contribute to our project's objectives.

3. **Data Preprocessing**: Prepare the cleaned data for analysis or machine learning:
   - Tokenization: Split text data into words or tokens.
   - Vectorization: Convert text into numerical representations suitable for machine learning.
   - Apply Natural Language Processing (NLP) techniques for text data, such as stemming or lemmatization.

4. **Analysis or Machine Learning**: Use the cleaned and preprocessed data for our analysis or machine learning tasks. In this project, we are classifying text-based posts into categories like "Intermittent Fasting" and "Anorexia Nervosa."

5. **Evaluation and Iteration**: Evaluate the performance of our analysis or machine learning models and make iterations or improvements as needed.

6. **Visualization and Reporting**: Create visualizations and reports to effectively communicate our findings and results.

This workflow outlines the essential steps in collecting, cleaning, and preparing data for our project.

## Conclusion

Our text classification model, specifically the Multinomial Naive Bayes TF-IDF model, achieved an impressive accuracy of 0.985. This high accuracy indicates the model's effectiveness in classifying posts into the "Healthy Fasting" and "Anorexia Nervosa" categories.

## Recommendations

### Key Insights
The success of our model lies in its ability to identify the keywords in Reddit threads, allowing us to accurately classify users into either the "Healthy Fasting" or "Anorexia Nervosa" groups.

### Business Recommendations and Applications
Based on the classification results, we propose the following recommendations and applications:

#### Users in "Blue Mode" (Healthy Fasting):

**Product Recommendations:**
- Gym equipment
- Whey products
- Grooming classes

#### Users in "Amber Mode" (Anorexia Nervosa):

**Service Recommendations:**
- Amber: Mental health advice clinic
- Fasting guidelines
- Red: SOS hotline

These recommendations aim to provide appropriate support and resources to users based on their classification, ensuring they receive the necessary assistance and guidance.

## Future Work

As we continue to evolve the Anorexia Nervosa Predictor Web App, we envision several directions for future work and enhancements:

1. **Scalability**: Consider implementing a scalable infrastructure to handle increased user traffic and data as our user base expands. This may involve cloud solutions and optimizations for efficient processing.

2. **Enhanced User Engagement**: Explore ways to enhance user engagement and interaction within the web app. Features such as user forums, community support, and personalized recommendations could be valuable additions.

3. **Integration with Mental Health Resources**: Develop partnerships or integrations with mental health organizations to provide users with easy access to professional resources and support, especially for those classified under "Amber Mode."

4. **Real-time Monitoring**: Investigate real-time monitoring of user interactions and posts to promptly identify potential crisis situations, particularly for users exhibiting signs of suicidal tendencies.

5. **Cross-Platform Expansion**: Consider expanding the web app's presence to other online platforms and communities beyond Reddit. This expansion can broaden the reach of our tools and make a more significant impact.

These future work items demonstrate our commitment to continuous improvement and our dedication to addressing critical issues in mental health and wellness through technology.

We welcome collaboration and contributions from the community to help us achieve these goals and further enhance the Anorexia Nervosa Predictor Web App.

