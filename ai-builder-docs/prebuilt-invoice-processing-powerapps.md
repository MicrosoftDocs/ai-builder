---
title: Use invoice processing in Power Apps -  AI Builder | Microsoft Docs
description: Provides information about how to use AI Builder invoice processing in Power Apps.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 12/01/2020
ms.author: jofernan
ms.reviewer: kvivek
---

# Use invoice processing in Power Apps (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Currently, there is no invoice processing control available for canvas apps in Power Apps. But you can create an app that calls a Power Automate flow that uses the invoice processing prebuilt AI model, and then return the results back to your app. The following example shows how to do this:

## Build your flow

1. Sign in to [Power Automate](https://flow.microsoft.com).
1. Make sure you are in the same Power Platform environment where you will have your canvas app. Check the environment on the top right of the page. Next select **My flows** in the left-side navigation pane.
1. Select **New** > **Instant – from blank**.
1. Name your flow: “Invoice processing flow”, then select **Power Apps** under **Choose how to trigger this flow**.
1. Select **Create**.
1. Select **+ New step**, search for AI Builder, and then select **Process and save information from invoices** in the list of actions.
1. Select the **Invoice file** input and then select **Ask in Power Apps** in the **Dynamic content** menu.
   > [!div class="mx-imgBorder"]
   > ![Process and save information](media/flow-process-and-save.png "Choose dynamic content")

1. Select **+ New step**, search for *respond to a powerapp*, and then select **Respond to a PowerApp or flow** in the list of actions.
1. Select **+Add an output** and for this example we’re going to add two Text outputs: *Invoice ID* and *Invoice Total*. You might want to add more or different outputs based on the extracted invoice fields you want to send back to your canvas app.
   > [!div class="mx-imgBorder"]
   > ![Respond to a Power App tile](media/flow-respond-to-power-app.png "Configure the 'Respond to Power App' screen")

1. Select the **Enter a value to respond** field next to each defined output and then select from the dynamic content menu: **Invoice ID** and **Invoice Total (text)**.
1. Save your flow. 

## Build your canvas app

1. Sign in to [Power Apps](https://make.powerapps.com/). 
1. Make sure you are on the same Microsoft Power Platform environment where you created the flow on the top right of the page. 
1. Select **+Create** in the left-side navigation pane.
1. Select the **Canvas app from blank** tile. Give a name to your app and select either **Tablet** or **Phone** format.
1. In the app editor, select **Insert** > **Media** > **Add picture** to insert a control intro your app where users can upload a picture from a device or  camera.
1. Select the **AddMediaButton1** control on the left.  Then on the formula bar on the top, select the **OnSelect** event. 


1. Select the **Action** menu and select **Power Automate**. Choose the flow that we created in the previous steps. If you don’t see the flow, make sure you are on the same Power Platform environment as where you created the flow, you can check the environment on the top right of the page.
   > [!div class="mx-imgBorder"]
   > ![Action menu](media/canvas-app-action-menu.png "Select the 'Action' menu")

1. Enter the following formula on the **OnSelect** event for the **AddMediaButton1** control. This formula tells the app to call the flow we’ve built once a new image is uploaded and saves the results we received from the flow in variables.

   The name of the variables and name of your flow might be different depending on how you configured it when building the flow:

   > *Set(FlowResults, Invoiceprocessingflow.Run(AddMediaButton1.Media));*
   >
   > *Set(InvoiceId, FlowResults.invoice_id);*
   >
   > *Set(InvoiceTotal, FlowResults.invoice_total);*

   > [!div class="mx-imgBorder"]
   > ![Formula menu](media/canvas-app-formula.png "Enter the formula")

1. Now let’s add two labels and two text inputs to display the results we will get from the flow. Change the Default property for each text input to take the values from the variables we have defined in the previous step.
   > [!div class="mx-imgBorder"]
   > ![Add labels and text inputs](media/canvas-app-add-labels.png "Add two labels and two text inputs")

1. The app is now ready to run! Select the **Play** icon on the top right to test it.
   > [!div class="mx-imgBorder"]
   > ![Finished app](media/canvas-app-done.png "Finished app screen")


[!INCLUDE[footer-include](includes/footer-banner.md)]