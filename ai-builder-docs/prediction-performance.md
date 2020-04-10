---
title: Prediction model performance -  AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/10/2020
ms.author: norliu
ms.reviewer: v-dehaas
---

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result. These results include a performance grade and/or accuracy score, depending on the type of prediction being done.

## Measuring performance for different types of predictions

Based on your model's prediction type, AI Builder measures performance differently.


|Pediction type |Performance metric |
|---------|---------|
|Binary    |Performance grade         |
|Multiple   |Accuracy score      |
|Numerical   |Performance score        |

## How to understand model performance

AI Builder shows a performance grade to help you evaluate your model's ability to predict results. The decision about whether your model is ready to publish is one you have to make based on your unique needs and circumstances. AI Builder provides the following grades to help you make that judgement call.

## Accuracy grade

AI Builder shows a grade to help you  evaluate your model's accuracy. The decision about whether your model is ready to publish is one you have to make based on your unique needs and circumstances. AI Builder provides the following accuracy grades to help you make that judgment call.

|Grade |Guidance  |
|---------|---------|
|A|It might still be possible to improve the model, but this is the best grade you can get. |
|B|The model is correct a lot of the time. Could it be improved? That depends on your unique circumstances, data, and requirements. |
|C|The model is doing slightly better than a random guess. It might be acceptable for some applications, but in most cases, this is a model that you'd continue to tweak and improve.  |
|D|Something's wrong. Your model is either performing worse than we'd expect a random guess to perform [underfit model](manage-model.md#underfit-model), or it's performing so well (at or near 100%) that you've probably got a data field that is directly correlated  to the result [overfit](manage-model.md#overfit-model) .

More information about [underfit models](manage-model.md#underfit-model)
More information about [overfit models](manage-model.md#overfit-model) 
 |

Depending on the data distribution of your historical data, the actual accuracy rates that correspond to the above grades can vary. The difference accounts for the fact that the improvement relative to your baseline rate changes when you move that baseline.

Let's say your model predicts if a shipment will arrive on-time or not. If your historical on-time rate is 80%, an accuracy score of 92 would correspond to a B grade. But, if your historical on-time rate is only 50%, 92 would correspond to an A grade. That's because 92 is a much better improvement over 50% than it is over 80%, and you'd expect a random guess to be close to those percentages.

This example shows the accuracy ranges for each grade when the historical data contains different on-time rates for a binary prediction.

| Grade | Accuracy range for historical 25% on-time rate | Accuracy range for historical 50% on-time rate | Accuracy range for historical 80% on-time rate | Accuracy range for historical 95% on-time rate |
|-------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|
| A | 92.5 - <99.3% | 90 – 98% | 93 – <99% | 98.1 - <99.8% |
| B | 81.3 - <92.5% | 75 – <90% | 84 – <93% | 95.3 - <98.1% |
| C | 66.3 - <81.3% | 55 – <75% | 71 – <84% | 91.5 - <95.3% |
| D | <66.3% or ≥99.3% | <55% or ≥98% | <71% or ≥99% | <91.5% or ≥99.8% |

## Multiple choice prediction

An accuracy score measures the model's performance. A higher accuracy score generally means better model performance, but keep in mind that an extremely high score could indicate a problem with your training data. You have to determine the appropriate level of accuracy for your intended use of the AI model.

Here is some guidance for accuracy scores:

 
|Score |Guidance  |
|---------|---------|
| ≥50% |Consistent scores greater than 50% mean that your model performs better than a guess. Generally, the higher the score, the more accurate the model.   |
|<50% [underfit model](manage-model.md#underfit-model)  |Consistent scores below 50% mean that something is wrong with your model. It is wrong more often than a simple guess would be. This is known as an [underfit model](manage-model.md#underfit-model). Perhaps your data fields are not mapped correctly, or you are using the wrong data.    |
|~99%-100% [overfit](manage-model.md#overfit-model)    |Consistent scores close to 100% could indicate bias in the training data, or that a field that is correlating directly to the answer. This is known as an [overfit model](manage-model.md#overfit-model)     |
|50%-98%   |If your scores are consistently between 50% – 100% you must assess whether the performance is appropriate for your intended use of the AI model. Different model implementations have different tolerance for inaccuracy.  Predictions for marketing,  fraud detection, or order fulfillment would all have different levels of accuracy that make the AI model practical to use.     |

## Numerical prediction

For numerical prediction, we use a linear performance score. This score measures distance between the prediction and the actual data.

Let's say you're predicting the number of days to fulfill, ship, and deliver an order. The model predicts a set of numbers. The linear performance score shows the distances between predicted values and actual values in your training data. This is expressed as a number between  0 – 100%, with higher values indicating the predicted value is closer to the real value. Typically, a higher score means the model performs better. Remember though, that perfect or near-perfect scores ([overfit models](manage-model.md#overfit-model) ) are usually indicative of a problem with your training data.

Here is some broad guidance for linear performance scores:

|Score |Guidance  |
|---------|---------|
| ≥50% |Consistent scores greater than 50% mean that your model performs better than a guess. Generally, the higher the score, the more accurate the model.   |
|<50%  ([underfit](manage-model.md#underfit-model))  |Consistent scores below 50% mean that something is wrong with your model. It is wrong more often than a simple guess would be. This is known as an [underfit model](manage-model.md#underfit-model). Perhaps your data fields are not mapped correctly, or you are using the wrong data.    |
|~99%-100%  ([overfit](manage-model.md#overfit-model))   |Consistent scores close to 100% could indicate bias in the training data, or that a field that is correlating directly to the answer. This is known as an [overfit model](manage-model.md#overfit-model)     |
|50%-98%   |If your scores are consistently between 50% – 100% you must assess whether the performance is appropriate for your intended use of the AI model. Different model implementations have different tolerance for inaccuracy.  Predictions for marketing,  fraud detection, or order fulfillment would all have different levels of accuracy that make the AI model practical to use.     |

## Performance details

For training details, select **See details** on the model's grade box.  

>[!NOTE]
 >For information about additional features planned for this area, see [release plans](https://docs.microsoft.com/power-platform-release-plan/2020wave1/ai-builder/).

### Binary prediction

The following performance information is available
- Performance grade
- Accuracy score

#### Performance grade
  
In addition to your model's grade, information about each grade and the corresponding accuracy range appears on the model details page. This tells you how much room you  might have to improve your model.

#### Accuracy score

AI Builder calculates the accuracy score for your model based on prediction result of the test data set. Before training, AI Builder separates your dataset into separate training data and testing data sets. And after training, AI Builder applies your AI model to the testing data set, and then calculates your accuracy score. For example: if your test data set has 200 records, and AI Builder correctly predicts 192 of them, AI Builder shows an accuracy score of 96%.
For more information, see [Evaluate your model](manage-model.md#evaluate-your-model).

#### When predicting multiple outcomes
The following performance information is available

- Training date
- Data source
- Historical outcome
- Entity list used to do prediction.

#### When predicting a number

The following performance information is available

- Training date
- Data source
- Historical outcome
- Entity list used to do prediction.


<!-- Coming May 2020 tentatively
- Accuracy per outcome
- Confusion matrix
- Cumulative gains chart -->

### Accuracy score

AI Builder calculates the accuracy score for your model based on prediction result of the test data set. Before training, AI Builder separates your dataset into separate training data and testing data sets. And after training, AI Builder applies your AI model to the testing data set, and then calculates your accuracy score. For example: if your test data set has 200 records, and AI Builder correctly predicts 192 of them, AI Builder shows an accuracy score of 96%.

For more information, see [Evaluate your model](manage-model.md#evaluate-your-model).

<!--
### Accuracy per outcome
This section shows the distribution of correct and incorrect results. You can use this to help you evaluate the model.
AI Builder shows a bar chart to quantify the accuracy of your AI model. Let's still use the business loan application as an example. The "Approved" bar would show how many predictions match the actual result, compared to all the records processed. If the rate of the correctly predicted records is high,  this information might help you decide to go ahead and use this model. 

### Confusion matrix
The confusion matrix describes the performance of the model as follows:

- true positives
- false positives
- true negatives
- false negatives

True positives and true negatives are correctly predicted outcomes. False positives & false negatives are records that were incorrectly predicted.

### Cumulative gains chart

> [!Note]
> This feature uses Highcharts (https://www.highcharts.com Copyright (c) Highsoft Solutions AS. All Rights Reserved)
-->

## Improve prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve it's performance. Here are some things you can try to help improve your model's predictive power:

### Review errors and issues

- After you finish training, if there are any errors, fix them and retrain the model.
- If there are no errors, check the training  details. Try to address as many issues as possible, and then retrain the model.

### Review top influencers

After each training, a list of top influencers appears on the model details page. Each field used in the training has a score to represent its influence on the training. These scores combined equal 100%.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers' intention. And you're expecting Age, Product as the most influential field, you should see that in the most influential field list in model details page. If not, it may indicate that the training result is not as expected. In this case, you can either deselect the irrelevant or misleading fields and retrain or check your training issues to see details.


### Add more data

The minimum requirement for training data is 50 records, but this doesn't mean 50 data records will train a highly predictive model. Try to provide 1000 or more data records, correctly labeled, with a realistic distribution between options.

### Check your data distribution

For example, if you are using two option label of *Yes* or *No*, and most of your data record only has a *Yes* in this field, it's hard for your model to learn from this data. Try to have a distribution of options in your data that roughly reflects the distribution of the options you might expect see. For example, if you are looking at data fields for *cat_owner* and *dog_owner*, use a data distribution somewhere around 50%. If you are looking at fraudulent transactions, use a more imbalanced distribution - perhaps 95% - 5%. Look to industry standards for this type of information if you don't know what to expect.

### Add more fields

For example, if you want to predict which customers are more likely to return and buy your products. You can add more fields to make the training data richer.  For example:

- How do they rate the product?
- How much do they use the product?
- Are they an existing customer?

### Narrow selected fields to relevant information

You may already have a lot of correctly labeled training data, with many data fields. Then why might the model still not performing well? It could be that you're selecting fields that lead to unwanted bias. Make sure all the fields you select are relevant to influence what you want to predict. Deselect irrelevant or misleading fields.

### Validate data

- Make sure the data fields  don't have high rate of missing values (>99%). Populate the missing values with default or remove the data field from the model training.
- If a data field has high correlation with prediction outcome, remove the data field from the model training.  

## Next step

[Use your published prediction model in a model-driven app](prediction-model-driven-app.md)
