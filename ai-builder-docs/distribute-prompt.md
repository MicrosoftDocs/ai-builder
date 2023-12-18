---
title: Distribute your prompt using a solution
description: Learn how to distribute your prompt in a packaged solution.
author: antrodfr
contributors:
  - antrodfr
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 12/18/2023
ms.author: antrod
ms.reviewer: angieandrews
---

# Distribute your prompt using a solution

You can distribute a prompt as a *solution component*. After you create a prompt in AI Builder, make it available for other environments to use. Do this by packaging it into a solution, and then exporting it into a zip file. After the solution is imported in the target environment, the packaged AI model is available for use.

## Solution explorer

Use the Power Apps or Power Automate solution explorer to create solutions and add components&mdash;such as prompts&mdash;to them. You can also export and import solutions by using the solution explorer.

To learn more, go to [Introduction to solutions](/power-apps/maker/data-platform/solutions-overview).

> [!NOTE]
> Prompts can be added using the menu **Add exising > AI models** inside a solution.

## Recommended process

It's a good idea for you to develop prompts in a sandbox or development environment first. Then, you can deploy them to a production environment with managed solutions. If you need to copy your production environment into a sandbox environment, follow the instructions in [Copy an environment](/power-platform/admin/copy-environment).

Using this process, you can use the prompt immediately after you import it. No other action is required to use it in Power Apps or Power Automate, but it's a good idea to perform a quick test in AI Builder first.

## Automate the process

As prompts can be distributed across environments using solutions, you can automate your prompt lifecycle in the same way you would for other platform components. To learn more, go to
 [Application lifecycle management (ALM) with Microsoft Power Platform](/power-platform/alm).

## Change imported prompts

Generally, we don't recommend changing imported prompts because it generates unmanaged customizations. These customizations can prevent the prompt from being properly updated in the future. Changes include updating prompt instruction or configuration.

If you accidentally modify your prompt after you've imported, delete the imported solution and then import the solution again.

To avoid accidental modification of a prompt after import, it might be a good idea to disable customization in the managed properties of the prompt before importing it.

To disable customizations, do the following:

1. From the solution on the menu at the top, select **Managed Properties**.

1. Turn off **Allow customizations**.

    :::image type="content" source="media/ai-builder-managed-properties.png" alt-text="Screenshot of Managed properties.":::

