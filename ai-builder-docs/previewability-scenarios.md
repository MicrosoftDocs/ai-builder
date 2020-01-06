---
title: Scenarios in preview -  AI Builder | Microsoft Docs
description: Explain why some scenarios are in preview and what it means
author: Antoine2F
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 01/03/2020
ms.author: antode
ms.reviewer: v-dehaas
---

# Preview features

AI Builder is released and is generally available. But, some of its features are still in preview status.
You'll notice these features, as they display a **Preview** tag near their names

 - in the AI Builder/ Build page
 - in the Maker Studio/ Insert / AI Builder menu

## Block preview scenarios

The environment administrator can decide to hide accesses to preview features. In the Power Platform Admin Center in **Settings > Features**, a toggle lets you specify whether preview features are displayed.

## FAQ

### What happens if a model linked to a scenario in Preview mode is created and published, then Admin decides to hide all accesses to scenarios in Preview?

 In that case, this model will be blocked: it can't be edited or retrained, and it can't be used to compute new predictions. It's displayed in list of models, but is disabled and only specific actions are allowed: delete.
