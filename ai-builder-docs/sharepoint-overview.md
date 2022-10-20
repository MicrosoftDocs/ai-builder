---
title: AI Builder in SharePoint overview - AI Builder | Microsoft Docs
description: Provides an overview of how to use your AI models in SharePoint.
author: v-aangie
ms.topic: overview
ms.custom: 
ms.date: 05/31/2022
ms.author: angieandrews
ms.reviewer: angieandrews
---

# AI Builder in SharePoint (Syntex)

## Overview
With the Syntex offering, you are able to create AI Builder models from within SharePoint. [Learn more about Syntex](/microsoft-365/contentunderstanding/syntex-overview).

From the **Classify and Extract** menu in your SharePoint library, you can apply an existing AI model to a library or create a new one. Two model types are powered by AI Builder:
- **Freeform document processing** which creates AI Builder document processing models for unstructured or free form documents (contracts, statement of work, letters, etc.)
- **Structured document processing** which creates AI Builder document processing models for structured documents (Invoices, purchase orders, delivery orders, tax documents, etc.)

Once an AI Builder model is applied to a library, every document added to the library will be processed by the applied model and results displayed as new library columns.

For information about requirements and step-by-step instructions to use this feature, see [Work with models](/microsoft-365/contentunderstanding/model-types-overview) in the SharePoint documentation.

## Training data storage
If you are using AI Builder models, training data is stored in [Microsoft Dataverse](/power-apps/maker/data-platform/data-platform-intro). 

Only training data is stored in Microsoft Dataverse, it is solely used to train the AI Builder model and is never used for any other purpose. Training data is never shared externally.

Microsoft Dataverse has strong security mechanisms that prevent unauthorized access to user data. Data stored to train your AI Builder model is only accessible by:
- The owner of the model
- The Power Platform System Administrators and System Customizers of your organization


Learn more with [Roles and Security in AI Builder](/ai-builder/security)


### See also

[AI Builder document processing models](form-processing-model-overview.md)

[Feature availability by region](availability-region.md)

[Roles and Security in AI Builder](/ai-builder/security)

[!INCLUDE[footer-include](includes/footer-banner.md)]
