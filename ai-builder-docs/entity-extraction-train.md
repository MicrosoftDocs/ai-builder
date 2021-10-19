---
title: Train and publish your custom entity extraction AI model - AI Builder | Microsoft Docs
description: Provides steps to train and publish your custom entity extraction AI model in AI Builder.
author: mfotedar
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 04/08/2020
ms.author: mfotedar
ms.reviewer: kvivek
---

# Train and publish your entity extraction custom model

After you create your entity extraction model, you can train and publish it to make it available.

## Train and validate your model

1. After you create your model, select **Next** to check your selected entities. If everything looks good, select **Train** to train your model.

1. On the **Training complete** screen, select **Go to Details page**.

## Quick-test your model

You can use the **Details** page to test your model before you publish or use it:

1. On the **Details** page, enter the text you want to test.

The quick test should only take a few seconds before displaying the results.

## Publish your model

If you're happy with your model, you can select **Publish** to publish it. When publishing is completed, your model is promoted as published and is ready to be used. More information: [Publish your model in AI Builder](publish-model.md)

After you've published your model, you can use it in a Power Apps canvas app or in Power Automate.

## Edit your model

 You can create a new version of your published model by selecting **Edit model** on the model details page. You can create new entity types or modify existing entity types.

### See also

[Feature availability by region](availability-region.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]