---
title: Image description prebuilt AI model (preview)
description: Learn how to use the prebuilt image analyzer model in AI Builder to analyze images and generate user-friendly descriptions.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 09/21/2023
ms.author: plarrue
ms.reviewer: angieandrews
ms.custom:
  - bap-template
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/15/2023
---

# Image description prebuilt model (preview)

[!INCLUDE[cc_beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The image description prebuilt model analyzes an image and generates a user-friendly description based on its visual features. The following list describes the image description features.

- **Auto-captioning**: Use machine learning to automatically generate descriptive text for images.
- **Security and surveillance**: Describe the presence, person, or an activity in a video frame, so you can monitor or identify threats easily.
- **SEO (search engine optimization)**: Describe images in a webpage to make the page more discoverable.
- **Chatbots**: Describe a given image and reason for it, which gives the illusion of a multi-modal capability.
- **Retail environment**: Describe a product and helps with inventory management and restocking.

[!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

## Use the image description model

Select the links in this section to learn how to use the image description prebuilt model in Power Apps and Power Automate.

- **Power Apps**: [Use the image description prebuilt model in Power Apps (preview)](image-description-in-powerapps.md)
- **Power Automate**: [Use the image description prebuilt model in Power Automate (preview)](flow-image-description.md)

## Licensing and role requirements

This feature is currently in preview, so using it won't deduct any AI Builder credits.

You need to have the **Basic User** role to consume the image description prebuilt model.

## Supported files

The following list show the format, size, and dimensions of supported files.

- Document formats accepted: .JPG, .JPEG, .PNG, and .BMP
- Maximum document size: 4MB
- The dimensions of the image must be greater than 50 x 50 pixels

## Model output

If a valid image is detected, the model tries to locate and extract the following properties.

|Property  |Note  |
|---------|---------|
|Description*     |    Description of the image    |
|Tags*     |   The list of tags extracted from the image      |
|Confidence score     |    A confidence score represents the accuracy of a prediction as a percentage     |

*Supported language of **Description** and **Tags**: English (United States)
