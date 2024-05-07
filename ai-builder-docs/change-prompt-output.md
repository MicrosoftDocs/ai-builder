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

See [more details](change-prompt-output.md#use-cases) on the uses cases below in this documentation.

## Create a prompt with JSON output
### Selecting JSON as output
To change how the prompt response will be rendered, go to the **Output section** in the right panel and select **JSON (preview)** option.

Make sure to clik on **Test prompt** to check how your response renders in JSON.

:::image type="content" source="media/change-prompt-output/test-prompt-auto.png" alt-text="JSON option":::

### Edit JSON format

By default the format will be **Auto detected**. That means, each time you test your prompt, the format associated to the prompt will be refreshed with the one detected at testing time. This is convenient when you are iterating on your prompt instructions and want to see how the response format evolves.

:::image type="content" source="media/change-prompt-output/auto-detect.png" alt-text="Auto detect":::

If you update the example, the format becomes **Custom** and will never be updated if you test again your prompt. This is convenient when you don't want any prompt tweaking to influence the format or if you need to follow a very specific format.

:::image type="content" source="media/change-prompt-output/custom.png" alt-text="Custom":::

Note that at prompt save time, you are locking the latest **Auto-detected** format or the **Custom** format defined. It means that when you will use your prompt in Power Automate, Power Apps or Copilot topics, the saved format will be used and won't vary.

## Use a prompt with JSON output
### In Power Automate

### In Power Apps


## Use cases
In this section, some uses cases are described to demonstrate how it can be powerful to use JSON output.
