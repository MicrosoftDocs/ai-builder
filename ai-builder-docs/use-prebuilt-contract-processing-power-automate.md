---
title: Use the contract processing prebuilt model in Power Automate (preview)
description: Learn how to use the AI Builder contract processing prebuilt model in Power Automate.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 06/27/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the contract processing prebuilt model in Power Automate (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

In this article, you learn how to create a flow that uses the contract processing model.

[!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

1. Sign in to [Power Automate](https://flow.microsoft.com/).
1. On the navigation pane to the left, select **My flows**, and then select **New flow** > **Instant cloud flow** in the command bar at the top.
1. In the **Build an instant flow** screen, do the following:
    1. In the **Flow name** field, enter a name for your flow.
    1. Under **Choose how to trigger this flow**, select **Manually trigger a flow**.
    1. Select **Create**.
1. Select the **Manually trigger a flow** card to open the configuration pane.
1. In the configuration pane, select **+Add an input** > **File** as the input type.
1. In the designer, select **+Insert a new action** (below the **Manually trigger a flow** card) > **AI Builder** > **Extract information from Contract**.
1. Specify **File Content** as the contract document file you want to process in your flow.

    :::image type="content" source="media/use-prebuilt-contract-power-automate/extract-information-from-contract-file-input.png" alt-text="Screenshot of a manually triggered extract information step in a flow, with an contract document selected.":::

Congratulations! You've created a flow that uses the contract processing model. In the command bar, select **Save**, and then select **Test** to try out your flow.

## Test the flow

1. In the command bar, select **Test**.
1. In the **Test Flow** screen, select **Manually**.
1. Select **Test** to trigger the action.
1. In **File Content**, select a contract document file or image, and then select **Import**.
1. Select **Run Flow**.

## Example flow that sends extracted information in data operation

The following example shows how to set up a flow to send the extracted information of the contract document in a Data operation (Compose).

:::image type="content" source="media/use-prebuilt-contract-power-automate/extract-information-from-contract-compose.png" alt-text="Screenshot of a manually triggered extract information step in a flow, with a contract document selected and output the result in a data operation.":::

## Related information

[Contract processing prebuilt model](prebuilt-contract-processing.md)