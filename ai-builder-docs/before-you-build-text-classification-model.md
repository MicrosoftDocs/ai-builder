---
title: Before you build a category classification model - AI Builder | Microsoft Docs
description: Describes the steps and requirements that you have to consider before you build your model.
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/19/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Before you build a category classification model

Before you build your category classification model, make sure your data is in Microsoft Dataverse and it's structured in the correct format.

If you don't have training data and want to try AI Builder category classification, follow these [instructions](text-classification-sample-data.md) to use sample data.

## Prerequisites

- Training data should be in a Dataverse table.
- Make sure your administrator has assigned you a security role with **Read** privilege to training data.
- You have appropriate permissions to create tables in your Dataverse environment.
- AI Builder category classification supports the following languages: English, French, German, Italian, Spanish, and Portuguese. If you try to classify text items in other languages, your model might not work properly. 

## Data format

- Text and tags should be stored in text fields under the same table.
- Tags should be separated by using a delimiter. The following delimiters are supported: comma ( , ), semicolon ( ; ), tab character, or no delimiter.
- Tags that contain fewer than 10 distinct text items are ignored.
- There can be up to 200 categories. 
- Text must be fewer than 5,000 characters.

If data is represented in a table, it looks like the following.

| Text      | Tags                |
|-----------|---------------------|
| Text data | Tag X, Tag Y        |
| Text data | Tag X, Tag Y, Tag Z |

## Import your data into Dataverse

Dataverse includes a powerful set of connectors to help you import data from many sources. More information: [Add data to a table in Dataverse by using Power Query](/powerapps/maker/common-data-service/data-platform-cds-newentity-pq)

As an example, let's look at how to import training data from an Excel workbook. This example uses a file containing what's shown in the following table.

| Comment ID  | User comment  | Tags  |
|---|---|---|
|326589    |It's a powerful tool that helps make quick changes   |Good \| Quick \| Powerful |
|326590    |This program is great and has lots of potential. The user interface is intuitive and makes it easy to filter results. However, when I try to edit a link, I get an error.    |Potential, Easy \| Good, Ease of Use \| filters \| bug  |
|326591    | You need to work on your feature Y capabilities, they are not as good as your competition. |Feature Y \| Competition     |
|326592    |Easy to view data        |Easy \| Ease of use                                |
|326593    |I like how you made feature X easy to use. This reduces many complexities when I want to onboard new customers. | Easy \|  Good \| Feature X                             |

Note that tags data is separated by using a vertical bar or pipe ( | ).

1. Sign in to [Power Apps](https://make.powerapps.com/).

1. Select **Data** > **Tables** in the left panel, and then select **Data** > **Get data** from the menu at the top.

    If you need to create a new table, see [Create a custom table](/powerapps/maker/common-data-service/data-platform-create-entity).

1. In the list of data sources, select **Excel**.

1. Select **Browse OneDrive** to upload your Excel workbook, select **Next**, and then select the sheet or sheets your data is in.

    You might have to allow third-party cookies for your browser to perform this step.

1. On the **Power Query** screen, select **Transform table** > **Transform** > **Use first row as headers**.

1. Select the **Tags** column, and then select **Transform Column** > **Replace values**.

1. Replace the vertical bar ( | ) character with a semicolon ( ; ), and then select **OK**.

1. Now that your data is in the correct format, select **Next** > **Load to new table** (or **Next** > **Load to existing table** if you already have a target table).

1. Use the drop-down menu to select your target table, and then map your columns to the destination fields.

    > [!div class="mx-imgBorder"]
    > ![Map your columns to the destination fields.](media/create-text-model-map-columns-temp.png "Map your columns to the destination fields")

1. On the **Refresh settings** page, select **Refresh manually**.

You're all set. Power Query will import your data into your Dataverse table.

### Next step

[Create a category classification model](create-text-classification-model.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
