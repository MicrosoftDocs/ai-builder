---
title: Use sample data to do entity extraction - AI Builder | Microsoft Docs
description: Provides the information you need to try out an entity extraction model with sample data AI Builder.
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 08/03/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Use sample data to do entity extraction

You can get started with the entity extraction model using sample data. The sample data provided refers to feedback or conversations related to travel. The intent is to be able to use the entity extraction AI model to extract and identify entities related to places, persons, organizations, date, time, and a custom entity type: **Location Type**. 

## Get the sample data

1. Download the AIBuilderLab.zip and look for AIBuilderLabSolution_1_0_0_1.zip that contains the sample table, *Travel Feedback*. 

   Sample data for this table can be found in the Lab Data\EntityClassification\aib_travelfeedback.csv,

1. Sign in to [Power Apps](https://make.powerapps.com/) and choose the environment where you have imported the solution from step 1.

1. Go to **Solutions** > **AIBuilderLabs** > **Tables** > **Travel Feedback**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of AI Builder Lab Solution screen showing Travel Feedback table.](media/entity-solution.png "AI Builder Lab Solution screen showing Travel Feedback table")

1. Select **Data** > **Get Data** > **Get data from Excel** from the ribbon.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of Travel Feedback screen with import option to get data from Excel.](media/entity-excel.png "Travel Feedback screen with import option to get data from Excel")

      You'll see the Import data screen:

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the Import data screen.](media/entity-import.png "Import data screen")

1. Select **aib_travelfeedback.csv**, which has the data to be imported in this table.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the Import data screen with aib_travelfeedback.csv selected.](media/entity-import-csv.png "Import data screen with aib_travelfeedback.csv selected")

1. Review the column mappings by selecting **Map columns**.

1. Map the **Name** and **Comments** columns in the **Source values** column, and select **Save changes**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of column mappings to Travel Feedback table.](media/entity-import-map.png "Column mappings to Travel Feedback table")

   You'll return to the Import data screen with status updated to reflect that the mappings are complete.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the Import data screen showing that mapping was successful.](media/entity-import-map-done.png "Import data screen showing that mapping was successful")

1. Select **Import** on the top right for the import process to begin.

   It may take a few minutes for the import process to complete, depending on the rows included in the file provided.

1. Go to the **Data** tab of the Travel Feedback table in the solution to view all the records imported.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the Import data screen showing that mapping was successful.](media/entity-import-map-view.png "Import data screen showing that mapping was successful")
