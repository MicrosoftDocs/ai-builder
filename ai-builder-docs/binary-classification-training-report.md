---
title: Understand the training report| Microsoft Docs
description: Describes the binary classification model training report
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Understand the training report

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]


Here are some of the details to help you understand the training report errors and warnings. 
## Errors
- *Not enough data to train your model*

    If you only have 50 records or less, you can’t train the model. Ideally, you should have at least 1000 records or more.

- *Not enough examples of each historical outcome to train your model*

    You need at least 10 records of historical outcome for each class to train the model and predict the outcome.

- *Not enough relevant data to train your model*

    You don’t have any relevant data to create the model.

## Warnings
- *Less than 1000 records provided*

    You have less than 1000 records. Ideally, you should provide at least 1000 records to train the model.

- *Some fields had low relevance*

    You should delete data fields that have less relevance to train the model. For example, data fields that all have the same value in each record.

- *Some fields were missing values*

    You should delete data fields that have a high rate of missing values.

- *Some fields were dropped during training*

    Data fields that have a high correlation with prediction outcome may be dropped in model training.

