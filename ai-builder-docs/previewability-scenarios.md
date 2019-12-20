---
title: Scenarios in preview -  AI Builder | Microsoft Docs
description: Explain why some scenarios are in preview and what it means
author: Antoine2F
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 08/27/2019
ms.author: antode
ms.reviewer: v-dehaas
---

# Preview features

AI Builder has been shipped and is generally available, but some of it's features are still in preview status.
You will notice them as they display a 'Preview' tag near their names

 - in the AI Builder/ Build page
 - in the Maker Studio/ Insert / AI Builder menu

## Block preview scenarios

Admin of an environment can decide to hide all accesses to scenarios in preview. In PowerPlatform Admin Center / Settings/ Features, a toggle allows to specify if scenarios in preview should be displayed or not.

## FAQ

### What happens if a model linked to a scenario in Preview mode is created and published, then Admin decides to hide all accesses to scenarios in Preview?

 In that case, this model will be blocked: it cannot be edited or retrained, and it cannot be used to compute new predictions. It is displayed in list of models, but is disabled and only specific actions are allowed : delete.
