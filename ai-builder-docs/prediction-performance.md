---
title: Prediction model performance - AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/10/2020
ms.author: norliu
ms.reviewer: v-dehaas
---

# Prediction model performance

After each training, AI Builder uses the test dataset to evaluate the quality and accuracy of the new model. A summary page for your model shows the results of your model training. These results include a performance grade and/or performance score, depending on the type of prediction being done.

## Measuring performance for different types of predictions

Based on whether you're predicting outcomes or numbers, AI Builder evaluates performance in two ways.

|Prediction type |Performance metric |
|---------|---------|
|Classification (outcomes)   |Performance grade         |
|Numerical   |Performance score        |

### Performance grade

If your model is predicting outcomes, such as binary (true/false) or multiple (early, late, on-time) options, AI Builder shows a grade to help you evaluate the accuracy of your model. The decision about whether your model is ready to publish is one you have to make based on your unique needs and circumstances. AI Builder provides the following performance grades to help you make that judgment call.

|Grade |Guidance   |
|---------|---------|
|A|It might still be possible to improve the model, but this is the best grade you can get. |
|B|The model is correct in a lot of the cases. Can it be improved? That depends on your unique circumstances, data, and requirements. |
|C|The model is doing slightly better than a random guess. It might be acceptable for some applications, but in most cases, this is a model that you'd continue to tweak and improve.  |
|D|Something's wrong. Your model is either performing worse than we'd expect a random guess to perform (an [underfit model](manage-model.md#underfit-models)), or it's performing so well&mdash;at or near 100%&mdash;that you've probably got a data field that's directly correlated to the result (an [overfit model](manage-model.md#overfit-models)).

Depending on the data distribution of your historical data, the actual accuracy rates that correspond to the above grades can vary. The difference accounts for the fact that the improvement relative to your baseline rate changes when you move that baseline.

Let's say your model predicts whether a shipment will arrive on time. If your historical on-time rate is 80&nbsp;percent, a performance score of 92 would correspond to a B grade. But, if your historical on-time rate is only 50&nbsp;percent, 92 would correspond to an A grade. That's because 92 is a much better improvement over 50&nbsp;percent than it is over 80&nbsp;percent, and you'd expect a random guess to be close to those percentages.

This example shows the accuracy ranges for each grade when the historical data contains different on-time rates for a binary prediction.
<!--note from editor: En dash for number ranges is via Writing Style Guide. -->
| Grade | Accuracy range for historical 25% on-time rate | Accuracy range for historical 50% on-time rate | Accuracy range for historical 80% on-time rate | Accuracy range for historical 95% on-time rate |
|-------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|
| A | 92.5 &ndash; <99.3% | 90 &ndash; 98% | 93 &ndash; <99% | 98.1 &ndash; <99.8% |
| B | 81.3 &ndash; <92.5% | 75 &ndash; <90% | 84 &ndash; <93% | 95.3 &ndash; <98.1% |
| C | 66.3 &ndash; <81.3% | 55 &ndash; <75% | 71 &ndash; <84% | 91.5 &ndash; <95.3% |
| D | <66.3% or ≥99.3% | <55% or ≥98% | <71% or ≥99% | <91.5% or ≥99.8% |

Accuracy rates that correspond to each grade can also vary when you're predicting more than two outcomes. Let's say your model predicts more than two options for delivery: early, on time, or late.

The accuracy ranges for each grade changes when your historical on-time rates change.

Grade|Early (33.3%)|Early (20%)|Early (10%)
:-----:|:-----:|:-----:|:-----:
| |**On time (33.3%**)|**On time (40%**)|**On time (80%)**
| |**Late (33.4%)**|**Late (40%)**|**Late (10%)**
A|86.7 &ndash; <98.7%|87.2 &ndash; <98.7%|93.2 &ndash; <99.3%
B|66.7 &ndash; <86.7%|68.0 &ndash; <87.2%|83.0 &ndash; <93.2%
C|40.0 &ndash; <66.7%|42.4 &ndash; <68.0%|69.4 &ndash; <83.0%
D|33.3 &ndash; <40.0%|36.0 &ndash; <42.4%|66.0 &ndash; <69.4%


### Performance score

For numerical prediction, we use a performance score. This score measures performance differently than the grades discussed previously.

Let's say you're predicting the number of days to fulfill, ship, and deliver an order. The model predicts a set of numbers. The performance score shows the distances between predicted values and actual values in your training data. This is expressed as a number from 0 through 100 percent<!--Edit okay? Style Guide says to use this structure when the range includes the numbers on either side of it. If the range excludes 0 and 100, then "between" is better.-->, with higher values indicating the predicted value is closer to the real value. Typically, a higher score means the model performs better. Remember though, that perfect or near-perfect scores ([overfit models](manage-model.md#overfit-models)) are usually indicative of a problem with your training data.

The following table has some broad guidance for performance scores.

|Score |Guidance  |
|---------|---------|
| ≥50% |Consistent scores greater than 50% mean that your model performs better than a guess. Generally, the higher the score, the more accurate the model.   |
|<50%  ([underfit](manage-model.md#underfit-models))  |Consistent scores below 50% mean that something is wrong with your model. It's wrong more often than a simple guess would be. This is known as an underfit model. Perhaps your data fields aren't mapped correctly, or you're using the wrong data.    |
|~99% &ndash; 100%  ([overfit](manage-model.md#overfit-models))   |Consistent scores close to 100% can indicate bias in the training data, or that a field that is correlating directly to the answer. This is known as an overfit model.     |
|50% &ndash; ~98%   |If your scores are consistently between 50% and approximately 98%, you must assess whether the performance is appropriate for your intended use of the AI model. Different model implementations have different tolerance for inaccuracy. Predictions for revenue, fraud rates, or delivery timelines all have different levels of accuracy that will determine whether the AI model is practical to use.     |

## Performance details

For training details, select **See details** on the grade box for the model.

>[!NOTE]
 >For information about additional features planned for this area, see [release plans](https://docs.microsoft.com/power-platform-release-plan/2020wave1/ai-builder/).

### Predicting two or more options

The following performance information is available:
- Performance grade
- Accuracy score

#### Performance grade

In addition to the grade for your model, information about each grade and the corresponding accuracy range appears on the model details page. This tells you how much room you might have to improve your model.

<!-- note from editor: This heading was a red herring; commenting it out for now. ### Numerical prediction -->

#### Accuracy score

AI Builder calculates the accuracy score for your model based on the prediction result of the test dataset. Before training, AI Builder separates your dataset into separate training data and testing datasets. After training, AI Builder applies your AI model to the testing dataset, and then calculates your accuracy score. For example: if your test dataset has 200 records, and AI Builder correctly predicted 192 of them, AI Builder shows an accuracy score of 96&nbsp;percent. More information: [Evaluate your model](manage-model.md#evaluate-your-model)

The following performance information is available:

- Training date
- Data source
- Historical outcome
- Entity list used to do prediction


<!-- Coming May 2020 tentatively
- Accuracy per outcome
- Confusion matrix
- Cumulative gains chart -->

<!--
### Accuracy per outcome
This section shows the distribution of correct and incorrect results. You can use this to help you evaluate the model.
AI Builder shows a bar chart to quantify the accuracy of your AI model. Let's still use the business loan application as an example. The "Approved" bar would show how many predictions match the actual result, compared to all the records processed. If the rate of the correctly predicted records is high, this information might help you decide to go ahead and use this model. 

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

## Improve your prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve its performance. Here are some things you can try to help improve your model's predictive power.

### Review errors and issues

- If there are any errors after you finish training, fix them and retrain the model.
- If there are no errors, check the training details. Try to address as many issues as possible, and then retrain the model.

### Review top influencers

After each training, a list of top influencers appears on the model details page. Each field used in the training has a score to represent its influence on the training. These scores combine to equal 100 percent.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers' intention and you're expecting Age, Product as the most influential field, you should see that in the most influential field list in model details page. If not, it might indicate that the training result is not as expected. In this case, you can either deselect the irrelevant or misleading fields and retrain the model, or check your training issues to see further details.<!--Edit okay? I wasn't sure what this was saying. -->

### Add more data

The minimum requirement for training data is 50 records, but this doesn't mean 50 data records will train a highly predictive model. Try to provide 1,000 or more data records, correctly labeled, with a realistic distribution between options.

### Check your data distribution

For example, if you're using two option labels of *Yes* or *No*, and most of your data records only have *Yes* in this field, it's hard for your model to learn from this data. Try to have a distribution of options in your data that roughly reflects the distribution of the options you might expect to see. For example, if you're looking at data fields for *cat_owner* and *dog_owner*, use a data distribution somewhere around 50&nbsp;percent. If you're looking at fraudulent transactions, use a more imbalanced distribution&mdash;perhaps 95&nbsp;percent to 5&nbsp;percent. Look to industry standards for this type of information if you don't know what to expect.

### Add more fields

For example, you want to predict which customers are more likely to return and buy your products. You can add more fields to make the training data richer. For example:

- How do they rate the product?
- How much do they use the product?
- Are they an existing customer?

### Narrow selected fields to relevant information

You might already have a lot of correctly labeled training data, with many data fields. Then why might the model still not perform well? It could be that you're selecting fields that lead to unwanted bias. Make sure all the fields you select are relevant to influence what you want to predict. Deselect irrelevant or misleading fields.

### Validate data

- Make sure the data fields don't have high rate of missing values (greater than 99&nbsp;percent). Populate the missing values with default data or remove the data field from the model training.
- If a data field has a high correlation with prediction outcome, remove the data field from the model training.

### Next step

[Use your prediction model in Power Apps](prediction-model-driven-app.md)
