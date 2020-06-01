---
title: Use the language detection prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the AI Builder language detection prebuilt model in your flows
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the language detection prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/signin), select the **My flows** tab, and then select **Create from blank**.

1. Search for the term **manually**, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.
1. Select **Text**, and enter **My Text** as the input title.
1. Select **+ New step**, search for the term **Predict**, and then select **Predict Common Data Service (current Environment)** in the list of actions.
    >[!NOTE]
    > **Predict Common Data Service (current Environment)** doesn't appear unless you've followed these instructions first: [Create a flow in a solution](/flow/create-flow-solution).
1. Select **LanguageDetection model**. 
1. Specify the **My Text** field from the trigger in the **Text** input, and then specify the two-letter country code for your default country. 

   >[!NOTE]
   >You can use the countryHint parameter to specify a two-letter country code. 
   >
   >For example, "impossible" is common to English and French languages. With a limited context, the response will be based on the "US" country hint. If the origin of the text is known to be coming from France, that can be given as a hint.

   ![Manually trigger a flow screen](media/trigger-text-flow.png "Manually trigger a flow screens")

Now you can iterate through the detected languages returned by the language detection model. In the following example, we add the detected languages to an existing Common Data Service record.<!--As noted in flow-key-phrase-extraction.md, maybe you should you describe what's happening in the image in the alt text if it won't be obvious to the reader. At the very least, the alt text should be a bit more descriptive than this!-->

![Example](media/text-flow-example.png "Example")

Congratulations! You've created a flow that uses the language detection model. Select **Save**in the upper-right corner, and then select **Test** to try out your flow.
