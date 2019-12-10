---
title: Use the key phrase extraction prebuilt model in Microsoft Flow - AI Builder | Microsoft Docs
description: Provides information about how to set up and use the AI Builder business card reader in model-driven apps 

author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the key phrase extraction prebuilt model in Power Automate

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > Currently, to use AI Builder models in Power Automate, you will need to create the flow inside a solution. More information: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **My flows** tab, and then select **Create from blank**.
1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.
1. Select **Text** and set as input title: **My Text**.
1. Select **+Add an input** again.
1. Select **Text** and set as input title: *My Language*.
1. Select **+ New step**, search for *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.
1. Select **KeyPhraseExtraction model**, and in the **Request Payload** field, enter *{“text”:”My Text”, “language”:”Language_code”}*. Add the **My Text** and **My Language** fields from the trigger.
   > ![Manually trigger flow screen](media/flow-trigger-flow.png "Manually trigger flow screen")

1. Select **+ New step**, search for Parse JSON, and then select **Parse JSON – Data Operations** in the lists of actions.
1. In the **Content** field, select **Response Payload**.
1. Copy the following JSON code and paste it into the **Schema** box: 

    ```JSON
          { 
            "type": "object", 
            "properties": { 
                "predictionOutput": { 
                    "type": "object", 
                    "properties": { 
                        "results": { 
                            "type": "array", 
                            "items": { 
                                "type": "object", 
                                "properties": { 
                                    "phrase": { 
                                        "type": "string" 
                                    } 
                                }, 
                                "required": [ 
                                    "phrase" 
                                ] 
                            } 
                        } 
                    } 
                }, 
                "operationStatus": { 
                    "type": "string" 
                }, 
                "error": {} 
            } 
        } 
    ```

   ![Parse JSON screen](media/flow-parse-json-2.png "Parse JSON screen")

Now you can iterate through the outputs returned by the key phrase extraction model. In the following example, we add each key phrase to a Common Data Service record.

![Add key phrases screen](media/flow-add-phrase.png "Add key phrases in Common Data Service")

Congratulations! You have created a flow that leverages a key phrase extraction model. Select **Save** on the top right and then select **Test** to try out your flow.
