---
title: Use sample data to do object detection  -  AI Builder | Microsoft Docs
description: Provides steps to train and publish your object detection model in AI Builder.
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/06/2019
ms.author: aminab
ms.reviewer: v-dehaas
---

# Use sample data to do object detection

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To explore the possibilities of object detection in AI Builder, you can get started by building and training an object detection model using sample pictures and labels.

> [!NOTE]
> This sample data is added to your environment automatically if you enable the [Deploy sample apps and data](build-model.md#deploy-sample-apps-and-data) setting when you create your database.

## Get the sample data

Download [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171) file, which contains object detection sample images and labels.

> [!NOTE]
> The [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171) also contains sample files for working with other AI Builder model types, as well as some hands-on-labs that you can use to learn more about AI Builder. More information about the contents of the zip file is available in the [readme.txt](https://go.microsoft.com/fwlink/?linkid=2108226) file, which is contained in the zip file.

## Add labels in Common Data Service

1. Go to [Power Apps](https://make.powerapps.com/), and then select **Data > Entities** in the left navigation pane.
2. Prepare an entity with one column in a text format, either by using an existing one or creating a new one.
    - If you need to create a new entity, use [this guide](/powerapps/maker/common-data-service/data-platform-create-entity).
3. On the top menu, select **Get data**.
4. In the list of data sources, select **Excel**.
5. Select **Browse** to upload your Excel file, and then select the sheet or sheets that your data is in.
    - You might have to allow third-party cookies for your browser to complete this step.
6. On the **Edit Queries** screen, select **Transform table > Use first row as headers**.
7. Select **Next > Load to new entity**.
8. Use the drop-down menu to select your target entity, and then map your columns to the destination field.
9. Select **Next** to finish.

### Related topic

[Use an object detection component in Power Apps](/ai-builder/object-detector-component-in-powerapps)
