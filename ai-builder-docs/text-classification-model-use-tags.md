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
ms.reviewer: v-dehaas
---

# Use model to generate tags

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Power Automate

If you want to use your trained model in Power Automate, you can find more information in [Use text classification model in Power Automate](text-classification-model-in-flow.md).

## Set run schedule on Common Data Service

You can set the run schedule by navigating to the **Run** view in the **Model settings** panel. You can configure your model to run on your database to predict tags by choosing the following option:

**Generate predictions when new data is added**

Your model runs once on all existing data in your text entity, and then again whenever a new record is added to that entity.


## What if the model is not writing new tag suggestions?

- Check that you didn’t exceed the number of runs for your Power Automate subscription.
- Turn off the Common Data Service run setting, and then turn it back on.
