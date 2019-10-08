---
title: Prediction model performance -  AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: norliu
ms.reviewer: v-dehaas
---

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result, including a Performance score.

## Accuracy score

AI Builder calculates the accuracy score for your model based on prediction result of the test data set. Before training, AI Builder separates your dataset into separate training data and testing data sets. And after training, AI Builder applies your AI model to the testing data set, and then calculates your accuracy score. For example: if your test data set has 200 records, and AI Builder correctly predicts 160 of them, AI Builder shows an accuracy score of 80%.

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## How is accuracy related to performance?

A higher accuracy score generally means better model performance, but keep in mind that an extremely high score could indicate issues with the relevance or bias of your training data. You have to determine the appropriate level of accuracy for your intended use of the AI model.

Here are some broad guidelines for assessing accuracy scores:

|Score |Guidance  |
|---------|---------|
|<50%|Scores consistently below 50% mean that something is wrong with your model - it is wrong more often than a simple guess would be. Perhaps your data fields are not mapped correctly, or you are using the wrong data. |
|>50% |Scores consistently greater than 50% mean that your model performs better than a guess. The higher the score, the more accurate the model is.|
|~100%|Scores consistently close to 100% could indicate bias in the training data, or that a field that is correlating directly to the answer. |

If your scores are consistently between 50% – 100%, you have to assess whether the performance is appropriate for your intended use of the AI model. You'll have a different tolerance for inaccuracy depending on your AI model implementation. Whether your model is intended for marketing, predicting online shopper intention, or detecting fraud, you should decide the level of accuracy that makes the AI model practical to use based on the intended use.

## Improve prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve it's performance. Here are some things you can try to help improve your model's predictive power:

### Review errors and issues

- After you finish training, if there are any errors, fix them and retrain the model.
- If there are no errors, check the training  details. Try to address as many issues as possible, and then retrain the model.

### Review top influencers

After each training, a list of top influencers appears on the model details page. Each field used in the training has a score to represent its influence on the training. These scores combined equal 100%.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers’ intention. And you’re expecting Age, Product as the most influential field, you should see that in the most influential field list in model details page. If not, it may indicate that the training result is not as expected. In this case, you can either deselect the irrelevant or misleading fields and retrain or check your training issues to see details.


### Add more data

The minimum requirement for training data is 50 records, but this doesn't mean 50 data records will train a highly predictive model. Try to provide 1000 or more data records, correctly labeled, with a realistic distribution between options.

### Check your data distribution

For example, if you are using two option label of *Yes* or *No*, and most of your data record only has a *Yes* in this field, it’s hard for your model to learn from this data. Try to have a distribution of options in your data that roughly reflects the distribution of the options you might expect see. For example, if you are looking at data fields for *cat_owner* and *dog_owner*, use a data distribution somewhere around 50%. If you are looking at fraudulent transactions, use a more imbalanced distribution - perhaps 95% - 5%. Look to industry standards for this type of information if you don't know what to expect.

### Add more fields

For example, if you want to predict which customer is more likely to return and buy your products. You can add more fields like how they rate the product, how much they use the product, are they returning users for other product under this brand, and so forth to make the training data richer.

### Narrow selected fields to relevant information

You may already have a lot of correctly labeled training data, with lot of data fields. Then why might the model still not performing well? It could be that you're selecting fields that lead to unwanted bias. Make sure all the fields you select are relevant to influence what you want to predict. Deselect irrelevant or misleading fields.

### Validate data

- Make sure the data fields  don't have high rate of missing values (>99%). Populate the missing values with default or remove the data field from the model training.
- If a data field has high correlation with prediction outcome, remove the data field from the model training.  

## Next step

[Use your published prediction model in a model-driven app](prediction-model-driven-app.md)
