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

AI Builder calculates the 

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## How is Accuracy related to performance?

A higher accuracy score generally means better model performance, but keep in mind that an extremely high score could indicate issues with the relevance or bias of your training data. You have to you to determine the appropriate level of accuracy  for your intended use of the AI model.

Here are some broad guidelines for assessing accuracy scores:

|Score |Guidance  |
|---------|---------|
|>50% |Consistent scores greater than 50% mean that your model performs better than a guess. The higher the score, the more accurate the model is.|
|<50%|Consistent scores below 50% mean that something is wrong with your model so that it is wrong more often than a simple guess would be. Perhaps your data fields are not mapped correctly, or you are using the wrong data. |
|~100%|Consistent scores close to 100% could indicate bias in the training data, or that a field that is correlating directly to the answer. |
|50% - 100% |If your scores are consistently between 50% – 100% you must assess whether the performance is appropriate for your intended use of the AI model. Different model implementations have different tolerance for inaccuracy.  Predictions for marketing, payments, or fraud detection, will all have different levels of accuracy that make the AI model practical to use. |

## Improve prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve it's performance. Here are some things you can try to help improve your model's predictive power:

### Review errors and issues

• After you finish training, if there are any errors, fix them and retrain the model.
• If there are no errors, check the training  details. Try to address as many issues as possible, and then retrain the model.

### Review top influencers

After each training, a list of top influencers appears on the model details page. Each field used in the training has a score to represent its influence on the training. These scores combined equal 100%.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers’ intention. And you’re expecting Age, Product as the most influential field, you should see that in the most influential field list in model details page. If not, it may indicate that the training result is not as expected. In this case, you can either deselect the irrelevant or misleading fields and retrain or check your training issues to see details.


### Add more correctly labeled training data

Even though the minimum requirement for training data is 50, it doesn't mean 50 data records can train a highly predictive model. For example, if your two option label is *Yes* or *No*, and most of your data record only has an *Yes* in this field. It’s hard for your model to learn all the signals from your data. And if your data is not correctly labeled, it will impact the accuracy in a negative way. Try to provide 1000 data records or more for better results. 

### Add more fields

For example, if you want to predict which customer is more likely to return and buy your products. You can add more fields like how they rate the product, how much they use the product, are they returning users for other product under this brand, and so forth to make the training data richer.

### Narrow selected fields to relevant information

You may already have a lot of correctly labeled training data, with lot of data fields. Then why might the model still not performing well? It could be that you're selecting fields that lead to unwanted bias. Make sure all the fields you select are relevant to influence what you want to predict. Deselect irrelevant or misleading fields.

### Validate data

- Make sure the data fields  don't have high rate of missing values (>99%). Populate the missing values with default or remove the data field from the model training.
- If a data field has high correlation with prediction outcome, remove the data field from the model training.  

If your accuracy score is extremely high, e.g. consistently close to 100%, check your top influencers to make sure these fields are not revealing the answer of the issue you’re trying to predict. If this is the case, deselect the field and retrain the model.

For example, let's say you want to predict which customers are likely to return and buy your products. You set your target field as *ReturningCustomer*, but there is also a field *NewCustomer* in your training data indicating whether this is a new customer. Your model would be 100% accurate because it has data that reveals whether the customer is a returning one. 
•	  In this case, deselect the *NewCustomer* field, and then retrain the model.


##


## Next step

[Use your published binary classification model in a model-driven app](binary-classification-model-driven-app.md)
