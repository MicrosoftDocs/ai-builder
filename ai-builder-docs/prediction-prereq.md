---
title: Prediction model prerequisites - AI Builder | Microsoft Docs
description: Describes what you should know and what data you need before you can build a prediction model in AI Builder.
author: Dean-Haas
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/19/2021
ms.author: norliu
ms.reviewer: kvivek
---

# Prediction model prerequisites

For information about AI Builder requirements that aren't specific to this AI model, see [AI model prerequisites](build-model.md#prerequisites).

## What skills do I need?

- The person creating the prediction model should know enough about the business in question to understand the meaning of a dataset.

- Because you don't need coding skills to create an AI model in AI Builder, you don't need to be a developer or data scientist to use the AI Builder prediction model. If you aren't familiar with a certain concept, select the **Tips** and **Help** links in AI Builder.

## What data do I need?

- Your data must be in [Microsoft Dataverse](/powerapps/maker/common-data-service/data-platform-intro).
- Make sure your administrator has assigned you a security role with Read privilege over your data.
- You need at least 10 rows of historical outcome for each class of the **Label** data column to train a prediction model.
- The minimum for training is 50 rows, but for best results you should have at least 1,000 rows.

## Work with sample data

To help you get started quickly with prediction, AI Builder provides sample data that you can use to get started. More information: [Use sample data to do prediction](prediction-sample-data.md)

### Next step

[Data preparation](prediction-data-prep.md)

### See also

[AI model prerequisites](build-model.md#prerequisites)


[!INCLUDE[footer-include](includes/footer-banner.md)]