---
title: Scenarios in preview - AI Builder | Microsoft Docs
description: Explain why some scenarios are in preview and what it means.
author: Antoine2F
ms.topic: conceptual
ms.custom: 
ms.date: 06/17/2022
ms.author: antode
ms.reviewer: angieandrews
---

# Preview features

AI Builder is released and is generally available. But, some of its features are still in preview status. These features display a **Preview** tag near their names:

 - On the AI Builder **Explore** page.
 - In the Power Apps Studio > **Insert** > **AI Builder** menu.

## Block preview scenarios

The environment administrator can decide to hide accesses to preview features. In the Microsoft Power Platform admin center, under **Settings** > **Features**, a toggle switch lets the admin specify whether preview features are displayed.

## FAQ

### What happens if a model linked to a scenario in preview mode is created and published, then the admin decides to hide all access to scenarios in preview?

 In that case, this model will be blocked; it can't be edited or retrained, and it can't be used to compute new predictions. It will be displayed in the list of models, but it will be disabled and the only action that will be allowed is Delete.

[!INCLUDE[footer-include](includes/footer-banner.md)]
