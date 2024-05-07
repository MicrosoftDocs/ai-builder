---
title: Change the output of your prompt
description: Change the output of your prompt.
author: antrod
contributors:
  - antrod
  - v-aangie
ms.topic: conceptual
ms.collection: 
ms.date: 04/22/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Change the output of your prompt

## Benefits of using JSON output
By default, the prompt will generate a text as response. This can be convenient for many uses cases but if the response has several elements that need to be identified individually, the text option can be limited.

The JSON output allows you to generate a JSON structure for your prompt response instead of a text. This allows an easier processing of responses with multiple elements in Power Automate or Power Apps.

Example of use cases that become possible with JSON output
- Display structured content like project schedule or product information.
- Extract data from text like invoices, purchase order, delivery forms and many more.
- Identify object attributes from text sources like emails or Dataverse data.
- Get multiple categories or sentiments from a text.


## Create a prompt with JSON output
### Selecting JSON as output
To change how the prompt response will be rendered, go to the **Output section** in the right panel and select **JSON (preview)** option.

Make sure to click on **Test prompt** to check how your prompt response renders in JSON.

:::image type="content" source="media/change-prompt-output/test-prompt-auto.png" alt-text="JSON option":::

### Edit JSON format

By default the format will be **Auto detected**. That means, each time you test your prompt, the format associated to the prompt will be refreshed with the one detected at testing time. This is convenient when you are iterating on your prompt instructions and want to see how the response format evolves.

:::image type="content" source="media/change-prompt-output/auto-detect.png" alt-text="Auto detect":::

If you update the JSON example, the format becomes **Custom** and will never be updated if you test again your prompt. This is convenient when you don't want any prompt tweaking to influence the format or if you need to follow a very specific format. You can revert to auto detect mode by clicking on the **Back to Auto detect** icon.

:::image type="content" source="media/change-prompt-output/back-auto.png" alt-text="Back to Auto detect":::

To confirm the newly modified example, click on **Apply**. Then, click on **Test prompt** to check how your prompt response renders with the new format.

:::image type="content" source="media/change-prompt-output/custom.png" alt-text="Custom":::

When you've done all your modifications, make sure to click on **Save custom prompt**, otherwise all changes will be lost.

Note that at prompt save time, you are locking the latest **Auto-detected** format or the **Custom** format defined. It means that when you will use your prompt in Power Automate, Power Apps or Copilot topics, the saved format will be used and won't vary.

At any time, you can click on the **</>** icon to check the JSON schema that is generated out of the JSON example. This schema is not modifiable for now.


## Use a prompt with JSON output

### In Power Automate
After adding the **Create text with GPT action** in a Power Automate flow, you can use all the JSON fields as dynamic values, without the need to add a complex logic to parse the response.

In the following example, we'll see how an invoice received by email can be simply processed using the prompt described above.

1- Create a prompt with the trigger **When a new email arrives**. Make sure to set filters if you just need to process specific emails.

2- Extract the text of the attachment(s) using the action **Recognize text in an image or a PDF document**. 

:::image type="content" source="media/change-prompt-output/ocr-json-flow.png" alt-text="Use OCR action":::

3- As the previous action returns a table of lines within a table of page, it will be more convenient to aggregate all the lines in a unique variable. Intialize a variable and append in this variable the **Text** dynamic value from the **Recognize text in an image or a PDF document** action.

:::image type="content" source="media/change-prompt-output/ocr-append-json-flow.png" alt-text="Append OCR text":::

4- Include the **Create text with GPT action**, select your prompt with JSON output, and add the invoice variable you just created in the prompt input.

:::image type="content" source="media/change-prompt-output/gpt-json-flow.png" alt-text="Use GPT action":::

5- Send an email that contains the elements extracted by the prompt with JSON output.

:::image type="content" source="media/change-prompt-output/gpt-output-json-flow.png" alt-text="Use JSON fields":::

As you can see, this allows you to easily and safely use multiple values extracted from a text using a prompt.


### In Power Apps
JSON support in Power Apps will come soon.

### In Copilot topics
To be redacted.

## Limitations
- Using JSON field in Power Apps is not supported for now.
- Modifying a JSON schema is not possible.
- JSON format with nested arrays are not supported for now.
- Defining a JSON format without field keys is not supported. Example: _["abc", "def"]_ is not supported but _["item1": "abc", "item 2": "def"]_ is supported.

