---
title:  Common issues and resolutions for AI Builder -  AI Builder | Microsoft Docs
description: Provides a list of common issues you might encounter while using AI Builder, and potential workarounds where applicable.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 08/27/2019
ms.author: joshrenn
ms.reviewer: v-dehaas
---

# Common issues and resolutions for AI Builder

Here are some issues that you might encounter when you  use AI Builder. Where applicable, workarounds are provided.


<!--from editor: Skipping a heading level isn't recommended. I'm bumping the level 3 heds up to a level 2. If you want to keep them at level 3, you need to add a level 2 heading. -->


## AI Builder is not set up correctly in your environment

If you are using an environment that was created before AI Builder was first released, it's possible that AI Builder wasn't set up correctly in your environment. To work around this issue, [create a new environment](https://docs.microsoft.com/power-platform/admin/create-environment) so that AI Builder can be correctly installed in that new environment. If you must use a particular environment, [contact support](https://docs.microsoft.com/power-platform/admin/get-help-support) for more options.

## AI Builder encounters errors reading data from your Common Data Service entity

Use the navigation links on the left side of your screen to locate the data preparation section for the type of AI model that you are working with. Make sure your Common Data Service environment is configured correctly so that your model can access it.

## AI Builder business card reader doesn't work for some users

Make sure that the user of the business card reader component has permissions in Common Data Service, or has access to the AI Builder model entity that is configured in the business card reader component.
