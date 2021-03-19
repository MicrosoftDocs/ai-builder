---
title: Training errors and issues - AI Builder | Microsoft Docs
description: Describes the errors and issues that appear on the AI Builder prediction model details page
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/19/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Prediction model training errors and issues

AI Builder reports errors and issues on the model details page. These messages are explained here.

## Errors

When an error occurs, you can't continue until you resolve it. Here are some error messages that might occur:

- *The model needs at least **\<ThresholdValue>** rows to train. **\<TableName>** has only **\<ActualValue>** rows. Add data or select another table.*

    If you have only 50 rows or fewer, you can't train the model. Ideally, you should have at least 1,000 rows.

- *The model needs at least **\<ThresholdValue>** historical outcome rows of each outcome value to train. Add data or select another table.*

    You need at least 10 rows of historical outcome for each class to train the model and predict the outcome.

- *The model requires at least **\<ThresholdValue>** features to train the model. Select the required columns.*

    You don't have any relevant features generated to train the model.

## Issues

These messages don't prevent you from continuing to train and publish your model; instead, they show you issues that might cause your model to under perform.

- *The model might produce better performance with optimum rows of **\<ThresholdValue>** or more to train the model. **\<TableName>** has **\<ActualValue>** rows. Add data for better model performance.*

    You have fewer than 1,000 rows. Ideally, you should provide at least 1,000 rows to train the model.

- ***\<TableName>.\<AttributeName>** might get dropped from training as it has a single value and does not contribute to training the model.*

    Data columns that have less relevance for training the model are dropped&mdash;for example, data columns that all have the same value in each row.

- ***\<TableName>.\<AttributeName>** has a high ratio of missing values, greater than **\<ThresholdValue>** percentage and might not contribute to train the model.*

    For best results, populate data for the data columns that have a high rate of missing values.

- ***\<TableName>.\<AttributeName>** has **\<ThresholdValue>** percent correlation **\<CorrelationName>** with **\<OutcomeAttributeName>** and model might suspect to cause target leak.*

    Data columns that have a high correlation with the outcome of a prediction are dropped in model training.

### See also

[Common issues and resolutions for AI Builder](common-issues.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]