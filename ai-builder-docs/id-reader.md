---
title: Use the ID reader prebuilt model in Power Automate
description: Learn how to use the prebuilt ID reader AI Builder model to extract information from identity documents. 
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 09/12/2022
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Use the ID reader prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. In the left pane, select **My flows**, and then select **New flow** > **Instant cloud flow** in the menu at the top.

1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.

1. Expand **Manually trigger a flow**, and then select **+Add an input** > **File** as the input type.

1. Select **+New step** > **AI Builder** > **Extract information from identity documents**.

1. Specify **File Content** as the identity document file you want to process in your flow.

    :::image type="content" source="media/flow-identity-docs.png" alt-text="Screenshot of a manually triggered extract information step in a flow, with an identity document selected.":::

Congratulations! You've created a flow that uses the ID reader model. Select **Save**, and then select **Test** in the upper-right corner to try out your flow.

## Example flow that adds extracted information to an Excel worksheet

In the following example, you'll add steps to your flow to enter the extracted information in an Excel worksheet. First, you'll prepare a table to use in your flow. The table must match the information you want to extract. Then you'll add an Excel connector to your flow.

### Create an Excel table

1. Create an Excel workbook in a Microsoft OneDrive or SharePoint folder.

1. In the first row of the worksheet, enter the following values, one to a column: **First name**, **Last name**, **Identity document number**, and **Country**. These values are the column headers for your table.

1. Select the cells and format them as a table, with the first row as the header.

    :::image type="content" source="media/excel-table.png" alt-text="Screenshot of part of an Excel table with four columns named First name, Last name, Identity document number, and Country.":::

1. Save and close the workbook.

### Enter the extracted data in the table

1. Use the ID reader flow you created, or create another one for this example.

1. Select **+New step** > **Excel Online (Business)** > **Add a row into a table**.

1. Select a **Location**, **Document Library**, and **File** to specify where to find your Excel workbook.

1. Select the **Table** that you created in the previous step.

1. In **First name**, **Last name**, and **Identity document number**, select the matching value in the dynamic content list.

1. In **Country**, select **Country/Region** in the dynamic content list.

    :::image type="content" source="media/add-row-in-a-table.png" alt-text="Screenshot of a populated Add a row into a table connector in a manually triggered extract information step in a flow.":::

1. Select **Save**.

### Test the flow

1. Select **Test**, select **Manually**, and then select **Test** to trigger the action.

1. In **File Content**, select an identity document file or image, and then select **Import**.

    :::image type="content" source="media/file-content.png" alt-text="Screenshot of the File Content import box.":::

1. Select **Run Flow**.

The flow may take a few seconds to execute while AI Builder extracts the data and adds a new entry to the table in Excel. Open your Excel workbook to confirm the extracted information has been entered.

:::image type="content" source="media/excel-extracted-data-id-reader.png" alt-text="Screenshot of an Excel table with data extracted from an identity document.":::

## Example flow that sends extracted information in an email

The following example shows how to set up a flow to send the extracted information in an email. You can add the **Send an email notification** connector to the flow you created earlier or create an ID reader flow for this example.

:::image type="content" source="media/flow-id-reader-email.png" alt-text="Screenshot of a send email connector in a manually triggered extract information step in a flow.":::

### See also

[ID reader prebuilt model overview](prebuilt-id-reader.md)
