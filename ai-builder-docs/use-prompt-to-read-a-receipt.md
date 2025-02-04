---
title: Create a canvas app to develop a receipt reader that utilizes prompts
description: Learn how to create a canvas app to develop a receipt reader that utilizes prompts.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom:
ms.date: 02/04/2025
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Create a canvas app to develop a receipt reader that utilizes prompts

This sample demonstrates how to use a canvas app to extract information from a receipt with the help of a prompt and a Dataverse table.

:::image type="content" source="media/receipt_reader_app.png" alt-text="Screenshot of the receipt reader app.":::

### Prerequisite: 

- Active Power Apps plan
- AI Builder credits
- Dataverse environment

### Import Solution

Sign in to [Power Automate](https://make.powerautomate.com/). or [Power Apps](https://make.powerapps.com/).

On the left navigation pane, select **Solutions**, select **Import Solution**

Select **Browse** for the solution file to import ["Receiptreader_1_0_0_1.zip"](https://go.microsoft.com/fwlink/?linkid=2301859) , select **Next**, select **Import**
(it may takes a few minutes to import the solution)

### Try it out

On the left navigation pane, select **Tables**, you should have 2 tables called "Table receipt" and "World Currencies"

On the left navigation pane, select **... More**, select **AI hub**, select **Prompts**, select **My Prompts**, you should have a prompt called 'Receipt reader'

On the left navigation pane, select **Apps**, select **My apps**, you should have a canvas app called "Receipt Reader v1"

**You can now run the app to try it out.**

- Select a camera control within the canvas app.
- Capture an image of a receipt using either the front or rear camera.
- Extract the receipt data as a JSON object with a prompt.
- Save the output JSON data as a row in a Dataverse table.

### Helpful links

- https://aka.ms/AIBuilderDataGrounding
- https://aka.ms/PromptJsonOutput
- https://aka.ms/MultiModalPrompts

