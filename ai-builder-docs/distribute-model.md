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

AI models should be developed in a production sandbox environment and deployed in a production environment using managed solutions. You shouldn't do any training or configuration changes of AI models after you import them to a production environment. Doing so would add unmanaged customizations which would prevent proper update of the AI models in the future.

For more information, see [Introduction to Solutions](/powerapps/developer/common-data-service/introduction-solutions).

## Limitations

- Only prediction models can be distributed through solutions.
- Only published/scheduled models can be distributed through solutions.
- When adding a prediction model in a solution, the output entity used by the model needs to be added.
