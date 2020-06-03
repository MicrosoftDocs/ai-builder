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

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1.	Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1.	Select **+ New step**, search for the term **AI Builder**, and then select **Extract the key phrases from text** in the list of actions.
1.	Select the language in the Language input and specify the **My Text** field from the trigger in the Text input:

    > [!div class="mx-imgBorder"]
    > ![Specify my text](media/flow-kpe.png "Specify my text")



1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can create a common data service record for each **Key phrase**:

    > [!div class="mx-imgBorder"]
    > ![Add key phrases screen](media/flow-add-phrase-2.png "Add key phrases in Common Data Service")

Congratulations! You have created a flow that uses your key phrase extraction AI model. Select **Save** on the top right and then select **Test** to try out your flow.


### Related topic

[Key phrase extraction overview](prebuilt-key-phrase.md)
