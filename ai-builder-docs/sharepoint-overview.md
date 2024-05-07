---
title: AI Builder in SharePoint with Microsoft Syntex overview - AI Builder
description: Provides an overview of how to use your AI models in SharePoint with Microsoft Syntex.
author: antrodfr
contributors:
  - antrodfr
  - v-aangie
ms.topic: overview
ms.custom: 
ms.date: 04/11/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# AI Builder in SharePoint with Microsoft Syntex overview

With the Microsoft Syntex service, you're able to create AI Builder models in SharePoint. To learn more, go to [Overview of Microsoft Syntex](/microsoft-365/contentunderstanding/syntex-overview).

From the **Classify and Extract** menu in your SharePoint library, you can apply an existing AI model to a library or create a new one. Two model types are powered by AI Builder:
- **Structured document processing:** Creates AI Builder document processing models for fixed-template documents like invoices, purchase orders, delivery orders, tax documents, and more.
- **Freeform document processing:** Creates AI Builder document processing models for general documents like invoices, purchase orders, delivery orders, tax documents, but also contracts, statements of work, letters, and more.

Once an AI Builder model is applied to a library, every document added to the library will be processed by the applied model. The results are displayed as new library columns.

To learn about requirements and get step-by-step instructions on how to use this service, go to [Work with models](/microsoft-365/contentunderstanding/model-types-overview).

## Training data storage

If you're using AI Builder models, training data is stored in [Microsoft Dataverse](/power-apps/maker/data-platform/data-platform-intro).

Only training data is stored in Dataverse. It's used solely to train the AI Builder model and is never used for any other purpose. Training data is never shared externally.

Dataverse has strong security mechanisms that prevent unauthorized access to user data. Data stored to train your AI Builder model is only accessible by:

- The owner of the model.
- Individuals with Power Platform **System Administrator** and **System Customizer** roles in your organization.

To learn more, go to [Roles and security in AI Builder](/ai-builder/security).

### See also

- [AI Builder document processing models](form-processing-model-overview.md)<br/>
- [Feature availability by region](availability-region.md)<br/>
- [Roles and security in AI Builder](security.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
