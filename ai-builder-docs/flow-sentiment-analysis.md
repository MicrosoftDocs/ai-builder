---
title: Use the sentiment analysis prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the sentiment analysis prebuilt model in your Flows
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the sentiment analysis prebuilt model in Power Automate

## Create a flow that uses the AI Builder sentiment analysis prebuilt model

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/signin), select the **My flows** tab, and then select **Create from blank**.

1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.

1. Select **Text**, and enter **My Text** as the input title.

1. Select **+Add an input** again.

1. Select **Text**, and enter **My Language** as the input title.

1. Select **+ New step**, search for *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.
 >[!NOTE]
 > **Predict Common Data Service (current Environment)** doesn't appear unless you've followed these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Select **SentimentAnalysis model**.<!--Edit okay? -->

1. Specify the **My Language** field from the trigger in the **Language** input, and the **My Text** field in the **Text** input.
   > ![Manually trigger flow screen](media/flow-sentiment-analysis.png "Manually trigger flow screen")

Now you can use the sentiment properties detected by the sentiment analysis model. In the following example, we set the Sentiment property to a new Common Data Service record.

![Update record](media/flow-update-sentiment.png "Update record")

Congratulations! You've created a flow that uses the sentiment analysis model. Select **Save** in the upper-right corner, and then select **Test** to try out your flow.

## Use sentiment analysis to analyze incoming Dynamics 365 emails

Power Automate provides a template that enables you to analyze incoming Dynamics 365 emails by using AI Builder sentiment analysis. This template requires some customization of your Common Data Service email entity before you can use it.

1. Create an attribute in your Email Messages entity in which to save the sentiment analysis results.

   For information about how to create an attribute, see [Create and edit fields for Common Data Service using Power Apps portal](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-field-portal).

1. Sign in to [Power Automate](https://flow.microsoft.com/signin).
1. In the left pane, select **Templates**, and then search for *AI Builder sentiment*.
1. Select **Analyze sentiment of Dynamics emails using AI Builder**.
1. Select your environment, then type **Email Messages** in the **Entity Name** field, and type **Organization** in the **Scope** field.

   > ![Template settings screen](media/sentiment-analysis-template.png "Template settings screen")

1. Next, the template shows messages from **draft emails** and **received emails**. You can filter these if you want to perform sentiment analysis only on selected email statuses. For a list of status codes, see [email EntityType](/dynamics365/customer-engagement/web-api/email?view=dynamics-ce-odata-9).
1. Select **Add sentiment to CDS Email Entity**, select **Show advanced options**, and then locate the attribute you added in step 1.
1. Finally, add **Global sentiment** from the **Dynamic content** list.<!--Can you make this alt text different from the last image?-->

   > ![Template settings screen](media/sentiment-analysis-template2.png "Template settings screen")

If you want this field to be visible in your email grid view, follow these steps:

1. Go to the view/form designer, and add the custom field you created in step 1 of the preceding procedure<!--Is this what "prerequisite step" means?-->. For information about how to add the column to your view, see [Add a column to your view](/dynamics365/customerengagement/on-premises/customize/create-edit-views-app-designer#add-a-column-to-your-view).

1. Then add a field to the form. For details, see [Add a field to a form](/dynamics365/customerengagement/on-premises/customize/add-field-form).
