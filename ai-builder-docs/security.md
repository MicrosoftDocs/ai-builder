---
title: Security in AI Builder - AI Builder | Microsoft Docs
description: Describes security information related to roles, privileges, and access in AI Builder and the services it connects to. 
author: v-aangie
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 04/09/2021
ms.author: kvivek
ms.reviewer: v-aangie
---

# Security in AI Builder

AI Builder relies on environment security and Microsoft Dataverse security roles and privileges to grant access to AI features in Power Apps. More information: [Security overview](/power-platform/admin/wp-security)

Some privileges are set by default in Dataverse. This allows built-in security roles to use AI Builder without further actions from system administrators. Specifically:

- Environment makers can use AI Builder to create AI models.
- Dataverse users can access data by using the models embedded in Power Apps.
- Administrators and system customizers can access all AI models created in the environment.

These security roles have privileges to the AI Builder tables in Dataverse. Custom security roles can create AI models if they have the same access to the AI Builder tables as the environment maker role.

> [!div class="mx-imgBorder"]
> ![Security roles screen](media/security-roles-screen.png "Security roles screen" )

Scenarios such as object detection, category classification, and prediction require Read access to Dataverse tables. Make sure environment makers have access to them. They need those tables for objects to detect, tagged text, and input data.

Some features require system customizer privileges to publish your AI models and to allow them to be consumed. These actions can make changes to the Dataverse schema. Administrators should assign system customizer privileges to users who want to create such AI models.

When you create a prediction AI model, a new data column is added to the input table to store the prediction results. For this reason, you need at least system customizer rights to publish the model for the first time.

For category classification AI models, a data table is created for every new model as soon as the model runs for the first time. Therefore, only system customizers or administrators can run the model. After the model runs, administrators must modify the access rights to the newly created category classification table in Dataverse to allow users to use the results.

## Roles
Microsoft Dataverse permissions have been mapped to the Dataverse standard roles. Assigning these roles to a 
user will provide the necessary privileges to use AI Builder features like described in this table:

![image](https://user-images.githubusercontent.com/20269762/119011237-23fd4a80-b995-11eb-91ee-b0e36a4ae89e.png)

### See also

[Security concepts in Dataverse](/power-platform/admin/wp-security-cds)


[!INCLUDE[footer-include](includes/footer-banner.md)]
