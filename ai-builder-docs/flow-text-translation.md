---
title: Use the text translation prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the text translation prebuilt model in your Flows
author: alanabrito

ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 06/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the text translation prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Translate text into another language** in text in the list of actions.
1. Select the target language in the **Translate to** input and specify the **My Text** column from the trigger in the **Text** input. 
1. Optionionally, select the source language in the **Translate from** input after clicking at "Show More" to specify the language of the text in "My Text" column (if you don't specify this input, the model will automatically detect the source language for you).

    > [!div class="mx-imgBorder"]
    > ![Trigger text translation flow](media/trigger-text-translation.png "Trigger text translation flow")

1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can use get a notification of the translated text sent out to your email using the "Send me a notification email" and the output property "Text" from the text translation model.

    > [!div class="mx-imgBorder"]
    > ![Text translation flow example](media/text-translation-flow-example.png "Text translation flow example")
    
Congratulations! You've created a flow that uses a sentiment analysis model. Select **Save** on the top right and then select **Test** to try out your flow.



## Parameters
### Input
|Name |Required |Description |Values |
|---------|---------|---------|---------|
|Text |Yes |Text to translate |Text sentences |
|Translate to |Yes |Target language of the translated text | Item in a list of predefined languages or a language code (ex.: "en", "fr", "zh_chs", "ru")
|Translate from |No |Language of the text to be translated | Item in a list of predefined languages or a language code (ex.: "en", "fr", "zh_chs", "ru")

### Output
|Name |Description |Values |
|---------|---------|---------|
|Text |Translated version of the input text|Text sentences |
|Detected language |Detected language of the input text if the column "Translated from" wasn't specified |Language code (ex.: "en", "fr", "zh_chs", "ru")|

### Related topic

[Text translation overview](prebuilt-text-translation.md)
