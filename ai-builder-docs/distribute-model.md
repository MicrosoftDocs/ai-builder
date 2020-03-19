---
title: Distribute your model -  AI Builder | Microsoft Docs
description: Describes how to distribute your AI Builder model in a packaged solution.
author: Dean-Haas
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/01/2020
ms.author: antode
ms.reviewer: v-dehaas
---

# Distribute an AI model

You can distribute an AI model as a solution component. After you create a model in AI Builder, make it available for other environments to use by packaging it into a solution, and then exporting it into a zip file. After the solution is  imported in the target environment, the packaged AI model is available for use.

For more information on Solutions, see [Introduction to Solutions](/powerapps/developer/common-data-service/introduction-solutions).

## Solution explorer

 Power Apps provides a solution explorer that allows you to create solutions and add components such as AI models to them. The solution explorer also allows you to export and import solutions.

For more information, see [Use solutions in Power Apps](/powerapps/maker/common-data-service/use-solution-explorer).

## Recommended process

It's a good idea to develop AI models in a sandbox or development environment first. Then, deploy them to a production environment using managed solutions. If you need to copy your production environment into a sandbox environment, you can follow [these instructions](/power-platform/admin/copy-environment).

This process allows you to use the model directly after you import it. No additional action is required to use it in Power Apps or Power Automate, but it's a good idea to perform a quick-test in AI Builder first. 

Note that you have to publish a model before you can add it to a Solution.

## AI model customizations

Before you export your model, it's a good idea to disable customization.  By default, users can make changes to the model after they import it.

Disable customization in the managed properties of your AI model before you export it. Once you've disabled customization, your model will include a note that you have limited the possible actions on the models.

## Changes to imported models

It's not recommended to make changes to the model after importing it, which is possible when models are customizable. Unmanaged customizations can prevent proper update of the models in the future.  

These changes include updating the model's basic information, retraining, rescheduling, or republishing.
If you accidentally perform actions after import, just delete the imported solution, and then import the solution again.

## Importing status

For object detection and form processing models, the import process may continue after import action is finished. In this case "Importing" appears in the AI Builder model's list page. This is normal and can last several minutes.

## Limitations

- Import of solutions containing form processing models is not currently available.
- Only published models can be added in a solution.
- For object detection and form processing, only models trained after April 1st, 2020 can be added in a solution.
- Import of an object detection or form processing model should be done within 1 month of export. However, you can still import after that period if the source model remains unchanged after its export.
- Changes to imported models are not recommended.
- If you are using a model within a Power App or a Power Automate flow, you need to explicitly add the app and the model in the solution. The model is not considered an app or flow dependency.
- You can't create a new version of an imported object detection model because the training data set is not part of the imported solution. You should create a new model instead.
- You can't create a new AI Builder model in solution explorer.  
