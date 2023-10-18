---
title: Use the image description prebuilt model in Power Apps (preview)
description: Learn how to use the image description prebuilt model in Power Apps (preview).
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 09/21/2023
ms.author: plarrue
ms.reviewer: angieandrews
ms.custom: bap-template
---

# Use the image description prebuilt model in Power Apps (preview)

[!INCLUDE[cc_beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

In Power Apps, you can analyze or add your own image. You can also use this prebuilt model in an existing app.

[!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

## Explore image description

1. Sign in to [Power Apps](https://make.powerapps.com).
1. On the left navigation pane, select **More** > **AI models** > **+ New AI model**.
1. Under **AI Models > Explore**, select **Image description**.
1. On the **Generate description of an image** screen, select **+ Upload new**.
1. To see how the model analyzes your image, select predefined image samples.

    Alternatively, you can add your own image by selecting **+ Upload new**. You can also use the prebuilt model in an application, and then select **Use in an app**.

    :::image type="content" source="media/image-description-in-powerapps/use-in-app.png" alt-text="Screenshot of the Generate description of an image Use in app.":::

1. On at the upper-right corner of the screen, select **Play**.

    :::image type="content" source="media/image-description-in-powerapps/select-play-button.png" alt-text="Screenshot of the play button.":::

1. From your local device, select **Tap or click to add a picture**.

    You can analyze the image extracted from the model with a description and a confidence score, as in the following screenshot.

    :::image type="content" source="media/image-description-in-powerapps/image-extracted-from-model.png" alt-text="Screenshot of the image extracted from the model.":::

## Use the formula bar

You can integrate your AI Builder image description models in Power Apps Studio by using the formula bar, as in the following example.

`'Image description'.Predict(UploadedImage1.Image)`

### See also

To learn more, go to [Use AI Builder models in Power Apps](powerfx-in-powerapps.md).

