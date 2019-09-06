---
title: Use model to generate tags -  AI Builder | Microsoft Docs
description: Provides information about how to use text classification model–generated tags, and some troubleshooting information
author: raaourik 
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: raaourik 
ms.reviewer: kvivek
---

# Use model to generate tags

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Microsoft Flow

If you want to use your trained model in Microsoft Flow, you can find more information in [Use text classification model in Microsoft Flow](text-classification-model-in-flow.md).

## Set run schedule on Common Data Service

You can set the run schedule by navigating to the **Run** view in the **Model settings** panel. You can configure your model to run on your database to predict tags in two ways:

- **Generate predictions when new data is added**

    Your model runs once on all existing data in your text entity, and then again whenever a new record is added to that entity.

- **Generate predictions regularly for all data**

    Your model runs on scheduled intervals (day/week/month) and generates predictions on all text data in your entity.

## What if the model is not writing new tag suggestions?

- Check that you didn’t exceed the number of runs for your Microsoft Flow subscription.
- Turn off the Common Data Service run setting, and then turn it back on.
