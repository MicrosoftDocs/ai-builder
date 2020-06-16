---
title: Create a prediction model - AI Builder | Microsoft Docs
description: This topic lays out the steps you need to follow to create a prediction model in AI Builder. 
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 11/22/2019
ms.author: sdarapu
ms.reviewer: v-dehaas
---

# Create a prediction model

This example creates a Power Apps prediction AI model that uses the Online Shopper Intention entity in Common Data Service. To get this sample data into your Common Data Service environment, enable the **Deploy sample apps and data** setting when you create an environment as described in [Build a model in AI Builder](build-model.md). Or, follow the more detailed instructions in [Data preparation](prediction-data-prep.md). After your sample data is in Common Data Service, follow these steps to create your model.

1. Sign in to [Power Apps](https://make.powerapps.com), and then select **AI Builder** > **Build**.

1. Select **Prediction**. Enter a name for your model, and then select **Create**.

## Select your historical outcome

Think of the prediction you want AI Builder to make. For example, for the question "Will a this customer churn?, think about questions like these:

- Where is the entity that contains information about customer churn?
- Is there a field there that specifically states whether the customer has churned?
- Are there unknowns in a field that might cause uncertainty?

Use this information to make your selections. Working with provided sample data, the question is "did this user who interacted with my online store make a purchase?" If they did, there should be revenue for that customer. Therefore, whether there's revenue for this customer should be the historical outcome. Wherever this information is empty is where AI Builder can help you make a prediction.

1. In the **Entity** drop-down menu, select the entity that contains the data and the outcome you want to predict. For the sample data, select **Online shopper intention**.

1. In the **Field** drop-down menu, select the field that contains the outcome. For the sample data, select **Revenue (Label)**. Or, if you want to try out predicting a number, select **ExitRates**.

1. If you selected an option set that contains two or more outcomes, consider mapping it to "Yes" or "No" because you want to predict whether or not<!--Just FYI, the Style Guide says just to use "whether" instead of "whether or not," but in this case "whether or not" maps better to those two outcomes you're describing.--> something will happen.

1. If you want to predict multiple outcomes, use the Brazilian e-commerce dataset in the sample, and select **BC Order** in the **Entity** drop-down menu and **Delivery Timelines** in the **Field** drop-down menu. 

> [!NOTE]
> AI Builder supports these data types for the outcome field:
>
> - Two options
> - Option set
> - Whole number
> - Decimal number
> - Floating point number
> - Currency

## Select the data fields to train your model

After you select the **Entity** and **Field** and map your outcome, you can make changes to the data fields used to train the model. By default, all relevant fields are selected. You can deselect fields that might contribute to a less accurate model. If you don't know what to do here, don't worry. AI Builder will try to find fields that provide the best model possible. For the sample data, just leave everything as is and select **Next**.

### Data field selection considerations

The most important thing to consider here is whether a column that isn't your historical outcome field is indirectly determined by the outcome.

Let's say you want to predict whether a shipment is going to be delayed. You might have the actual delivered date in your data. That date is only present after the order is delivered. So, if you include this field, the model will have close to 100&nbsp;percent accuracy. The orders that you want to predict won't have been delivered yet, and won't have the delivered date field populated. So, you should deselect fields like this before training. In machine learning, this is called _target leakage_ or _data leakage_. AI Builder tries to filter fields that are "too good to be true," but you should still check them.

> [!NOTE]
> When you're selecting data fields, some data types&mdash;like Image, which can't be used as input to train the model&mdash;aren't shown. In addition, system fields like Created On are excluded by default.

### Use data from related entities

If you have related entities that might improve the performance of the prediction, you can include those as well. As you did when you wanted to predict whether a customer will churn, you should include additional information that might be in a separate entity. AI Builder supports many-to-one relationships at this time.

## Filter your data

After you select data fields for training, you can filter on your data. Your entities will contain all records. However, you might want to concentrate on training and predicting on a subset of records. If you know that there's irrelevant data within the same entity you're using to train a model, you can use this step to filter it.

For example, if you apply a filter to look at only the US region, the model will train on records where the outcome is known only for the US region. When this model is trained, it will only make a prediction for records where the outcome is not known for only the US region.

The filtering experience is the same as in the Power Apps view editor. Start by adding:

- A row, which contains a single filter condition.
- A group, which allows you to nest your filter conditions.
- A related entity, which allows you to create a filter condition on a related entity. 

Select the field, the operator, and the value that represents a filter condition. You can use the check boxes to group rows or to bulk-delete rows.

### Next step

[Train and publish your prediction model](prediction-train-model.md)<br/>
