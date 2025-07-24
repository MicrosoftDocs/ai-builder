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

The document output lets you generate a Word document for your prompt response instead of text. The generated document follows a template that needs to be provided in the document output settings.

Following is an example of use cases that become possible with document output:

- Generate business documents within automations such as invoices, RFPs, contracts, and more.
- Build reports or write documentation by gathering information from various sources.
- Answer users with a specific document during chat sessions when using an agent.


## Create a prompt with document output

This section describes how to select document as output and supply a Word document template. 
Let's suppose we want to create an invoice using unstructured information passed to the prompt.

1. Select **Document (preview)** as the output in the top-right corner.
2. Select **Document settings** that appeared left of the **Document (preview)** output option.
   
    :::image type="content" source="media/change-prompt-output/document-settings.png" alt-text="Screenshot of document settings option":::

3. Upload a Word template document that contains fields to replace by the prompt. Follow these rules:
    - Fields to replace should be identified using double curly brackets. _Example: {{FirstName}}_
    - Fields to replace in a table should identify the table name and the column name, separated with a point. _Example: {{items.quantity}}_
    - Fields to replace should not contain any space in the name.

    For our scenario, we will use the following this invoice document template:
    :::image type="content" source="media/change-prompt-output/invoice-template.png" alt-text="Screenshot of invoice template document":::

    You can also download it [here](url).

4. After uploading the template, all the identified fields to replace will be displayed for review.

    :::image type="content" source="media/change-prompt-output/document-settings-fields.png" alt-text="Screenshot of fields to replace":::

5. Let's now write the instruction that will allow to generate the adequate text for each field to replace and click on **Test**.

    :::image type="content" source="media/change-prompt-output/prompt-instruction.png" alt-text="Screenshot of prompt instruction for document creation":::

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

6. Download the document that appears on the right. All fields should be filled-in.

    > [!NOTE]
    > If the fields to replace have meaningful names, the AI model could efficiently generate the right text for each field to replace with minimal. It's recommanded to add specific instruction to correctly fill-in each field to replace, expecially when:
    >  - The name of the field to replace may be ambiguous, like multiple people names.
    >  - There is a specific formatting needed, like date format.
    >  - Additional rules must be applied, like text combinations or calculations.

## Use a prompt with document output in flow or agent flow

This section guides you to create the following cloud flow:

:::image type="content" source="media/change-prompt-output/output-flow.png" alt-text="Screenshot of a cloud flow with a prompt":::

1. Create a new flow and select the trigger action **When a new email arrives (V3)**.
1. Add the action **Run a prompt** and select the prompt created previously. Select the email content as input.
   
   :::image type="content" source="media/change-prompt-output/invoice-prompt.png" alt-text="Screenshot of an invoice processing prompt.":::

1. Update the JSON format by providing the following JSON example:

   :::image type="content" source="media/change-prompt-output/custom-format.png" alt-text="Screenshot of a custom JSON format.":::

1. Create a cloud flow with the **When a new email arrives** trigger. To process specific emails, make sure to set filters.

    Learn more in [Get started with triggers](/power-automate/triggers-introduction?tabs=classic-designer).

1. Add the **Run a prompt** action, and select the prompt you created in the first step.

1. In the **invoice** input, add the email attachment from the trigger action.

   :::image type="content" source="media/change-prompt-output/output-flow-prompt.png" alt-text="Screenshot of prompt parameters in a cloud flow.":::

1. Add the **Send an email** action.
   
1. Edit the email body to include the elements extracted by the prompt with JSON output.

    :::image type="content" source="media/change-prompt-output/gpt-output-json-flow.png" alt-text="Screenshot of an email body showing JSON fields.":::

## FAQ

### A JSON couldn't be generated

You might encounter the following error while testing a prompt: **A JSON could not be generated. Edit your prompt instruction and try again.**

This error might be because the model is enclosing the JSON output with metadata information that prevents successful verification of the required JSON format. To resolve the issue, try adding the following instruction to your prompt: **Don't include JSON markdown in your answer**.

### No JSON is returned in auto-detect mode

It's possible that no JSON is returned after selecting **Test prompt** with the auto-detect mode activated. It might be because the prompt instructions contradict with the system instruction of returning a JSON. It could be solved by changing the prompt instruction and test again.

### JSON format isn't updated at prompt runtime

The latest JSON format detected in auto-detect mode or the latest JSON format defined in custom mode is recorded at prompt save time. This recorded JSON format is applied at prompt runtime, ensuring the  consistency of the response format even when dynamic inputs to the prompt are changing.

## Limitations

- You can't modify a JSON schema.
- We don't support defining a JSON format without field keys.<br/>
    Example: `["abc", "def"]` isn't supported but `[{"Field1": "abc"}, {"Field1": "def"}]` is supported.

## Related information

[Video: AI Builder: JSON outputs in prompt builder](https://www.youtube.com/watch?v=F0fGnWrRY_I)
