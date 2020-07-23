---
title: Training errors and issues - AI Builder | Microsoft Docs
description: Describes the errors and issues that appear on the AI Builder prediction model details page
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 01/03/2020
ms.author: sdarapu
ms.reviewer: v-dehaas
---

# Training errors and issues
<!--Is it all right that this heading doesn't mention the prediction model specifically? It probably should if similar topics for other types of models might be written someday.-->
AI Builder reports errors and issues<!--Suggested, to avoid "issue messages" and also to echo the H2s below.--> on the model details page. These messages are explained here.

## Errors

When an error occurs, you can't continue until you resolve it. Here are some error messages that might occur:
<!--Suggest using full HTML. Some strings dropped out of these messages in the published version! I think it was just too complex for markdown.-->
- *The model needs at least **\<ThresholdValue>** records to train. **\<EntityName>** has only **\<ActualValue>** records. Add data or select another entity.*

    If you only have 50 records or less, you can't train the model. Ideally, you should have at least 1,000 records.

- *The model needs at least **\<ThresholdValue>** historical outcome records of each outcome value to train. Add data or select another entity.*

    You need at least 10 records of historical outcome for each class to train the model and predict the outcome.

- *The model requires at least **\<ThresholdValue>** features to train the model. Select the required fields.*

    You don't have any relevant features generated to train the model.

## Issues

These messages don't prevent you from continuing to train and publish your model; instead, they show you issues that might cause your model to underperform.

- *The model might produce better performance with optimum records of **\<ThresholdValue>** or more to train the model. **\<EntityName>** has **\<ActualValue>** records. Add data for better model performance.*

    You have fewer than 1,000 records. Ideally, you should provide at least 1,000 records to train the model.

- ***\<EntityName>.\<AttributeName>** might get dropped from training as it has a single value and does not contribute to training the model.*

    Data fields that have less relevance for training the model are dropped&mdash;for example, data fields that all have the same value in each record.

- ***\<EntityName>.\<AttributeName>** has a high ratio of missing values, greater than **\<ThresholdValue>** percentage and might not contribute to train the model.*

    For best results, populate data for the data fields that have a high rate of missing values.

<!--Can you do something about the grammar of this message? It needs to be passive voice. I'm not sure whether the model or the data is suspected of causing the target leak, but a model can't actually suspect anything.-->
- ***\<EntityName>.\<AttributeName>** has **\<ThresholdValue>** percent correlation **\<CorrelationName>** with **\<OutcomeAttributeName>** and model might suspect to cause target leak.*

    Data fields that have a high correlation with the outcome of a prediction are dropped in model training.
