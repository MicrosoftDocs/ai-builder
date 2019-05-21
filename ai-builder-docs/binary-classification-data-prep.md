---
title: Data Preparation | Microsoft Docs
description: Provides an overview of AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Data Preparation

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Create your custom entity
If you have data outside of Common Data Service that you want to import for training in AI Builder, you need to create an entity first.
 
1. In PowerApps, select **Entities** in the left-side navigation pane, then select **New entity** at the top of the screen.

2. On the **New entity** screen, in the **Display name** field, enter the desired entity name. For this example, use **Adult Income Census**. Note the other fields will automatically be populated.
 
3. On the **Field properties** screen, type **Id** in the **Display name** and **Name** fields .
4. At the top of the screen, select **Add field**.
5.	On the **Field properties** screen, type **Age** in the **Display name** and **Name** fields, and select **Whole Number** in the **Data type** menu.
6. Repeat these steps to add additional fields using the method above to create the following fields : 

>[!NOTE]
>In our example dataset, the label is not formatted correctly to directly import as a two-option field, but if you format your label field to be true and false, then you can simply create a two-option data type in this step for the label.

### Next steps
[Browse AI model types](browse-ai-model-types) 

### See also
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[PowerApps docs](https://docs.microsoft.com/powerapps/)<br/>
[Microsoft Flow docs](https://docs.microsoft.com/flow/getting-started)
