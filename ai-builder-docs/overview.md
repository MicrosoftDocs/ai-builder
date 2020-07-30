---
title: What is AI Builder? - AI Builder | Microsoft Docs
description: Provides an overview of AI Builder and high-level steps to add intelligence to your apps
author: Dean-Haas

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: cdbellar; mfotedar
ms.reviewer: v-dehaas
---

# What is AI Builder?

AI Builder is a Microsoft Power Platform capability you can use to improve business performance by automating processes and predicting outcomes. AI Builder is a turnkey solution that brings the power of AI through a point-and-click experience. With AI Builder, you can add intelligence to your apps even if you have no coding or data science skills.

 > [!IMPORTANT]
 >
 > - Some features in AI Builder haven't been released yet for general availability (GA) and remain in preview status. See [Release status](#release-status) later in this topic for more information.
 > - [!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]
 > - Administrators can control preview feature availability for their environment by using the Power Platform admin center. More information: [Enable or disable AI Builder preview features](administer.md#enable-or-disable-ai-builder-preview-features)

To explore AI Builder, sign in to [Power Apps](https://make.powerapps.com), and then select **AI Builder** > **Build**.

> [!div class="mx-imgBorder"]
> ![AI Builder home page](media/ai-builder-home.png "AI Builder home page")

## Release status

AI Builder was released for public preview on June 10, 2019, in Europe and the United States. The GA release will occur in a phased manner, with some features remaining in preview status while others are released for GA.

Because of technical dependencies, features will be released differently in various locations. For a breakdown of the release status of AI Builder features and model types for your region, see [Feature availability by region](availability-region.md).

For information about license capacity, pricing, and restrictions, see [Find the right Power Apps plan for your business needs](https://powerapps.microsoft.com/pricing/).

## How can I add intelligence to my apps?

Using AI is easy thanks to integration with Power Apps and Power Automate<!--note from editor: Because "Microsoft" occurs on every page in docs, we count that as the first occurrence. The one exception is Teams, which our branding guidelines say should be "Microsoft Teams" at the first occurrence, and then just "Teams" after that. And of course some things always need "Microsoft," such as "Microsoft Power Platform." -->. Adding intelligence to your business is simple:

1. **Choose an AI model type**: Use the model type that suits your business need. Choose from a growing set of AI solutions.
1. **Connect data**: Select your business-specific data from Common Data Service. AI Builder does the hard work for you, thanks to Common Data Model<!--New guidance: No "the" for Common Data Model in addition to Common Data Service. -->.
1. **Tailor your AI model**: Filter your data, set scheduling, and tweak the AI model to optimize how your AI performs.
1. **Train your AI model**: Training is an automatic process, where AI Builder "teaches" your AI model how to resolve your business problem (for example, how to recognize your products on an image) thanks to your business data and tailoring. When trained, your AI model can generate insights such as the result of a prediction, or the list and number of objects detected in an image.
1. **Use insights from your AI model**: Use the results from your AI model across Microsoft Power Platform to create solutions that meet your business needs, even if you have no coding skills. For example, you can create a flow that automates document processing in Power Automate or an app in Power Apps that predicts whether a supplier will be out of compliance.

### Next step

[Learn about AI model types](model-types.md)

### See also
<!--note from editor: The majority of Power Platform topics seem to use "See also," so I've used that here rather than "Related content" or "Related topics." The advantage is that sometimes the links don't go to content but to community forums, so "See also" covers everything.-->
[AI Builder release plan](/power-platform-release-plan/2019wave2/ai-builder/planned-features)  
[Power Apps docs](https://docs.microsoft.com/powerapps/)  
[Power Automate docs](https://docs.microsoft.com/flow/getting-started)
