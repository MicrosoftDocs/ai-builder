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

## Performance score calculations

AI Builder calculates the performance score for your model based on the precision and recall of the prediction results:

- **Performance score**: This is the harmonic mean of the precision and recall scores. It balances both scores for an imbalanced class distribution. Performance score values are between 0–100 percent. Generally, the higher the performance score, the better your model performs.
- **Precision**: The fraction of correct predictions among all the positive predictions.
- **Recall**: The fraction of correct predictions among all true positive cases.

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## Improve prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve it's performance. Here are some things you can try to help improve your model's predictive power:

### Add more correctly labeled training data

Even though the minimum requirement for training data is 50, it doesn't mean 50 data records can train a highly predictive model. For example, if your two option label is *Yes* or *No*, and most of your data record only has an *Yes* in this field. It’s hard for your model to learn all the signals from your data. And if your data is not correctly labeled, it will impact the accuracy in a negative way. Try to provide 1000 data records or more for better results. 

### Add more fields

For example, if you want to predict which customer is more likely to return and buy your products. You can add more fields like how they rate the product, how much they use the product, are they returning users for other product under this brand, and so forth to make the training data richer.

### Narrow selected fields to relevant information

You may already have a lot of correctly labeled training data, with lot of data fields. Then why might the model still not performing well? It could be that you're selecting fields that lead to unwanted bias. Make sure all the fields you select are relevant to influence what you want to predict. Deselect irrelevant or misleading fields.

### Validate data

Make sure the data fields  don't have high rate of missing values (>99%). Populate the missing values with default or remove the data field from the model training. If a data field has high correlation (>99%) with prediction outcome, remove the data field from the model training.  

## Next step

[Use your published binary classification model in a model-driven app](binary-classification-model-driven-app.md)
