---
title: Training errors and issues - AI Builder | Microsoft Docs
description: Describes the errors and issues that appear on the AI Builder prediction model details page
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 12/18/2020
ms.author: norliu
ms.reviewer: kvivek
---

# Prediction model training errors and issues

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

AI Builder reports errors and issues on the model details page. These messages are explained here.

## Errors

When an error occurs, you can't continue until you resolve it. Here are some error messages that might occur:

- *The model needs at least **\<ThresholdValue>** records to train. **\<EntityName>** has only **\<ActualValue>** records. Add data or select another entity.*

    If you only have 50 records or less, you can't train the model. Ideally, you should have at least 1,000 records.

- *The model needs at least **\<ThresholdValue>** historical outcome records of each outcome value to train. Add data or select another entity.*

    You need at least 10 records of historical outcome for each class to train the model and predict the outcome.

- *The model requires at least **\<ThresholdValue>** features to train the model. Select the required fields.*

    You don't have any relevant features generated to train the model.

## Issues

These messages don't prevent you from continuing to train and publish your model; instead, they show you issues that might cause your model to under perform.

- *The model might produce better performance with optimum records of **\<ThresholdValue>** or more to train the model. **\<EntityName>** has **\<ActualValue>** records. Add data for better model performance.*

    You have fewer than 1,000 records. Ideally, you should provide at least 1,000 records to train the model.

- ***\<EntityName>.\<AttributeName>** might get dropped from training as it has a single value and does not contribute to training the model.*

    Data fields that have less relevance for training the model are dropped&mdash;for example, data fields that all have the same value in each record.

- ***\<EntityName>.\<AttributeName>** has a high ratio of missing values, greater than **\<ThresholdValue>** percentage and might not contribute to train the model.*

    For best results, populate data for the data fields that have a high rate of missing values.

- ***\<EntityName>.\<AttributeName>** has **\<ThresholdValue>** percent correlation **\<CorrelationName>** with **\<OutcomeAttributeName>** and model might suspect to cause target leak.*

    Data fields that have a high correlation with the outcome of a prediction are dropped in model training.

## See also

[Common issues and resolutions for AI Builder](common-issues.md)
