---
title: Export image classification model by Lobe to AI Builder (preview) - AI Builder | Microsoft Docs
description: Learn how to export your image classification model from Lobe into AI Builder for use in Power Apps and Power Automate.
author: mbeissinger
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/15/2021
ms.author: mabeis
contributors:
    - JakeCohenMicrosoft
    - v-aangie
---
# Export your image classification model from Lobe to AI Builder (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Lobe is integrated with Microsoft Power Platform, which adds the ability to export your model to AI Builder for use in Power Apps and Power Automate.

> [!IMPORTANT]
> - This is a preview feature.
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
> - This feature is being gradually rolled out across regions and might not be available yet in your region.

## Export a model to Microsoft Power Platform

1. In Lobe, select **Use** > **Export** > **Power Platform**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Lobe Export screen.](media/lobe-export/lobe-export.png "Lobe Export screen")

1. Sign in with the credentials you use to sign in to your Microsoft Power Platform environment.

1. Name your model, and choose the environment where you'll use the model.

1. Select **Export**.

> [!NOTE]
> If you have access to multiple environments, make sure you're in the correct environment for your model to be exported.

### For application lifecycle management (ALM) users

[ALM](/power-platform/alm/overview-alm) users can [create a solution from the model in AI Builder](byom-alm.md) to transfer it between environments. As an alternative, you can re-export the model to your environment of choice after validation in your app or flow.

## View your Lobe models in AI Builder

After you've exported your image classification model from Lobe, it will appear in your list of models in AI Builder. Models that were exported from Lobe are listed in the **Model** column as **Image Classification**.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://flow.microsoft.com/).

1. To view a list of models, select **AI Builder** > **Models** on the left pane.

1. To see project details, select the model in order to access a summary of images with their test results and a breakdown of labels. This information can help you decide whether to test your app or to publish it.

## Next step

After you've exported an image classification model to your Microsoft Power Platform environment, you can use it in Power Apps or Power Automate.

- [Use an image classification model by Lobe in Power Apps](image-classification-component-in-powerapps.md)
- [Use an image classification model by Lobe in Power Automate](image-classification-model-in-flow.md)
