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

Each time you train a model, AI Builder uses the test data set to evaluate it's quality and accuracy. A summary page for your model shows your model training result, including an **Accuracy** score.  

## Accuracy score

The accuracy score is the ratio of the correct predictions among all the records you’re trying to predict.
Based on your business needs, you can either keep improving the model by following instructions here, or you can decide to publish it.

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## Improve prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve it's performance. Here are some things you can try to help improve your model's predictive power:

### Add more correctly labeled training data

Even though the minimum requirement for training data is 50, it doesn't mean 50 data records can train a highly predictive model. For example, if your two option label is Yes or No, and most of your data record only has an Yes in this field. It’s hard for your model to learn all the signals from your data. And if your data is not correctly labeled, it will give the model wrong signal. It would be ideal if you could provide 1000 data records or more. So your model could be more predictive.

### Add more fields

For example, if you want to predict which customer is more likely to return and buy your products. You can add more fields like how they rate the product, how much they use the product, are they returning users for other product under this brand, etc to make the training data richer so it could be more predictive.

### Narrow selected fields to relevant information

You may already have a lot of correctly labeled training data, and added a lot of data fields, but why the model is still not that predictive as you expect? It could be that you're selecting too many fields that leads to unwanted bias. Make sure all the fields you selected are going to influence what you want to predict. Unselect those irrelevant or misleading fields.

### Validate data

Also validate the data fields that you selected to train the model don't have high rate of missing values (>99%), populate the missing values with default or remove the data field from the model training. If a data field have high correlation (>99%) with prediction outcome, remove the data field from the model training.  

## Next step

[Use your published binary classification model in a model-driven app](binary-classification-model-driven-app.md)
