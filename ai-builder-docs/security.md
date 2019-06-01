---
title: Security in AI Builder -  AI Builder | Microsoft Docs
description: Describes security information related to roles, privileges, and access in AI Builder and the services it connects to. 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Security in AI Builder

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

AI Builder relies on environment security and Common Data Service security roles and privileges to grant access to AI features in PowerApps. For more information, see [Security overview](/power-platform/admin/wp-security) topic.

Some privileges are set by default in Common Data Service, allowing built-in security roles to take advantage of AI Builder without further actions from System Administrators.

- Environment Makers can use AI Builder to create AI models. 
- Common Data Service users can inference data using the models embedded in PowerApps. 
- Administrators and System Customizers can access all AI models created in the environment. 

These security roles have already set the right privileges to the AI Builder entities from Common Data Service. Custom security roles will be able to create AI models as long as they have the same privileges to the AI Builder entities as the Environment Maker role.

> [!div class="mx-imgBorder"]
> ![Security roles screen](media/security-roles-screen.png "Security roles screen" )

Scenarios such as object detection, text classification and binary classification require read access to entities from Common Data Service. Make sure Environment Makers have access to them in case they need to use those entities as object to detect, tagged text and input data respectively.

Some scenarios require at least System Customizer privileges to publish AI models and allow consumption since these actions imply changes to the Common Data Service schema. Therefore, we recommend Administrators to assign System Customizer to users that need to create such AI models.

When you create a binary classification AI model, a new field needs to be added to the input entity to store the prediction results from the prediction. Therefore, you need at least System Customizer rights to publish the model for the first time.

For text classification AI Models, an entity is created for every new model once the model runs for the first time. Therefore, only System Customizers or Administrators can run the model. After the model runs, administrators must modify the access rights to the newly created text classification entity in Common Data Service to allow users to consume the results.

### Related topics

[Security concepts in Common Data Service](/power-platform/admin/wp-security-cds)

