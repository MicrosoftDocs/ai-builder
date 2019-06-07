---
title: Binary classification model prerequisites -  AI Builder | Microsoft Docs
description: Describes what you should know, and what data you need before you can build a binary classification model in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Prerequisites

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

For information about AI Builder requirements that are not specific to this AI model, go to the [Prerequisites section](build-model.md#prerequisites) of this topic.

## What skills do I need?

- The person creating the binary classification model should know enough about the business in question to understand the meaning of a data set. 

- Since no coding is needed to create an AI model in AI Builder, you do not need to be a developer or data scientist to use the AI Builder binary classification model. If you are not familiar with a certain concept, select the **Tips** and **Help** links in AI Builder.

## What data do I need?

- Your data must be in Common Data Service. For more information go to the [Common Data Service](/powerapps/maker/common-data-service/data-platform-intro) section of PowerApps on Microsoft Docs.
- Make sure your administrator has assigned you a security role with read privilege over your data.
- You need at least 10 records of historical outcome for each class of the **Label** data field to train the model and predict the outcome. 
- 50 records is the minimum for training, but for best results you should have at least 1000 records. 

## Sample data

To help you get started quickly with binary classification, use the sample datasets available at <https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder>.

### Next steps

[Data preparation](binary-classification-data-prep.md)
