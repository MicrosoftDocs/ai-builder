---
title: Use sample data to do object detection - AI Builder | Microsoft Docs
description: Provides information to help you get started by building and training an object detection model using sample pictures and labels in AI Builder.
author: amina196
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 11/06/2020
ms.author: aminab
ms.reviewer: v-dehaas
---

# Use sample data to do object detection

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

To explore the possibilities of object detection in AI Builder, you can get started by building and training an object detection model using sample pictures and labels.

> [!NOTE]
> This sample data is added to your environment automatically if you enable the [Deploy sample apps and data](build-model.md#deploy-sample-apps-and-data) setting when you create your database.

## Get the sample data

Download [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171) file, which contains object detection sample images and labels.

> [!NOTE]
 > The AIBuilder_Lab.zip file also contains sample files for working with other AI Builder model types, in addition to some hands-on labs that you can use to learn more about AI Builder. For more information about the contents of the zip file, see the [readme.txt](https://go.microsoft.com/fwlink/?linkid=2108226) file that's included in the zip file.

## Add labels in Microsoft Dataverse

1. Go to [Power Apps](https://make.powerapps.com/), and then select **Data** > **Entities** in the left pane.
2. Prepare an entity with one column in a text format, either by using an existing entity<!--Edit okay?--> or creating a new one.
    If you need to create a new entity, use [this guide](/powerapps/maker/common-data-service/data-platform-create-entity).
3. On the top menu, select **Get data**.
4. In the list of data sources, select **Excel**.
5. Select **Browse** to upload your Excel workbook, and then select the sheet or sheets that your data is in.
    You might have to allow third-party cookies for your browser to complete this step.
6. On the **Edit Queries** screen, select **Transform table** > **Use first row as headers**.
7. Select **Next** > **Load to new entity**.
8. Use the drop-down menu to select your target entity, and then map your columns to the destination fields<!--Plural okay?-->.
9. Select **Next** to finish.

### See also

[Use the object detector component in Power Apps](object-detector-component-in-powerapps.md)
