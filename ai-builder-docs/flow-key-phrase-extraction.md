---
title: Use the key phrase extraction prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to set up and use the AI Builder key phrase extraction prebuilt model in Power Automate.
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 03/10/2020
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the key phrase extraction prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **My flows** tab, and then select **Create from blank**.
1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.
1. Select **Text**, and enter **My Text** as the input title.
1. Select **+Add an input** again.
1. Select **Text**, and enter **My Language** as the input title.
1. Select **+ New step**, search for *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.
    >[!NOTE]
    > **Predict Common Data Service (current Environment)** doesn't appear unless you've followed these instructions first: [Create a flow in a solution](/flow/create-flow-solution).
1. Specify the **My Language** field from the trigger in the **Language** input, and the **My Text** field in the **Text** input.

   > ![Manually trigger flow screen](media/flow-trigger-flow3.png "Manually trigger flow screen")

Now you can iterate through the outputs returned by the key phrase extraction model. In the following example, we add each key phrase to a Common Data Service record.<!--Should you describe what's happening in the image in the alt text, if it's not going to be obvious? Information shouldn't be carried only by a graphic. People might be reading this with low res or no graphics, or they might have low vision or be listening to a screen reader.-->

![Add key phrases screen](media/flow-add-phrase.png "Add key phrases in Common Data Service")

Congratulations! You've created a flow that uses your key phrase extraction model. Select **Save** in the upper-right corner, and then select **Test** to try out your flow.
