---
title: Use the text translation prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the text translation prebuilt model in your Flows
author: alanabrito

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the text translation prebuilt model in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Translate text into another language** in text in the list of actions.
1. Select the target language in the **Translate to** input and specify the **My Text** field from the trigger in the **Text** input. 
1. Optionionally, select the source language in the **Translate from** input after clicking at "Show More" to specify the language of the text in "My Text" field (if you don't specify this input, the model will automatically detect the source language for you).

    > [!div class="mx-imgBorder"]
    > ![Trigger text translation flow](media/trigger-text-translation.png "Trigger text translation flow")

1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can use get a notification of the translated text sent out to your email using the "Send me a notification email" and the output property "Text" from the text translation model.

    > [!div class="mx-imgBorder"]
    > ![Text translation flow example](media/text-translation-flow-example.png "Text translation flow example")
    
Congratulations! You've created a flow that uses a sentiment analysis model. Select **Save** on the top right and then select **Test** to try out your flow.


### Related topic

[Text translation overview](prebuilt-text-translation.md)
