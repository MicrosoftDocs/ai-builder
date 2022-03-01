---
title: Use the ID reader prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Describes how to use the ID reader prebuilt AI Builder model.
author: paulnog
ms.topic: conceptual
ms.custom: 
ms.date: 06/22/2021
ms.author: paulnog
ms.reviewer: angieandrews
---

# Use the ID reader prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/).
1. In the left pane, select **My flows**, and then select **New flow** > **Instant cloud flow** in the menu at the top.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select the **Create** button.
1. Expand **Manually trigger a flow**, select **+Add an input**, and select **File** as the input type.
1. Select **+New step**, search for **AI Builder** in the **Actions** tab, and then select **Extract information from identity documents**.
1. Specify **File Content** as the Identity document file you want to process in your flow:

    > [!div class="mx-imgBorder"]
    > ![Trigger identity document flow.](media/flow-identity-docs.png "Trigger identity document flow")

Congratulations! You've created a flow that uses the ID reader AI model. Select the **Save** button below the input, and then select **Test**  in the upper-right corner to try out your flow and see information extracted from a file.

## Example ID reader flow

The following example shows how you can set up a flow that sends you an email with extracted information from passports:

> [!div class="mx-imgBorder"]
> ![Trigger identity document email flow.](media/flow-id-reader-email.png "Trigger identity document email flow")

## See also

[ID reader prebuilt model overview](prebuilt-id-reader.md)
