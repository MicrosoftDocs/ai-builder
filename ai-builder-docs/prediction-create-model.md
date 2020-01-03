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


## Select the data fields to train your model

After you select the **Entity** and **Field** and map your outcome, you can make changes to the data fields used to train the model. By default, all relevant fields are selected (we may have deselected some system fields, which should have no impact to the model). You can deselect fields that may contribute to a less accurate model. If you don’t know what to do here, don’t worry. AI Builder will try to filter fields to provide the best model possible. For the sample data, just leave everything as is and select **Next**.

### Data field selection considerations

The most important thing to consider here is whether a column that is not your historical outcome field already contains the prediction.

Let’s say you want to predict whether a shipment is going to be delayed. You might have the actual delivered date in your data. That date is only present after the order is delivered. So, if you include this field, the model will have close to 100% accuracy. The orders that you want to predict won’t be delivered yet, and won’t have the delivered date field populated. So, you should deselect fields like this before training. In machine learning, this is called target leakage or data leakage. AI Builder tries to filter fields that are “too good to be true”, but you should still check.

- Make sure you select the data fields that you want to use in training the model.
- Deselect the data fields that don't address the problem you want to solve.
- Deselect the data fields that might carry unwanted bias.
- Make sure the data fields you select don't have a high rate of missing values. If it's a valuable data field, you can assign a default value.

> [!NOTE]
> These Common Data Service data types are excluded from the prediction model. These will not appear in the **Field** drop-down menu:

> - Customer
> - Image
> - Lookup
> - Multiple selection Option set
> - Multiline Text
> - Owner
> - Unique Identifier
> - String type data types with length greater than 100 characters

### Next step
[Train and publish your prediction model](prediction-train-model.md)<br/>
