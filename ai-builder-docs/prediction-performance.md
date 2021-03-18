---
title: Prediction model performance - AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/19/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and fit of the new model. A summary page for your model shows your model training result. These results are expressed as a performance grade of A, B, C, or D.

## Measuring performance

### Performance grade

After each training, AI Builder shows a grade to help you  evaluate your model's accuracy. The decision about whether your model is ready to publish is one you have to make based on your unique needs and circumstances. AI Builder provides the following performance grades to help you make that judgment call.

#### How to interpret each grade

|Grade |Guidance   |
|---------|---------|
|A|It might still be possible to improve the model, but this is the best grade you can get. |
|B|The model is correct in a lot of the cases. Can it be improved? That depends on your unique circumstances, data, and requirements. |
|C|The model is doing slightly better than a random guess. It might be acceptable for some applications, but in most cases, this is a model that you'd continue to tweak and improve.  |
|D|Something's wrong. Your model is either performing worse than we'd expect a random guess to perform ([underfit model](manage-model.md#underfit-models)). Or, it's performing so well (at or near 100%) that you've probably got a data column that is directly correlated  to the result ([overfit model](manage-model.md#overfit-models)) .

* More information about [underfit models](manage-model.md#underfit-models)
* More information about [overfit models](manage-model.md#overfit-models)

#### Accuracy range varies depending on your data


If you are predicting 2 or more outcomes, the actual accuracy rates that correspond to the above grades can vary depending on the data distribution of your historical data. The difference accounts for the fact that the improvement relative to your baseline rate changes when you move that baseline.

Let's say your model predicts whether a shipment will arrive on time. If your historical on-time rate is 80&nbsp;percent, a performance score of 92 would correspond to a B grade. But, if your historical on-time rate is only 50&nbsp;percent, 92 would correspond to an A grade. That's because 92 is a much better improvement over 50&nbsp;percent than it is over 80&nbsp;percent, and you'd expect a random guess to be close to those percentages.

#### Binary historical data example

This example shows the accuracy ranges for each grade when the historical data contains different on-time rates for a binary prediction.

| Grade | Accuracy range for historical 25% on-time rate | Accuracy range for historical 50% on-time rate | Accuracy range for historical 80% on-time rate | Accuracy range for historical 95% on-time rate |
|-------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|-------------------------------------------------|
| A | 92.5 &ndash; <99.3% | 90 &ndash; 98% | 93 &ndash; <99% | 98.1 &ndash; <99.8% |
| B | 81.3 &ndash; <92.5% | 75 &ndash; <90% | 84 &ndash; <93% | 95.3 &ndash; <98.1% |
| C | 66.3 &ndash; <81.3% | 55 &ndash; <75% | 71 &ndash; <84% | 91.5 &ndash; <95.3% |
| D | <66.3% or ≥99.3% | <55% or ≥98% | <71% or ≥99% | <91.5% or ≥99.8% |


#### Multiple outcome historical data example

Accuracy rates that correspond to each grade can also vary when you’re predicting more than 2 outcomes. Let’s say your model predicts more than two options for delivery: early, on time or late.


The accuracy ranges for each grade changes when your historical on-time rates change.

Grade|Early (33.3%)|Early (20%)|Early (10%)
:-----:|:-----:|:-----:|:-----:
| |**On time (33.3%**)|**On time (40%**)|**On time (80%)**
| |**Late (33.4%)**|**Late (40%)**|**Late (10%)**
A|86.7 &ndash; <98.7%|87.2 &ndash; <98.7%|93.2 &ndash; <99.3%
B|66.7 &ndash; <86.7%|68.0 &ndash; <87.2%|83.0 &ndash; <93.2%
C|40.0 &ndash; <66.7%|42.4 &ndash; <68.0%|69.4 &ndash; <83.0%
D|33.3 &ndash; <40.0%|36.0 &ndash; <42.4%|66.0 &ndash; <69.4%

#### Numerical prediction example

For numerical prediction, AI Builder uses the R-squared statistical measure to calculate your models accuracy grade. The following table shows the grades that correspond to each grade:

|Grade  |R-squared |
|---------|---------|
|A    |    85% - <99%   |
|B    |   60% - <85%      |
|C   |  10% - <60%      |
|D    |   ≥99% or <10%       |

## Performance details

For training details, select **See details** on the model's grade box. On the **Performance** tab, the following information is available:

>[!NOTE]
 >For information about additional features planned for this area, see [release plans](https://docs.microsoft.com/power-platform-release-plan/2020wave1/ai-builder/).


* Performance grade
* Accuracy score
* R-squared

#### Performance grade

#### Accuracy score

AI Builder calculates the accuracy score for your model based on prediction result of the test dataset. Before training, AI Builder separates your dataset into separate training data and testing data sets. And after training, AI Builder applies your AI model to the testing dataset, and then calculates your accuracy score. For example: if your test dataset has 200 rows, and AI Builder correctly predicts 192 of them, AI Builder shows an accuracy score of 96 percent.

For more information, see [Evaluate your model](manage-model.md#evaluate-your-model).

#### R -squared

For numerical prediction, AI Builder calculates an r-squared score after each training. This score measures your model’s ‘goodness of fit’, and is used to determine your model’s performance grade.

Let's say you're predicting the number of days to fulfill, ship, and deliver an order. The model predicts a set of numbers. The r-squared value is based on the distances between predicted values and actual values in your training data. This is expressed as a number between 0 – 100%, with higher values indicating the predicted value is closer to the real value. Typically, a higher score means the model performs better. Remember though, that perfect or near-perfect scores ([overfit models](https://docs.microsoft.com/ai-builder/manage-model#overfit-models)) are usually indicative of a problem with your training data.

On the **Summary** tab, the following performance information is available

* Training date
* Data source
* Historical outcome
* Table list used to do prediction.

## Improve your prediction model performance

After you've trained and evaluated your model, it's time to tweak your model to improve its performance. Here are some things you can try to help improve your model's predictive power.

### Review errors and issues

* If there are any errors after you finish training, fix them and retrain the model.
* If there are no errors, check the training details. Try to address as many issues as possible, and then retrain the model.

### Review top influencers

After each training, a list of top influencers appears on the model details page. Each column used in the training has a score to represent its influence on the training. These scores combine to equal 100 percent.

This helps show whether your model is trained as you expect. For example, if you want to predict online shoppers' intention and you're expecting Age, Product as the most influential column, you should see that in the most influential column list in model details page. If not, it might indicate that the training result is not as expected. In this case, you can either deselect the irrelevant or misleading columns and retrain the model, or check your training issues to see further details.

### Add more data

The minimum requirement for training data is 50 rows, but this doesn't mean 50 data rows will train a highly predictive model. Try to provide 1,000 or more data rows, correctly labeled, with a realistic distribution between options.

### Check your data distribution

For example, if you're using two option labels of *Yes* or *No*, and most of your data rows only have *Yes* in this column, it's hard for your model to learn from this data. Try to have a distribution of options in your data that roughly reflects the distribution of the options you might expect to see. For example, if you're looking at data columns for *cat_owner* and *dog_owner*, use a data distribution somewhere around 50&nbsp;percent. If you're looking at fraudulent transactions, use a more imbalanced distribution&mdash;perhaps 95&nbsp;percent to 5&nbsp;percent. Look to industry standards for this type of information if you don't know what to expect.

### Add more column

For example, you want to predict which customers are more likely to return and buy your products. You can add more columns to make the training data richer. For example:

- How do they rate the product?
- How much do they use the product?
- Are they an existing customer?

### Narrow selected columns to relevant information

You might already have a lot of correctly labeled training data, with many data columns. Then why might the model still not perform well? It could be that you're selecting columns that lead to unwanted bias. Make sure all the columns you select are relevant to influence what you want to predict. Deselect irrelevant or misleading columns.

### Validate data

- Make sure the data columns don't have high rate of missing values (greater than 99&nbsp;percent). Populate the missing values with default data or remove the data column from the model training.
- If a data column has a high correlation with prediction outcome, remove the data column from the model training.

### Next step

[Use your prediction model in Power Apps](prediction-model-driven-app.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]