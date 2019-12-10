---
title: Use the language detection prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the AI Builder language detection prebuilt model in your flows
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the language detection prebuilt model in Power Automate

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > Currently, to use AI Builder models in Power Automate, you will need to create the flow inside a solution. More information: [Create a flow in a solution](/flow/create-flow-solution).


1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **My flows** tab, and then select **Create from blank**.
1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.
1. Select **Text** and set as input title: **My Text**.
1. Select **+ New step**, search for the term *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.
1. Select  **LanguageDetection model**, and in the **Request Payload** field, enter *{“text”:”My Text”}*. Add the **My Text** field from the trigger: 

   ![Manually trigger flow screen](media/flow-trigger-flow2.png "Manually trigger flow screen")
   
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
                                      "language": { 
                                          "type": "string" 
                                      }, 
                                      "score": { 
                                          "type": "number" 
                                      } 
                                  }, 
                                  "required": [ 
                                      "language", 
                                      "score" 
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

Now you can iterate through the detected languages returned by the language detection model. In the following example, we add the detected languages to an existing Common Data Service record. 

![Apply to each screen](media/flow-apply-to-each.png "Apply to each screen")

Congratulations! You have created a flow that leverages a language detection model. Select **Save** on the top right and then select **Test** to try out your flow.
