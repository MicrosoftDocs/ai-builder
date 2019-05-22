---
title: Publish your text classification model | Microsoft Docs
description: Provides steps to publish your text classification model AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Publish your text classification model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

When you are satisfied with your model, you can publish it. When it’s published, your model is ready to run on your Common Data Services data. Please note that it will take up to two hours for the results to be available.

In the **Model settings** pane on the right side of the screen, you can turn on Common Data Service, and get important information on where the suggested tags will be stored.

>!IMPORTANT
>
>Currently, you can only schedule Common Data Service runs using the input entity and field you used for training. AI Builder creates a destination entity where the model will store the suggested tags and their confidence scores. This destination entity will have N:1 relationship with your source/input entity. 

>!NOTE
>
>AI Builder uses Microsoft Flow to schedule and run tagging on your data. When you publish your model to run on your Common Data Service data, this will consume Flow runs from your subscription.

For more information about publishing your AI Model, go to the [Publish a model in AI Builder](publish-model-ai-builder.md) section of this document.

## Where will suggested tags be stored?
The following entity will be created to your entity when you publish a model: **TC_{*Model_Name*}**.
Tags will be stored in a field called “**new_Tags**” under this entity.

> !NOTE
>
> Due to the character limitation of the field name, if the syntax provided creates text that is over the character limit, AI Builder cuts off the end of the text. This means that the project name may be incomplete or missing. You should choose shorter names so everything is visible.

## View generated tags
In this section we show you how to view the output of your prediction model.
 
1.	After you publish your model, the Output location appears in the Performance section.
    ![Tags output location screen](media/tags-output-location.png)

    The name shown in **Output** in the **Performance** section is the name of the entity and attribute that is created after publishing. It is a link that takes you to the entity viewer section where the new fields that are added by AI Builder appear. 
 
2.	In the **Views** section, you can view the values of the output fields for the different records. You can use the **Filter by** function in the lower right-side pane to filter for only the records that do not have a label.
3.	Next, you can build a simple model-driven app to consume the output. For information about how to build a model driven app in PowerApps, go to the [model-driven app overview](https://docs.microsoft.com/powerapps/maker/model-driven-apps/model-driven-app-overview) topic in PowerApps docs.





### See also
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[PowerApps docs](https://docs.microsoft.com/powerapps/)<br/>
[Microsoft Flow docs](https://docs.microsoft.com/flow/getting-started)
