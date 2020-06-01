---
title: Use the text recognition prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to text recognition prebuilt model in Power Automate 
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the text recognition prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/signin), select the **My flows** tab, and then select **Create from blank**.

1. Search for the term **manually**, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.

1. Select **File**, and enter **My Image** as the input title.

1. Select **+ New step**, search for the term **Predict**, and then select **Predict - Common Data Service (Conversational Environment)** in the list of actions.
    >[!NOTE]
    > **Predict Common Data Service (current Environment)** doesn't appear unless you've followed these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Select **Text recognition model**, and specify the **My Image** field from the trigger in the **Image** input.

    > ![Trigger text recognition flow](media/trigger-text-recognition.png "Trigger text recognition flow")

Now you can use the extracted text lines by the text recognition model. In the following example, we save the extracted text to a SharePoint list.<!--Should the alt text describe any details that the reader needs but might not be seeing (for various reasons)? -->

> ![Text recognition flow example](media/text-flow-example2.png "Text recognition flow example")

Congratulations! You've created a flow that uses the text recognition model. You can continue to build on this flow until it suits your needs. Select **Save** in the upper-right corner, and then select **Test** to try out your flow. 
