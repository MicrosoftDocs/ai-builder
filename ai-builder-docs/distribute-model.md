---
title: Distribute your model -  AI Builder | Microsoft Docs
description: Describes how to distribute your AI Builder model in a packaged solution.
author: Dean-Haas
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 08/26/2019
ms.author: antode
ms.reviewer: v-dehaas
---

# Distribute an AI model

You can distribute an AI model as a solution component. After you create a model in AI Builder, make it available for other environments to use by packaging it into a solution, and then exporting it into a zip file. After the solution is  imported in the target environment, the packaged AI model is available for use.

## Solution explorer

 PowerApps provides a solution explorer that allows you to create solutions and add components such as AI models to them. The solution explorer also allows you to export and import solutions.

For more information see [Use solutions in PowerApps](/powerapps/maker/common-data-service/use-solution-explorer).

## Recommended process

AI models should be developed in a production sandbox environment and deployed in a production environment using managed solutions. You can copy a production environment to a different environment by following [these instructions](/power-platform/admin/copy-environment).

You shouldn't do any training or configuration changes of AI models after you import them to a production environment. Doing so would add unmanaged customizations which would prevent proper update of the AI models in the future.

For more information, see [Introduction to Solutions](/powerapps/developer/common-data-service/introduction-solutions).

## Limitations

- You can't export an AI Builder preview model in a solution.
- You can't export an unpublished AI Builder model in a solution.
- You can't delete an imported solution that contains an AI Builder preview model in Solution Explorer.
- You can't upgrade a solution that contains an AI Builder model
- Imported AI Builder models do not show performance information on the model details page.
- An AI Builder model’s managed properties can’t be modified, they are set to customizable by default.
- Imported model attributes are created with the **new_** attribute, not the default publisher attribute.
- You can't create a new AI Builder model in Solution Explorer.
- You can't modify an AI Builder model properties in Solution Explorer.
