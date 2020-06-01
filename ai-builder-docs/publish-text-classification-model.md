---
title: Publish your category classification model - AI Builder | Microsoft Docs
description: Provides the information you need to know to publish your category classification model in AI Builder.
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 01/03/2020
ms.author: v-dehaas
ms.reviewer: v-dehaas
---

# Publish your category classification model

When you're satisfied with your model, you can publish it. After it's published, your model is ready to run on your Common Data Service data or be used through Power Automate. It can take up to two hours for the results to be available.

In the **Model settings** pane on the right side of the screen, you can turn on Common Data Service and get important information about where the suggested tags will be stored.

> [!IMPORTANT]
> - Currently, you can only schedule Common Data Service runs by using the input entity and field that you used for training. AI Builder creates a destination entity where the model will store the suggested tags and their confidence scores. This destination entity will have an N:1 (many-to-one)<!--Suggested.--> relationship with your source/input entity.
> - AI Builder uses Power Automate to schedule and run tagging on your data. When you publish your model to run on your Common Data Service data, this will use Power Automate runs from your subscription.

More information: [Publish your model in AI Builder](publish-model.md)

## Where will suggested tags be stored?

The following entity will be created<!--What does "to your entity" mean?--> when you publish a model: **TC_{*Model_Name*}**

Tags will be stored in a field called **new_Tags** under this entity.

> [!NOTE]
> Due to the character limitation of the field name, if the provided syntax creates text that is over the character limit, AI Builder cuts off the end of the text. This means that the model name might be incomplete or missing. You should choose shorter names so everything is visible.

### Next step

[View generated predictions](text-classification-view-predictions.md)
