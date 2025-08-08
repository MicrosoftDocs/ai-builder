---
title: Use the health insurance card processing prebuilt model in Power Automate
description: Learn how to use the AI Builder health insurance card processing prebuilt model in Power Automate.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 08/08/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the health insurance card processing prebuilt model in Power Automate

- Sign in to [Power Automate](https://make.powerautomate.com/).

- In the left pane, select My flows, and then select New flow > Instant cloud flow in the menu at the top.

- Name your flow, select Manually trigger a flow under Choose how to trigger this flow, and then select Create.

- Expand Manually trigger a flow, and then select +Add an input > File as the input type.

- Select + Insert a new action > AI Builder > Extract information from health insurance card processing.

- Specify File Content as the contract document file you want to process in your flow.

    :::image type="content" source="media/use-prebuilt-health-insurance-card-pauto/extract-information-from-health-insurance-card-file-input.png" alt-text="Screenshot of a manually triggered extract information step in a flow, with a health insurance card selected.":::

Congratulations! You've created a flow that uses the health insurance card processing model. Select Save, and then select Test in the upper-right corner to try out your flow.

## Test the flow

- Select Test, select Manually, and then select Test to trigger the action.

- In File Content, select a health insurance card file, and then select Import.

- Select Run Flow.