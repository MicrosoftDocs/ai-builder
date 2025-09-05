---
title: Use the health insurance card processing prebuilt model in Power Automate
description: Learn how to use the AI Builder health insurance card processing prebuilt model in Power Automate.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 09/05/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the health insurance card processing prebuilt model in Power Automate

1. Sign in to [Power Automate](https://make.powerautomate.com/).
1. On the navigation pane to the left, select **My flows**, and then select **New flow** > **Instant cloud flow** in the menu at the top.
1. Name your flow.
1. Under **Choose how to trigger this flow**, select **Manually trigger a flow**.
1. Select **Create**.
1. In the designer, expand the **Manually trigger a flow** card, and then select **+Add an input** > **File** as the input type.
1. Select **+Insert a new action** > **AI Builder** > **Extract information from health insurance card processing**.
1. Specify **File Content** as the contract document file you want to process in your flow.

    :::image type="content" source="media/use-prebuilt-health-insurance-card-power-automate/extract-information-from-health-insurance-card-file-input.png" alt-text="Screenshot of a manually triggered extract information step in a flow, with a health insurance card selected.":::

Congratulations! You created a flow that uses the health insurance card processing model. Select **Save**, and then select **Test** in the upper-right corner to try out your flow.

## Test the flow

1. Select **Test** > **Manually** > **Test** to trigger the action.
1. In **File Content**, select a health insurance card file, and then select **Import**.
1. Select **Run Flow**.