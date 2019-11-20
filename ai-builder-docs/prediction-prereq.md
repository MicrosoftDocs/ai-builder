---
title: Prediction model prerequisites -  AI Builder | Microsoft Docs
description: Describes what you should know, and what data you need before you can build a prediction model in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: tatn
ms.reviewer: v-dehaas
---

# Prerequisites

For information about AI Builder requirements that are not specific to this AI model, go to [this topic](build-model.md#prerequisites).

## What skills do I need?

- The person creating the prediction model should know enough about the business in question to understand the meaning of a dataset.

- Because no coding is needed to create an AI model in AI Builder, you do not need to be a developer or data scientist to use the AI Builder prediction model. If you are not familiar with a certain concept, select the **Tips** and **Help** links in AI Builder.

## What data do I need?

- Your data must be in [Common Data Service](/powerapps/maker/common-data-service/data-platform-intro).
- Make sure your administrator has assigned you a security role with read privilege over your data.
- You need at least 10 records of historical outcome for each class of the **Label** data field to train the model and predict the outcome.
- The minimum for training is 50 records, but for best results you should have at least 1,000 records. 

## Sample data

To help you get started quickly with prediction, use the sample datasets available [here](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder).

### Next step

[Data preparation](prediction-data-prep.md)
