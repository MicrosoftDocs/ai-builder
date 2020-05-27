---
title: Use model to generate tags - AI Builder | Microsoft Docs
description: Provides information about how to use category classification model–generated tags, and some troubleshooting information
author: raaourik 
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 05/11/2020
ms.author: raaourik 
ms.reviewer: v-dehaas
---

# Use a model to generate tags


[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Power Automate

If you want to use your trained model in Power Automate, you can find more information in [Use category classification model in Power Automate](text-classification-model-in-flow.md).

<a name="set-run-schedule-on-common-data-service"></a>

## Set a run schedule on Common Data Service

Go to the **Run** view in the **Model settings** panel to set the run schedule. To configure your model to run on your database and generate predictions, select **Generate predictions when new data is added**. 

Your model runs whenever a new record is added to that entity.

## Use in Power Apps

### Use the formula bar

You can integrate your AI Builder category classification models in Power Apps maker studio by using the formula bar. More information: [Use formulas for text AI models (Preview)](use-model.md#use-formulas-for-text-ai-models-preview)

## What if the model isn't writing new tag suggestions?

- Check that you didn't exceed the number of runs for your Power Automate subscription.
- Turn off the Common Data Service run setting, and then turn it back on.
