---
title: Create a prediction model -  AI Builder | Microsoft Docs
description: This topic lays out the steps you need to follow to create a prediction model in AI Builder. 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 11/22/2019
ms.author: sdarapu
ms.reviewer: v-dehaas
---

# Create a prediction model

This example creates a Power Apps prediction AI model that uses the *online shopper intention* Common Data Service entity.  To get this sample data into your Common Data Service environment. enable the **Deploy sample apps and data** setting when you create an environment as described in the [Build a model in AI Builder](build-model.md). Or, follow the more detailed instructions in the [Data preparation](prediction-data-prep.md). After your sample data is in Common Data Service, follow these steps to create your model:

1. Sign in to [Power Apps](https://make.powerapps.com) and then select **AI Builder > Build**.
2. Select **Prediction**. Enter a model name and then select **Create**.

## Select your historical outcome

Think of the prediction you want AI Builder to make. For example, for the question “Will my customer churn?”, think about questions like these:

- Where is the entity that contains information about customer churn?
- Is there a field there that specifically states whether the customer has churned?
- Are there unknowns in a field that might cause uncertainty?

Use this information to make your selections. Working with provided sample data, the question is "did this user who interacted with my online store make a purchase?". If they did, then there should be revenue for that customer. Therefore, whether there's revenue for this customer should be my historical outcome. Wherever this information is empty is where AI Builder can help you make a prediction.

1. In the **Entity** dropdown menu, select the entity that contains the data and the outcome you want to predict. For the sample data, select **Online shopper intention**.
1. In the **Field** dropdown menu, select field that contains the outcome. For the sample data, select and **Revenue (Label)**.
1. If you selected an option set that contains two or more outcomes, consider mapping it to “Yes” or “No” since you want to predict whether or not something will happen.

> [!NOTE]
> AI Builder supports these data types for the outcome field:
> - Two options
> - Option set

## Select the data fields to train your model

After you select the **Entity** and **Field** and map your outcome, you can make changes to the data fields used to train the model. By default, all relevant fields are selected. You can deselect fields that may contribute to a less accurate model. If you don’t know what to do here, don’t worry. AI Builder will try to find fields that provide the best model possible. For the sample data, just leave everything as is and select **Next**.

### Data field selection considerations

The most important thing to consider here is whether a column that is not your historical outcome field is indirectly determined by the outcome.

Let’s say you want to predict whether a shipment is going to be delayed. You might have the actual delivered date in your data. That date is only present after the order is delivered. So, if you include this field, the model will have close to 100% accuracy. The orders that you want to predict won’t be delivered yet, and won’t have the delivered date field populated. So, you should deselect fields like this before training. In machine learning, this is called target leakage or data leakage. AI Builder tries to filter fields that are “too good to be true”, but you should still check.

> [!NOTE]
> When selecting data fields, some data types like Image which cannot be used as input to train the model are not shown. In addition, system fields like Created On are excluded by default.

### Use data from related entities

If you have related entities that may improve the performance of the prediction, you can include those as well. Like predicting whether a customer will churn, you should include additional information that may be in a separate entity. Ai Builder supports many-to-one relationships at this time.

## Filter your data

After you select data fields for training, you can filter to your data. Your entities will contain all records. However, you may want to concentrate on training and predicting on a subset of records. If you know that there are irrelevant data within the same entity you are using to train a model, you can use this step to filter it.

For example, if you apply a filter to  look at only the U.S. region, the model will train on records where the outcome is known only for U.S. region. When this model is trained, it will only make a prediction for records where the outcome is not known for only the U.S. region.

The filtering experience is the same as in the PowerApps view editor. Start by adding either:

- A row, which contains a single filter condition.
- A group, which allows you to nest your filter conditions.
- A related entity, which allows you to create a filter condition on a related entity. 

Select the field, the operator, and the value that represents a filter condition. You can use the checkboxes to group rows, or bulk delete rows.

> [!NOTE]
> There is currently an issue with filtering on related entities that have a one-to-many relationship. This will be addressed in a week or two.

### Next step
[Train and publish your prediction model](prediction-train-model.md)<br/>
