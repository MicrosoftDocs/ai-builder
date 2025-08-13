---
title: Generate 'Document (preview)' output for a prompt (preview)
description: Learn how to manage document output.
author: antrodfr
contributors:
  - antrodfr
  - v-aangie
ms.topic: how-to
ms.date: 08/19/2025
ms.update-cycle: 180-days
ms.author: antrod
ms.reviewer: angieandrews
ms.collection: 
  - bap-ai-copilot
---

# Generate 'Document (preview)' output for a prompt (preview)
[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The document output lets you generate a Word document for your prompt response instead of text. The generated document follows a layout that needs to be provided in the document output settings.

Following is an example of possible use cases with document output:

- Generate business documents within automations such as invoices, request for proposals (RFPs), contracts, and more.
- Build reports or write documentation by gathering information from various sources.
- Answer users with a specific document during chat sessions when using an agent.

> [!IMPORTANT]
>- This is a production-ready preview feature.
>- Production-ready previews are subject to [supplemental terms of use](https://go.microsoft.com/fwlink/?linkid=2189520).
>- AI Builder prompts run on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
>- This capability might not be available in your region yet. Learn more in the **Prompts** section in [Feature availability by region or US Government environment](availability-region.md#prompts).
>- This capability might be subject to usage limits or capacity throttling.

## Create a prompt with document output

This section describes how to select document as output and supply a Word document layout. Suppose you want to create an invoice using unstructured information passed to the prompt.

1. As the output, select **Document (preview)** in the top-right corner.
1. To the left of the **Document (preview)** output option, select **Document settings**.
   
    :::image type="content" source="media/generate-document-output-prompt/document-settings.png" alt-text="Screenshot of document settings option.":::

1. Select **select to browse** and upload a Word document layout that contains fields to replace by the prompt.

    Follow these rules:
    - Fields to replace should be identified using double curly brackets. Example: `{{FirstName}}`
    - Fields to replace in a table should identify the table name and the column name, separated with a period. Example: `{{items.quantity}}`
    - Fields to replace shouldn't contain space in the name.
  
    > [!IMPORTANT]
    > Your document layout can't exceed 20MB, can't be confidential, or contain passwords.

    For this scenario, you use the following this invoice document layout:

    :::image type="content" source="media/generate-document-output-prompt/invoice-template.png" alt-text="Screenshot of invoice layout document.":::

1. After uploading the layout, the identified fields to replace display for review.

    :::image type="content" source="media/generate-document-output-prompt/document-settings-fields.png" alt-text="Screenshot of fields to replace.":::

1. Write the instruction that will allow you to generate the adequate text for each field to replace.
1. Select**Test**.

    :::image type="content" source="media/generate-document-output-prompt/prompt-instruction.png" alt-text="Screenshot of prompt instruction for document creation.":::

    The content of the **Text input** could contain all the information about an invoice. 

    Example:  
         Invoice INV-2025-074 – Payment Due by 2025-08-07  
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
         Subtotal: $1,024.00

1. Download the document that appears on the right. All fields should be filled in.

    > [!NOTE]
    > If the fields to replace have meaningful names, the AI model could efficiently generate the correct text for each field to replace with minimal instruction. We recommend that you add specific instructions to correctly fill in each field to replace, especially when:
    > - The name of the field to replace might be ambiguous, like multiple people names.
    > - There's a specific formatting needed, like date format.
    > - Other rules must be applied, like text combinations or calculations.

## Use a prompt with document output in a cloud flow or agent flow

1. Create a new flow and select the trigger action **When a new email arrives (V3)**.
1. Add the action **Run a prompt**, and then select the prompt created in [Create a prompt with document output](#create-a-prompt-with-document-output).
1. Select the body of the email as input of the prompt.

   :::image type="content" source="media/generate-document-output-prompt/prompt-flow.png" alt-text="Screenshot of prompt in a flow.":::

1. Add the action **Create file** from OneDrive.
1. Define the path and file name.
1. From the prompt action in the **File content** field, select **Document Output Content Bytes**.

   :::image type="content" source="media/generate-document-output-prompt/file-creation-flow.png" alt-text="Screenshot of file creation in a flow.":::

You can now send you an email with invoice information and get your file created in your OneDrive folder.

## FAQ

### Why is the document layout analysis failing?

You might encounter the following error after uploading a layout: **Error File analysis failed. Please check if your placeholders are in the correct format of '{{placeholder}}' and try again.**

This error means one of several fields to be replaced doesn't have the right format. All fields to replace should be between `{{` and `}}`.

### Is it possible to generate a document without uploading a layout?

It's not possible to generate a document without uploading a layout.

## Limitations

- Defining a text formatting in the instruction isn't supported. For example, you can't set a field in bold, or add a title or change the color.
- Only generating a Word document is supported.
- A document layout can't be more than 20MB.
- When uploading a document layout of more than 5MB, the prompt needs to be saved and reopened before testing.

## Related information

[FAQ for prompts and text generation capabilities](faqs-text-generation.md)
