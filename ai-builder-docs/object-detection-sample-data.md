---
title: Use sample data to do object detection  -  AI Builder | Microsoft Docs
description: Provides steps to train and publish your object detection model in AI Builder.
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/05/2019
ms.author: aminab
ms.reviewer: kvivek
---

# Use sample data to do object detection 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To explore the possibilities of object detection in AI Builder, you can get started by building and training an object detection model using sample pictures and labels. 

## Get the sample data

Download object detection sample images and labels here. 



## Add labels in Common Data Service

1. select the down arrow to expand Data in the navigation pane.
2. Prepare an entity with one column in a text format, either by using an existing one or creating a new one
a. If you need to create a new entity, use this guide.
3. Under Data > Entities > Get data.
4. In the list of data sources, select Excel.
5. Select Browse to upload your Excel file, and then select the sheet or sheets your data is in.
a. You might have to allow third-party cookies for your browser to perform this step.
6. On the Edit Queries screen, select Transform table > Use first row as headers.
7. Select Next > Load to new entity.
8. Use the drop-down menu to select your target entity, and then map your columns to the destination field.
9. Hit ‘Next’


### Related topic

