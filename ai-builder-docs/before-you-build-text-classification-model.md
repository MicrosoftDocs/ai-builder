---
title: Before you build a category classification model - AI Builder | Microsoft Docs
description: Describes the steps and requirements that you have to consider before you build your model.
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 07/23/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Before you build a category classification model

Before you build your category classification model, make sure your data is in Microsoft Dataverse and it's structured in the correct format.

## Prerequisites

- Training data should be in a Dataverse table.
- Make sure your administrator has assigned you a security role with **Read** privilege to training data.
- You have appropriate permissions to create tables in your Dataverse environment.
- AI Builder category classification supports the following languages: English, French, German, Italian, Spanish, and Portuguese. If you try to classify text items in other languages, your model might not work properly.

## Data preparation

The training data used to train the model from the Dataverse table should conform to the following:

- Text and tags should be stored in the same table as two (2) columns. Each row should have data in the text column.  

- You can provide one or more tags to a single text data in a row. You can also leave the tags column empty.

- If you have multiple tags that have been identified within the text provided, they should be provided as delimited text in the tags fields. Currently we support comma (,), semicolon (;), and tab as the separators.

  |Text  |Tags  |
  |---------|---------|
  |Great clean and quiet room with a free to go breakfast     | Dining, Room        |
  |Small but well-orchestrated room that was comfy   | Room        |
  |I love the view from the 13th floor   | (none)        |

- Make sure to have minimum 10 distinct text samples for each tag to be extracted. Tags with fewer than 10 samples won't be trained.

- In the previous example, there should be minimum 10 rows each that have been tagged with the **Dining** and **Room** tags. 

- If **Room** has been tagged to fewer than 10 rows in the data, it'll be ignored. The model will not be trained to categorize data for that tag.

- For every tag there should be a minimum of 10 text samples where they have not been used.

  |Text  |Tags  |
  |---------|---------|
  |Great clean and quiet room with a free to go breakfast     | Room        |
  |Small but well-orchestrated room that was comfy   | Room        |
  |(none)  | Room        |

  If all rows in the table have been tagged to **Room**, and there are no rows or fewer than 10 rows that have been tagged to another label, the model will fail the training process.

- There should be a minimum of two (2) tags with 10 text samples each included in the table.

- You can define up to 200 distinct tags. Each tag is a category that will be identified and extracted from the given text.

- Each text data should be fewer than 5,000 characters.

If you don't have training data and want to try AI Builder category classification, follow these [instructions](text-classification-sample-data.md) to use sample data.

## Examples of training data format

This section provides examples of the training data format in a Dataverse table.


|Columns  |Data type  |Size  |
|---------|---------|---------|
|Comments     | Text        | 3,000        |
|Tags     | Text        | 100        |
<br/>


|Comments  |Tags  |
|---------|---------|
|During my stay I was completely ignored. The staff failed to pick up on me<br/>aspirating and having a UTI. I also had pneumonia.      |  Care       |
|I was seen very soon after arriving each time and all the staff, nurse, doctor,<br/>and anesthetist were very helpful. There seems to be a good sense of teamwork.     | Staff, Check-in        |
|The equipment seemed up to date. The nurse/healthcare assistant seemed<br/>quite caring.     | Facilities, Staff         |

> [!Note]  
> If you don't have your own training data, and want to try AI Builder category classification, you can get started by downloading sample data for the category classification model. For more information, go to [Use sample data to do category classification](text-classification-sample-data.md).

## Import your data into Dataverse

Since training data for a category classification model should be available as a Dataverse table, let's begin with preparing data in Dataverse table.  

Dataverse includes a powerful set of connectors to help you import data from many sources. For more information, go to [Add data to a table in Microsoft Dataverse by using Power Query](/powerapps/maker/data-platform/add-data-power-query).

As an example, let's look at how to import training data from an Excel workbook. This example uses a file containing what's shown in the following table.

|Id  |Tags  |Text  |
|---------|---------|---------|
|1     | Dining        |Breakfast was a bit of a hassle.         |
|2     | Dining, Room        | Great clean and quiet room with a free to-go breakfast.        |
|3     | Room, Dining, Location        | The staff we dealt with was very friendly and helpful. The hallways and our room were clean and comfortable. Breakfast (included) was muffins and bagels.        |
|4     | Location, Dining        | Surrounding area is full of bars and restaurants.         |
|5     | Service        | Staff was respectful.        |

In the example, the tags are separated by comma (,). As an alternative, you can use semi-colon (;) or tab.

1. Sign in to [Power Apps](https://make.powerapps.com/).

1. Select the environment you want to work in.

   > [!div class="mx-imgBorder"]
   > ![Select your environment](media/select-environment.png "Select your environment")

1. Select **Data** > **Tables**.

1. Select your table. If you don’t have a table already, follow the steps in [Create a custom table](/powerapps/maker/data-platform/data-platform-create-entity).

1. Select **Data** > **Get data** > **Get data from Excel** from the ribbon of the selected table.

   > [!div class="mx-imgBorder"]
   > ![Get data from Excel](media/get-excel.png "Get data from Excel")

1. In the **Import data** screen, select the Excel file that has the data referred above in the [Examples of training data format](#examples-of-training-data-format) screen and then select **Upload**.


   > [!div class="mx-imgBorder"]
   > ![Upload an Excel file](media/upload-excel.png "Upload an Excel file")

1. Select **Map Columns** and review the field mappings in the **Column mappings for Text Category** screen.

   > [!div class="mx-imgBorder"]
   > ![Review the field mappings](media/map-excel.png "Review the field mappings")

    The left side lists all columns defined in the table and the dropdown on the right list the columns available in the Excel file. 

    Map the **Tags**, **Text**, and **Id** columns from Excel to the respective columns in the table.

1. Once you have mapped the columns select **Save changes** at the top-right to get back to the import step. 

   > [!div class="mx-imgBorder"]
   > ![Review the field mappings](media/map-columns.png "Review the field mappings")

1. Once you see the **Mapping status** as successful, select **Import** in the upper-right corner to begin import process.

   > [!div class="mx-imgBorder"]
   > ![Begin the import process by selecting the Import button](media/select-import.png "Begin the import process by selecting the Import button")

1. The import process may take a few minutes depending on the volume of data being imported. After a few minutes, refresh the **Data** tab of the table to find all the records imported from the Excel file.

You're now ready to go to the next step.

### Next step

[Create a category classification model](create-text-classification-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
