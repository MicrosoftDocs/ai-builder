---
title: AI Builder in SharePoint with document processing overview - AI Builder
description: Provides an overview of how to use your AI models in SharePointwith document processing in Microsoft 365.
author: antrodfr
contributors:
  - FarreltinF
  - antrodfr
  - v-aangie
ms.topic: overview
ms.custom: 
ms.date: 07/22/2026
ms.author: antrod
ms.reviewer: angieandrews
---

# AI Builder in SharePoint with document processing overview

By using document processing in Microsoft 365, you can create AI Builder models in SharePoint. Learn more in [Overview of document processing](/microsoft-365/contentunderstanding/syntex-overview).

From the **Classify and Extract** menu in your SharePoint library, you can apply an existing AI model to a library or create a new one. Two model types are powered by AI Builder:
- **Structured document processing**: Creates AI Builder document processing models for fixed-template documents like invoices, purchase orders, delivery orders, tax documents, and more.
- **Freeform document processing**: Creates AI Builder document processing models for general documents like invoices, purchase orders, delivery orders, and tax documents. It also creates models for contracts, statements of work, letters, and more.

When you apply an AI Builder model to a library, the model processes every document you add to the library. The results display as new library columns.

Learn about requirements and get step-by-step instructions on how to use this service in [Work with models](/microsoft-365/contentunderstanding/model-types-overview).

> [!IMPORTANT]
> - Exporting and importing AI Builder document processing models between environments&mdash;for example, migrating a trained model to another environment through a Dataverse solution import/export&mdash;isn't a supported scenario for the SharePoint/Syntex AI Builder integration. Some AI Builder document processing capabilities for SharePoint are being migrated into Copilot in SharePoint.
> - Learn about document metadata extraction in [Overview of autofill columns](/microsoft-365/documentprocessing/autofill-overview) and [Get started with Copilot in SharePoint (preview)](/sharepoint/copilot-in-sharepoint-get-started).

## Training data storage

If you use AI Builder models, training data is stored in [Microsoft Dataverse](/power-apps/maker/data-platform/data-platform-intro).

Only training data is stored in Dataverse. It's used solely to train the AI Builder model and is never used for any other purpose. Training data is never shared externally.

Dataverse has strong security mechanisms that prevent unauthorized access to user data. Only the following people can access data stored to train your AI Builder model:

- The owner of the model.
- Individuals with Power Platform **System Administrator** and **System Customizer** roles in your organization.

Learn more in [Roles and security in AI Builder](/ai-builder/security).

## Related information

- [AI Builder document processing models](form-processing-model-overview.md)<br/>
- [Feature availability by region](availability-region.md)<br/>
- [Roles and security in AI Builder](security.md)
