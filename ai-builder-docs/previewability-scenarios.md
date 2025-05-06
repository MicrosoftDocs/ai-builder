---
title: Scenarios in preview - AI Builder
description: Explain why some scenarios are in preview and what it means.
author: Antoine2F
ms.topic: article
ms.custom: 
ms.date: 01/27/2025
ms.author: antode
ms.reviewer: angieandrews
---

# Preview features

AI Builder is released and is generally available. But, some of its features are still in preview status. These features display a **preview** tag near their names:

- On the AI Builder **Explore** page.
- In the Power Apps Studio > **Insert** > **AI Builder** menu.

## Block preview scenarios

The environment administrator can decide to hide accesses to preview features. In the Microsoft Power Platform admin center, under **Settings** > **Features**, a toggle switch lets the admin specify whether preview features are displayed.

## FAQ

### What happens if a model linked to a scenario in preview mode is created and published, then the admin decides to hide all access to scenarios in preview?

 In that case, this model is blocked; it can't be edited or retrained, and it can't be used to compute new predictions. It displays in the list of models, but is disabled. The only action that's allowed is delete.

[!INCLUDE[footer-include](includes/footer-banner.md)]
