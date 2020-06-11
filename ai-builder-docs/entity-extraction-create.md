---
title: Create a custom entity extraction AI model -  AI Builder | Microsoft Docs
description: Provides steps to create a custom entity extraction AI model in AI Builder.
author: mfotedar

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/08/2020
ms.author: mfotedar
ms.reviewer: v-dehaas
---

# Create a custom entity extraction AI model 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Create your model

To create your custom entity extraction model, you'll need to:

1. Provide at least 10 examples of your text data.
1. Review the results from already existing prebuilt entities.
1. Refine by creating your own custom entities or modifying the existing prebuilt entities.
1. Review your model and train it.
1. Evaluate your model (optional).

## Upload examples of your text data

You need at least 10 data examples to start customizing the model. AI Builder will identify some entities out of the box.  You can customize by creating new entity types with a small set of examples or by modifying the existing entity types. Upload your data:

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/).
1. In the navigation pane select **AI Builder > Build**. Then, select **Entity Extraction**.
1. Type a name for your model, and then select **Create**.
1. Select the **Common Data Service** entity and the field that contains your data.

## Review & refine entities 

AI Builder will automatically extract the prebuilt entity types from your uploaded examples. If the results are satisfactory, then you don't need to customize a model and can use the [prebuilt entity extraction](prebuilt-entity-extraction.md) model out of the box.

You can customize your entity extraction model in these ways:  

1. Create a new entity type.

   You need to provide at least 5 examples to create a new entity type. For example, to create a new entity type "size", you can add an example like "The suitcase was {large}" . The braces designate that "large" is of entity type size.

1. Modify an existing entity type. 

   You need to add least 5 examples to an existing entity type to modify it.

1. Deselect any prebuilt entities, you don't want to be included in the model.

   You can select/deselect prebuilt entity types from the settings.


### Next step:

[Train and publish your entity extraction model](entity-extraction-train.md).  
