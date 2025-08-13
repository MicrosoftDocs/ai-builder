---
title: Process responses with JSON output
description: Learn how to create a document prompt, use it in Power Automate, and edit the prompt. 
author: antrodfr
contributors:
  - antrodfr
  - -phil-cmd
  - v-aangie
ms.topic: how-to
ms.date: 08/19/2025
ms.update-cycle: 180-days
ms.author: antrod
ms.reviewer: angieandrews
ms.collection: 
  - bap-ai-copilot
---

# Process responses with JSON output

By default, the prompt generates text as response. Text can be convenient for many uses cases; however, if the response has several elements that need to be identified individually, the text option can be limited.

## Benefits of using JSON output

The JSON output lets you generate a JSON structure for your prompt response instead of text. JSON makes it easier to process responses with multiple elements in agents, cloud flows, or apps.

Following is an example of use cases that become possible with JSON output:

- Display structured content like project schedule or product information.
- Extract data from text like invoices, purchase order, delivery forms, and many more.
- Identify object attributes from text sources like emails or Dataverse data.
- Get multiple categories or sentiments from a text.

## Create a prompt with JSON output

This section describes how to select JSON as output and edit the JSON format.

### Select JSON as output

To change how the prompt response is rendered, select **JSON** as the output in the top-right corner.

:::image type="content" source="media/process-responses-json-output/test-prompt-auto.png" alt-text="Screenshot of selections on the 'Prompt with JSON' page.":::

### Edit JSON format

To view or edit the JSON format, select the settings icon to the left of **Output: JSON**.

:::image type="content" source="media/process-responses-json-output/output-settings.png" alt-text="Screenshot of the output settings.":::

By default, the format is **Auto detected**. This format means each time you test your prompt, the format associated to the prompt is refreshed with the one detected at testing time. This format is convenient when you're iterating on your prompt instructions and want to know how the response format evolves.

:::image type="content" source="media/process-responses-json-output/auto-detect.png" alt-text="Screenshot of the 'Auto-detected format'.":::

If you update the JSON example, the format becomes **Custom** and is never updated if you test your prompt again. This format is convenient when you don't want prompt tweaking to influence the format, or if you need to follow a specific format.

You can revert to auto-detect mode by selecting the **Back to auto-detect** icon.

:::image type="content" source="media/process-responses-json-output/back-auto.png" alt-text="Screenshot of the 'Back to auto-detected' icon.":::

To test and save your prompt, follow these steps:

1. To confirm the newly modified example, select **Apply**.
1. To check how your prompt response renders with the new format, select **Test**.
1. When you finish your modifications, select **Save custom**. If you skip this step, your changes are lost.

When you save your prompt, you're locking the latest **Auto-detected** format or the **Custom** format defined. This means when you use your prompt in an agent, a cloud flow, or an app, the saved format is used&mdash;it doesn't vary.

At any time, you can check the JSON schema that generates out of the JSON examples by selecting **</>**. You can't modify this schema currently.

## Use a prompt with JSON output in Power Automate

This section guides you to create the following cloud flow:

:::image type="content" source="media/process-responses-json-output/output-flow.png" alt-text="Screenshot of a cloud flow with a prompt":::

1. Create a prompt to process invoices using an **Image or document** as input.

   Learn more in [Add text, image, or document input to a prompt](/ai-builder/add-inputs-prompt).

   :::image type="content" source="media/process-responses-json-output/invoice-prompt.png" alt-text="Screenshot of an invoice processing prompt.":::

1. Update the JSON format by providing the following JSON example:

   :::image type="content" source="media/process-responses-json-output/custom-format.png" alt-text="Screenshot of a custom JSON format.":::

1. Create a cloud flow with the **When a new email arrives** trigger. To process specific emails, make sure to set filters.

    Learn more in [Get started with triggers](/power-automate/triggers-introduction?tabs=classic-designer).

1. Add the **Run a prompt** action, and select the prompt you created in the first step.

1. In the **invoice** input, add the email attachment from the trigger action.

   :::image type="content" source="media/process-responses-json-output/output-flow-prompt.png" alt-text="Screenshot of prompt parameters in a cloud flow.":::

1. Add the **Send an email** action.
   
1. Edit the email body to include the elements extracted by the prompt with JSON output.

    :::image type="content" source="media/process-responses-json-output/gpt-output-json-flow.png" alt-text="Screenshot of an email body showing JSON fields.":::

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
