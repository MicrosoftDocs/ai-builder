---
title: Use predict action in Power Automate - AI Builder
description: Learn how to use the predict action in Power Automate.
author: chplanty
contributors:
  - chplanty
  - Antonio-Rodrigues
  - v-aangie
ms.topic: conceptual
ms.date: 10/24/2024
ms.author: chplanty
ms.reviewer: angieandrews
---

# Use predict action in Power Automate

You can use dedicated actions for each AI Builder model in Power Automate. However, the **predict** action lets you use many AI Builder model types.

## Use a custom or prebuilt model

1. Sign in to [Power Automate](https://make.powerautomate.com/).

1. On the navigation pane to the left, select **My flows**, and then select **New flow** > **Instant cloud flow**.

1. Name your flow.

1. Under **Choose how to trigger this flow**, select **Manually trigger a flow**, and then select **Create**.

1. Select **+New step**, and then enter **predict** in the search bar.

1. Select **Predict from AI Builder** or **Predict using AI Builder models from Microsoft Dataverse**. Both actions offer the same features.

    :::image type="content" source="media/predict-action.png" alt-text="Screenshot of the Predict action.":::

1. In the **Model** input, select a custom model you created or choose a prebuilt model.

> [!NOTE]
> Learn more about the input and output parameters of each model in the following sections in [AI Builder in Power Automate overview](use-in-flow-overview.md):
>- [Custom AI models that you build and train](use-in-flow-overview.md#custom-ai-models-that-you-build-and-train)
>- [Prebuilt AI models you can use in Power Automate right away](use-in-flow-overview.md#custom-ai-models-that-you-build-and-train)

## Use a dynamic model ID (advanced)

For some complex use cases, you might need to pass a model ID dynamically to the predict action. For example, if you want to process different types of invoices using different models, you might want to automatically choose a model depending on the type of invoice.

In this section, you learn how to configure the AI Builder predict action for this specific purpose depending on the model type.

1. Sign in to [Power Automate](https://make.powerautomate.com/).

1. Select **My flows** in the left pane, and then select **New flow** > **Instant cloud flow**.

1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.

1. Select **+ New step**.

1. Enter **Initialize variable** in the search bar, and then select it in the **Actions** tab.

1. Enter **model id** in the **Name** input, **String** in the **Type** input, and the actual model ID in the **Value** input.

   You can find the model ID in the URL of the model's detail page in Power Apps:
   *make.powerapps.com/environment/[environment id]/aibuilder/models/**[model id]***

1. Select **+ New step**, search for **predict** and then select **Predict from AI Builder**.

1. Select the input > **Enter custom value**, and then enter **model id** from step 6.

   The **Infer request** column value depends on the model type.

### Document processing model

1. In the step **Manually trigger a flow**, add a **File** input, and set its name to **File Content**.
1. In the step **Manually trigger a flow**, add a **Text** input, and set its name to **Mime Type**.
1. In the step **Initialize variable**, enter a document processing model ID.
1. In the step **Predict**, enter following value in the **Infer request** column:

    ```json
    {
        "version": "2.0",
        "requestv2": {
        "@@odata.type": "Microsoft.Dynamics.CRM.expando",
        "mimeType": "@{triggerBody()['text']}",
        "base64Encoded": "@{string(triggerBody()?['file']?['contentBytes'])}",
        "pages": "@{base64('1-2')}"
        }
    }
    ```

    **pages** parameter is optional, and can be in the form '2' or as a range like '1-10'.

    :::image type="content" source="media/DynModelId-1.png" alt-text="Screenshot of the Predict action with dynamic model ID.":::

1. Select **Save** in the upper-right corner, and then select **Test** to try out your flow:

    :::image type="content" source="media/DynModelId-2.png" alt-text="Screenshot of testing the predict action.":::

1. In the flow run details, get the model JSON output in the **OUTPUTS** section of the predict action. This output is useful to build downstream actions using values of the model.

     :::image type="content" source="media/DynModelId-3.png" alt-text="Screenshot of getting output from run results.":::

1. Go back to your flow in edit mode.

1. Select  **+ New step** and select the **Compose** action (or any other action to process your model output). Let's say your model output has the **Total** column. You can get it with the following formula:

    ```
    @{outputs('Predict')?['body/responsev2/predictionOutput/labels/Total/value']}
    ```

    :::image type="content" source="media/DynModelId-4.png" alt-text="Screenshot of using the predict output.":::

### Object detection model

This process is similar to the infer request in step 4 in the [Document processing model](#document-processing-model) section:

```json
{
    "version": "2.0",
    "requestv2": {
        "@@odata.type": "Microsoft.Dynamics.CRM.expando",
        "base64Encoded": "@{string(triggerBody()?['file']?['contentBytes'])}"
    }
}
```

### Category classification model

This process is similar to the infer request in step 4 in the [Document processing model](#document-processing-model) section:

```json
{
    "version": "2.0",
    "requestv2": {
        "@@odata.type": "Microsoft.Dynamics.CRM.expando",
        "language": "Detect automatically",
        "text": "The text to categorize"
    }
}
```

[!INCLUDE[footer-include](includes/footer-banner.md)]
