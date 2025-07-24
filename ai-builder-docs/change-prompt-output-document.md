---
title: Document output
description: Learn how to manage document output.
author: antrodfr
contributors:
  - antrodfr
  - v-aangie
ms.topic: how-to
ms.date: 07/23/2025
ms.update-cycle: 180-days
ms.author: antrod
ms.reviewer: angieandrews
ms.collection: 
  - bap-ai-copilot
---

# Document output for prompts

The document output lets you generate a Word document for your prompt response instead of text. The generated document follows a layout that needs to be provided in the document output settings.

Following is an example of use cases that become possible with document output:

- Generate business documents within automations such as invoices, RFPs, contracts, and more.
- Build reports or write documentation by gathering information from various sources.
- Answer users with a specific document during chat sessions when using an agent.


## Create a prompt with document output

This section describes how to select document as output and supply a Word document layout. 
Let's suppose we want to create an invoice using unstructured information passed to the prompt.

1. Select **Document (preview)** as the output in the top-right corner.
2. Select **Document settings** that appeared left of the **Document (preview)** output option.
   
    :::image type="content" source="media/change-prompt-output/document-settings.png" alt-text="Screenshot of document settings option.":::

3. Click on **select to browse** and upload a Word document layout that contains fields to replace by the prompt. Follow these rules:
    - Fields to replace should be identified using double curly brackets. _Example: {{FirstName}}_
    - Fields to replace in a table should identify the table name and the column name, separated with a point. _Example: {{items.quantity}}_
    - Fields to replace should not contain any space in the name.
  
    > [!IMPORTANT]
    > Your document layout can't exceed 25Mb and can't be confidential or contain passwords.

    For our scenario, we will use the following this invoice document layout:
    :::image type="content" source="media/change-prompt-output/invoice-template.png" alt-text="Screenshot of invoice layout document.":::


4. After uploading the layout, all the identified fields to replace will be displayed for review.

    :::image type="content" source="media/change-prompt-output/document-settings-fields.png" alt-text="Screenshot of fields to replace.":::

5. Let's now write the instruction that will allow to generate the adequate text for each field to replace and click on **Test**.

    :::image type="content" source="media/change-prompt-output/prompt-instruction.png" alt-text="Screenshot of prompt instruction for document creation.":::

    The content of the **Text input** could contain all the information about an Invoice. Example:  
         _Invoice INV-2025-074 – Payment Due by 2025-08-07  
         Please find below the details of your invoice:  
         Invoice Date: 2025-07-24  
         Invoice Number: INV-2025-074  
         Customer ID: CUST-45892  
         Billed To: Adatum  
         Billing Address: 145 Greenfield Avenue, Suite 12, Springfield, IL 62704  
         Due Date: 2025-08-07  
         Products/Services Provided:  
         - Office Chair ErgoComfort X1 – Qty: 2 – Unit Price: $189.00  
         - Standing Desk ProLift 120 – Qty: 1 – Unit Price: $499.00  
         - LED Desk Lamp BrightLite – Qty: 3 – Unit Price: $49.00  
         Subtotal: $1,024.00_

7. Download the document that appears on the right. All fields should be filled-in.

    > [!NOTE]
    > If the fields to replace have meaningful names, the AI model could efficiently generate the right text for each field to replace with minimal instruction. It's however recommanded to add specific instruction to correctly fill-in each field to replace, expecially when:
    >  - The name of the field to replace may be ambiguous, like multiple people names.
    >  - There is a specific formatting needed, like date format.
    >  - Additional rules must be applied, like text combinations or calculations.

## Use a prompt with document output in flow or agent flow

1. Create a new flow and select the trigger action **When a new email arrives (V3)**.
1. Add the action **Run a prompt** and select the prompt created previously. Select the body of the email as input of the prompt.
   
   :::image type="content" source="media/change-prompt-output/prompt-flow.png" alt-text="Screenshot of prompt in a flow.":::

1. Add the action **Create file** from OneDrive. Define the path and file name, and select **Document Output Content Bytes** from the prompt action in the **File content** field.

   :::image type="content" source="media/change-prompt-output/file-creation-flow.png" alt-text="Screenshot of file creation in a flow.":::

You can now send you an email with invoice information and see get your file created in your OneDrive folder.

## FAQ

### Why is the document layout analysis failing?

You might encounter the following error after uploading a layout: **Error File analysis failed. Please check if your placeholders are in the correct format of '{{placeholder}}' and try again.**

This error means one of several fields to replaced don't have the right format. All fields to replace should be between {{ and }}.

### Is it possible to generate a document without uploading a layout?

It's not possible to generate a document without uploading a layout.


## Limitations

- Defining a text formatting in the instruction is not supported. For example: set a field in bold, add a title or change the color.
- Only generating a Word document is supported for now.
- When uploading a document of more than 5Mb, the prompts needs to be saved before testing.


