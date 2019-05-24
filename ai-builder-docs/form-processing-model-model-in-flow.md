---
title: Use form processing model in Microsoft Flow | Microsoft Docs
description: Provides information about how to use a form processing model in Microsoft Flow
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Use form processing model in Microsoft Flow

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Create your flow
1. Sign in to [Microsoft Flow](https://flow.microsoft.com/), select the **My flows** tab, and then select **Create from blank**.
2.	Search for **manually**, select **Manually trigger a flow** in the list of triggers, and then select **+Add an input**.
5.	Select **File** and set **My Document** as input title. 
4.	Select **+ New step**, search for **Predict**, and then select **Predict Common Data Service** in the list of actions.
8.	Select the form processing model you want to use, and specify the following as **Request Payload**:

    -	For a a jpeg image of the form:

        {
            "base64Encoded": "EXPRESSION",
    	    "mimeType": "image/jpeg"
        }

    - 	For a a pdf document of the form:

        {
            "base64Encoded": "EXPRESSION",
    	"mimeType": "application/pdf"
        }

    - In the formula bar on the right, replace **EXPRESSION** with the following expression string:

        (triggerBody()?['file']?['contentBytes']) 

    ![Replace expression screens](media/replace-expression.png "Replace expression screens")

## Test and edit your flow

1.	Select **Test** on the upper right and, select **I’ll perform the trigger action**,  and then select **Save & Test**.
10.	Import a document that can be processed by your trained form processing model, select **Run flow**. 
12.	Copy the results to an editor like Visual Studio Code, and remove all the " \\" characters.
13.	Back on the Flow editor,  select **+ New step**, search for **Parse JSON**, and then select **Parse JSON – Data Operations** from the list of actions.
    ![Parse JSON screens](media/parse-json-forms.png "Parse JSON screens")
15.	In the Parse JSON screen, next to **Content**, select **Response Payload**.
16. Select **Use sample payload to generate schema link**, paste the output from your test, and then select **Done**. 
18.	Copy the generated schema and paste it in an editor like Visual Studio Code, and replace all instanced of **integer** with **number**, and then copy the modified schema back into the Parse JSON screen in Flow. 
    ![Visual Studio  screen](media/visual-studio-replace-integer.png "Visual Studio screen")

    ![Paste schema](media/parse-json-schema.png "Paste schema")

## Use form processing model output in Flow
Now you can use the output of the form processing model in subsequent actions in Flow. 

For example to retreive the value of a field named ‘Total’ you would use the following expression:  

        body('Parse_JSON')?['predictionOutput']?['labels']?['Total']?['value']

To iterate over tables, put the entries value on an 'Apply to each' loop. To access the value of a column named **Amount** for instance inside the table, use the expression: 

        items('Apply_to_each')?['Amount']?['value'] 


 Congratulations! You have created a flow that leverages a form processing AI Builder model. Click **Save** on the top right, and then click **Test** to try out your flow. 



### Related topics
[Form processing model overview](form-processing-model-overview.md)
