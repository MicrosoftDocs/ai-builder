---
title: Use a model to generate tags - AI Builder
description: Provides information about how to use category classification model–generated tags, and some troubleshooting information
author: v-aangie 
ms.topic: how-to
ms.custom: 
ms.date: 09/08/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use a category classification model to generate tags

## Use in Power Automate

If you want to use your trained model in Power Automate, go to [Use a category classification custom model in Power Automate](text-classification-model-in-flow.md).

<a name="set-run-schedule-on-common-data-service"></a>

## Use in Power Apps

You can integrate your AI Builder category classification models in Power Apps Studio by using the formula bar. For more information, go to [Use Power Fx in AI Builder models in Power Apps (preview)](powerfx-in-powerapps.md).

## Set a run schedule on Microsoft Dataverse (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Create a schedule to generate predictions regularly in Microsoft Dataverse.

1. To set the run schedule, go to the **Run** view in the **Model settings** panel.

1. To configure your model to run on your database and generate predictions, select **Generate predictions when new data is added**.

Your model runs whenever a new row is added to its table.

To learn more, go to [Run your prediction model](prediction-use.md#prediction-run).

> [!NOTE]
>You can’t set run schedule for imported category classification models.

## What if the model isn't writing new tag suggestions?

- Check that you didn't exceed the number of runs for your Power Automate subscription.

- Turn off the Dataverse run setting, and then turn it back on.

[!INCLUDE[footer-include](includes/footer-banner.md)]
