---
title: Use form processing model in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use a form processing model in Power Automate
author: JoeFernandezMS
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Use form processing model in Power Automate


 > [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **File** as the input type, and set as input title **File Content**.
1. Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Process and save information from forms** in the list of actions.
1.	Select the form processing model you want to use, select the Document type, and in the **Document** field add **File Content** from the trigger:

    > [!div class="mx-imgBorder"]
    > ![Select file content](media/flow-select-file-content-2.png "Select file content")

1. In the successive actions, you can use any fields and tables extracted by the AI Builder model. For example, let's say that our model is trained to extract the *Invoice Id* and the *Total Amount* value, and we want to post those to a Microsoft Teams channel. Just add the **Post a message to Teams** action, and then select your fields in the list of tokens  .

    > [!NOTE]
    >
    >- To retreive the value for a field, select **<field_name> value** . For example, for the *INVOICE* field, select **INVOICE value**.
    >- To retrieve the confidence score for a field, select **<field_name> confidence score** . For example, for the *INVOICE* field, select **INVOICE confidence score**.
    
    > [!div class="mx-imgBorder"]
    > ![Form processing flow overview](media/flow-fp-overview-2.png "Form processing flow overview")

Congratulations! You've created a flow that uses an AI Builder form processing model. Select **Save** on the top right, and then select **Test** to try out your flow.

### Related topic
[Form processing model overview](form-processing-model-overview.md)
