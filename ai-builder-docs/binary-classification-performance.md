---
redirect_url: prediction-performance
title: Prediction model performance -  AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: norliu
ms.reviewer: kvivek
---

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result, including a **Accuracy** score.  

## Accuracy score calculations

AI Builder calculates the accuracy score for your model based on prediciton result of the test data set. Before training, your dataset is separated to a training data set and a testing data set. And after training, AI Builder will apply model to the testing data set. For example, the test data set has 200 records, and AI Builder predicts 160 correctly, then your will see an accuracy score of 80%.

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## <a name="ImproveAccuracy"> How to improve your model's Accuracy</a>

If your business issue requires the accuracy to be very high, here are some tips on hwo to tweak your model to improve its predictive power.

### Add more data

Even though the minimum requirement for training data is 50, it doesn't mean 50 data records can train a highly predictive model. For example, if your two option label is Yes or No, and most of your data record only has an Yes in this field. It’s hard for your model to learn all the signals from your data. And if your data is not correctly labeled, it will give the model wrong signal. It would be ideal if you could provide 1000 data records or more. So your model could be more predictive.

### Add more fields

Add more fields that you think could influence what you want to predict. For example, if you want to predict which customer is more likely to return and buy your products. You can add more fields like how they rate the product, how heavy they use the product, are they returning users for other product under this brand, etc to make the training data richer so it could be more predictive.

### Deselect irrelevant or misleading fields

You may already have a lot of correctly labeled training data, and added a lot of data fields, but why the model is still not that predictive as you expect? It could be that you're selecting too many fields that leads to unwanted bias. Make sure all the fields you selected are going to influence what you want to predict. Unselect those irrelevant or misleading fields.

### Fill in missing values

Also validate the data fields that you selected to train the model don't have high rate of missing values (>99%), populate the missing values with default or remove the data field from the model training. If a data field have high correlation (>99%) with prediction outcome, remove the data field from the model training. 

## How is Accuracy related to my model

Generally speaking, higher accuracy score means better performance of your model. But it's not always true. You need to determine if the model is accurate enough to solve your business issue.

If your accuracy score is less than 50%, it generally means that your model is not accurate enough. And you need to follow the instructions listed in [How to improve your model's Accuracy](#ImproveAccuracy) to improve your model.

If your accuracy score is too high, e.g. 99% or even 100%, that doesn't mean your model is perfect. In fact, it could mean that you may have selected some columns that could reveal the answer of the issue you're trying to predict. In this case, check your top influencers and if there is one field with extreamly high influence (influence score equals to 100 or close to 100), it means this field reveals the answers. Please deselect this field during retrain at the select field stage and then hit train button again to check the new accuracy.

If your accuracy score is above 50, but less that the too high score. It means you may decide to publish your model based on your business need. E.g if you're predicting which customers are likely to return to buy your product again in order to make a campaign to them, you may not require very high accuracy as long as the model is better than 50. But if you're trying to predict stock increase or descrease in order to make investment, then you may require a much higher accuracy because you don't want to risk your investment.

## Top influencers

After each training, there will be a list of top influencers shown on the model details page. Each field used in the training has a score to represent its influence on the training. The higher the score is, the more influential the field is. These scores combined equal 100%.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers’ intention. And you’re expecting “Age”, “Product” as the most influential field, you should see that in the most influential field list in model details page. If not, it may indicate that the training result is not as expected. In this case, you can either deselect the irrelavant or misleading fields and retrain or check your training issues to see details.

### Next step

[Use your published binary classification model in a model-driven app](binary-classification-model-driven-app.md)
