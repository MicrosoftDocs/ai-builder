---
title: Create a canvas app to develop a receipt reader that utilizes prompts
description: Learn how to create a canvas app to develop a receipt reader that utilizes prompts.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom:
ms.date: 02/05/2025
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Create a canvas app to develop a receipt reader that utilizes prompts

This sample demonstrates how to use a canvas app to extract information from a receipt with the help of a prompt and a Dataverse table.

## Prerequisites

- Active Power Apps plan
- AI Builder credits
- Dataverse environment

## Import the solution

Before you start the import process, make sure you meet the prerequisites[Prerequisites](#prerequisites).

1. Sign in to [Power Automate](https://make.powerautomate.com/) or [Power Apps](https://make.powerapps.com/).
1. On the left navigation pane, select **Solutions** > **Import Solution**.
1. To import the solution file, select **Browse** > ["Receiptreader_1_0_0_1.zip"](https://go.microsoft.com/fwlink/?linkid=2301859) > **Next** > **Import**.

    It might take a few minutes to import the solution.

## Try it out

Before you begin, make sure you have the following set up:

1. On the left navigation pane, select **Tables**. You should have two (2) tables called **Table receipt** and **World Currencies**.
1. On the left navigation pane, select **... More** > **AI hub** > **Prompts** > **My Prompts**. You should have a prompt called **Receipt reader**.
1. On the left navigation pane, select **Apps** > **My apps**. You should have a canvas app called **Receipt Reader v1**.

You can now run the app to try it out.

1. In the canvas app, select a camera control.
1. Capture an image of a receipt with the front or rear camera.
1. Extract the receipt data as a JSON object with a prompt.
1. Save the output JSON data as a row in a Dataverse table.

    :::image type="content" source="media/use-prompt-to-read-a-receipt/receipt-reader-app.png" alt-text="Screenshot of the receipt reader app.":::

## Related information

- [Use your own data in a prompt](use-your-own-prompt-data.md)
- [Change the output of your prompt](change-prompt-output.md)
- [Add text, image, or document input to a prompt](add-inputs-prompt.md)

