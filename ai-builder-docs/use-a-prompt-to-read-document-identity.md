---
title: Create a canvas app to develop a document identity reader that utilizes prompts
description: Learn how to create a canvas app to develop a document identity reader that utilizes prompts.
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

# Create a canvas app to develop a document identity reader that utilizes prompts

This sample allows you to explore a canvas app that extracts information from identity documents, such as a U.S. passport or a French identity card, using a prompt and a Dataverse table.

### Prerequisite: 

- Active Power Apps plan
- AI Builder credits
- Dataverse environment

### Import Solution 

Sign in to [Power Automate](https://make.powerautomate.com/). or [Power Apps](https://make.powerapps.com/).

On the left navigation pane, select **Solutions**, select **Import Solution**

Select **Browse** for the solution file to import ["Documentidentityreader_1_0_0_1.zip"](https://go.microsoft.com/fwlink/?linkid=2301870), select **Next**, select **Import**
(it may takes a few minutes to import the solution)

### Try it out

On the left navigation pane, select **Tables**, you should have a table called "Table document identity"

On the left navigation pane, select **... More**, select **AI hub**, select **Prompts**, select **My Prompts**, you should have a prompt called 'Document identity reader'

On the left navigation pane, select **Apps**, select **My apps**, you should have a canvas app called 'Document identity reader v1'


**You can now run the app to try it out.**

- Select a camera control in the canvas app.
- Capture an image of an identity document using the front or rear camera.
- Extract the document's information and output it as a JSON object with a prompt.
- Save the output JSON data as a row in a Dataverse table.


### Helpful links

- https://aka.ms/PromptJsonOutput
- https://aka.ms/MultiModalPrompts

