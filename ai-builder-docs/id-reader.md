---
title: Use the ID reader prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: This topic describes how to use the ID reader prebuilt AI Builder model.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 08/25/2022
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Use the ID reader prebuilt model in Power Automate

You can use the identity document (ID) reader prebuilt model to extract information from passports and US driver licenses. The model will extract information such as the person’s first name, date of birth, or gender.

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. In the left pane, select **My flows**, and then select **New flow** > **Instant cloud flow** in the menu at the top.


1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select the **Create** button.

1. Expand **Manually trigger a flow**, select **+Add an input**, and select **File** as the input type.

1. Select **+New step**, search for **AI Builder** in the **Actions** tab, and then select **Extract information from identity documents**.

1. Specify **File Content** as the identity document file you want to process in your flow.

    > [!div class="mx-imgBorder"]
    > ![Trigger identity document flow.](media/flow-identity-docs.png "Trigger identity document flow")

Congratulations! You've created a flow that uses the ID reader AI model. Select the **Save** button below the input, and then select **Test**  in the upper-right corner to try out your flow and see information extracted from a file.

## Example flow that uses the 'Send an email notification' connector

The following example shows how you can set up a flow that sends you an email with extracted information from passports.

> [!div class="mx-imgBorder"]
> ![Screenshot of the trigger identity document email flow.](media/flow-id-reader-email.png "Trigger identity document email flow")

## Example flow that uses the Microsoft Excel Online connector

You can set up a flow that add lines to an Excel spreadsheet with extracted information from an identity document. Before you begin entering your data into Excel, make sure that you've created a table that matches the information that you want to store.

### Create an Excel table

Prepare a table to use in your flow.

1. Create a new Excel spreadsheet in a Microsoft OneDrive or SharePoint folder.

1. In the first row, enter the following values in their own cells: **First Name**, **Last Name**, **Identity document number**, and **Country**. These values will serve as the column headers for your table.

1. Select the cells that you entered, format them as a table, and then mark the first row as the header.

     > [!div class="mx-imgBorder"]
     > ![Screenshot of the trigger identity document Excel table flow.](media/excel-table.png "Trigger identity document Excel table flow")

### Write the data to Excel

Now that your table is set up, you can add the extracted identity document information to the Excel spreadsheet.

1. Select **+New step**.

1. Search for the **Excel Online (Business)** connector or select it from the list of connectors.

1. Select the **Add a row into a table** action.

1. In the **Location**, **Document Library**, and **File** fields, specify the location in OneDrive or SharePoint where your file is stored.

1. In the **Table** field, select the table that you created.

1. In the **First name** field, select **First name** in the dynamic content list.

1. In the **Last name** field, select **Last name** in the dynamic content list.

1. In the **Identity document number** field, select **Identity document number** in the dynamic content list.

1. In the **Country** field, select **Country/Region** in the dynamic content list.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the trigger identity document add row in a table flow.](media/add-row-in-a-table.png "Trigger identity document add row in a table flow")

### Test the flow

You're done building the flow. Now you can test it.

1. Select the **Save** button on the top right.

1. Select the **Test** button next the **Save** button.

1. Select **Manually**, and then select **Test** to trigger the action.

1. Select an identity document file or image where your file is stored in the **File Content** field, and then select **Import**.

    > [!div class="mx-imgBorder"]
    > ![Trigger identity document file content flow.](media/file-content.png "Trigger identity document file content flow")

1. Select **Run Flow**.

The flow will execute after some seconds: AI Builder will extract the data and a new entry will be added to Excel with the extracted information.

> [!div class="mx-imgBorder"]
> ![Screenshot of the trigger identity document Excel extracted data flow.](media/excel-extracted-data-id-reader.png "Trigger identity document Excel extracted data flow")

### See also

[ID reader prebuilt model overview](prebuilt-id-reader.md)
