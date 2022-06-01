---
title: Continously improve your model - AI Builder | Microsoft Docs
description: This topic provides an overview of how to continously improve AI Builder models.
author: antrod
ms.topic: conceptual
ms.custom:
ms.date: 06/01/2022
ms.author: antrod
ms.reviewer: angieandrews
---

# Continously improve your model

## Overview

After the model creation, it is likely that you will need to improve your model on a regular basis using Production data. The **Feeback loop** feature will help
you automate this continous process.

> [!NOTE]
> For now, only custom **Document processing** models are supported by the feedback loop feature.

## Select documents to add in the feedback loop
The first thing you will have to do is select the documents eligible for the feedback loop. This has to be done from within the **Power Automate flow** that runs 
your model.
