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

After the model creation, it is likely that you will need to improve your model on a regular basis using Production data. The **feeback loop** feature will help
you automate this continous process.

> [!NOTE]
> For now, only custom **Document processing** models are supported by the feedback loop feature.

## Select documents to add in the feedback loop
The first thing you will have to do is select the documents eligible for the feedback loop. This has to be done from within the **Power Automate flow** that runs 
your model.

### New flow
If you don't have a Power Automate flow to run your model yet, you can simply create a new one from the model detail page after publishing the model.

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/signin).

1. In the left pane, select **AI Builder** > **Models**. Then click on the model for wish you would like to set-up the feedback loop (if your model is not published yet, click on the Publish button before continuing).

1. Click on **Use model** and select **Build intelligent automations**. Pick up the template that best fits your needs.

*Add image here*

1. Validate the template connexions to land in the Power Automate flow authoring experience

1. From there, go to the **Feedback loop** section to edit the conditions that will allow you to add documents in the feedback loop storage.

In this case we defined a condition stating that confidence score of the *Total* field should be higher than 0.7 (70%), otherwise the document goes in the feedback loop storage.

*Add image here*

> [!NOTE]
> The feedback loop storage is a Dataverse table within the the same environment in which the flow runs. The table is called **AI Builder Feedback Loop**. Unless you need to delete records in the table, you don't need to access it directly to make the feedback loop work.

