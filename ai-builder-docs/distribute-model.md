---
title: Distribute your model - AI Builder | Microsoft Docs
description: Describes how to distribute your AI Builder model in a packaged solution.
author: Dean-Haas
manager: cdbellar
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 10/26/2020
ms.author: antode
ms.reviewer: kvivek
---

# Distribute your AI model

You can distribute an AI model as a solution component. After you create a model in AI Builder, make it available for other environments to use by packaging it into a solution and then exporting it into a zip file. After the solution is imported in the target environment, the packaged AI model is available for use. More information: [Introduction to solutions](/powerapps/developer/common-data-service/introduction-solutions)

## Solution explorer

Use the Power Apps solution explorer to create solutions and add components&mdash;such as AI models&mdash;to them. You can also export and import solutions by using the solution explorer. More information: [Use solutions in Power Apps](/powerapps/maker/common-data-service/use-solution-explorer)

## Recommended process

It's a good idea to develop AI models in a sandbox or development environment first. Then deploy them to a production environment by using managed solutions. If you need to copy your production environment into a sandbox environment, you can follow [these instructions](/power-platform/admin/copy-environment).

Using this process, you can use the model immediately after you import it. No additional action is required to use it in Power Apps or Power Automate, but it's a good idea to perform a quick test in AI Builder first.

A model can only be added in a solution when a trained version of the model has been published. When the solution is exported and imported in a new environment, only the published version of the model is installed in the new environment.

## Disabling AI model customizations

Before you export your model, it's a good idea to disable customization in the managed properties of the model. This overrides the default setting, where users can make changes to the model after they import it. After you've disabled customization, your model will include a note that you have limited the possible actions on it.

## Changing imported models

If customization isn't disabled for a model, you can make changes to it after you import it. We recommend against doing this, because unmanaged customizations can prevent the model from being properly updated in the future.

Such changes can include updating basic information, retraining, rescheduling, or republishing the model. If you accidentally perform actions after you've imported, just delete the imported solution and then import the solution again.

## Importing status

For object detection models, the import process might continue after the import action is finished. In this case, "Importing" appears on the list page of the AI Builder model. This is normal and can last several minutes.

## Limitations

* For object detection and form processing, only models trained after April 2nd, 2020, can be added to a solution.
* Importing an object detection model or form-processing model should be done within one month of export. However, you can still import * After that period if the source model remains unchanged after its export.
* Changes to imported models aren't recommended.
* If you're using a model within an app or a Power Automate flow, you need to explicitly add the app and the model to the solution. The model isn't considered an app or flow dependency.
* You can't create a new version of an imported form processing, object detection or entity extraction model, because the training dataset isn't part of the imported solution. You should create a new model instead.
* You can’t set run schedule on imported category classification models.
* You can't create a new AI Builder model in solution explorer.
