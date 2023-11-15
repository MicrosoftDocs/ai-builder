---
title: Image description prebuilt AI model (preview)
description: Learn how to use the AI Builder prebuilt image analyzer model to analyze images and generate user-friendly descriptions in your apps and flows.
author: phil-cmd
ms.author: plarrue
ms.reviewer: angieandrews
contributors:
  - phil-cmd
  - v-aangie
ms.topic: overview
ms.collection: get-started
ms.date: 09/21/2023
ms.custom:
  - bap-template
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/15/2023
---

# Image description prebuilt model (preview)

[!INCLUDE [cc_beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

The image description prebuilt model analyzes an image and generates a user-friendly description based on its analysis. It's useful in a variety of scenarios:

- **Auto-captioning**: Use machine learning to generate descriptive text for images.

- **Security and surveillance**: Monitor or identify threats easily with descriptions of presence, people, or activity in a video frame.

- **Search engine optimization**: Describe the images in a web page to make the page more discoverable in searches.

- **Chatbots**: Describe an image and reason for it, which gives the illusion of a multi-modal capability.<!-- EDITOR'S NOTE: I can't parse this sentence. Can you please clarify what you mean? -->

- **Retail environment**: Describe a product to help with inventory management and restocking.

## Use in Power Apps

[Use the image description prebuilt model in Power Apps (preview)](image-description-in-powerapps).

## Use in Power Automate

[Use the image description prebuilt model in Power Automate (preview)](flow-image-description.md).

## Licensing and role requirements

This feature is in preview. Using it doesn't deduct any AI Builder credits.

You need to have the **Basic User** role to use the image description prebuilt model in your apps and flows.

## Supported files

- Document formats accepted: .JPG, .JPEG, .PNG, and .BMP
- Maximum document size: 4 MB
- The dimensions of the image must be greater than 50 x 50 pixels

## Model output

If a valid image is detected, the model tries to locate and extract the following properties:

- Description: A description of the image in English (en-us)
- Tags: A list of tags in the image in English (en-us)
- Confidence score: A percentage that represents the estimated accuracy of the description
