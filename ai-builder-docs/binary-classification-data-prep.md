---
title: Data preparation | Microsoft Docs
description: Provides an overview of AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Data preparation

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]
Before you create your binary classification model, you'll want to make sure your data is in Common Data Service, and that it's in the correct format. 

## Create your custom entity
If you have data outside of Common Data Service that you want to import for training in AI Builder, you need to create an entity first. In this example, we’ll provide a solution which has pre-defined custom entities. To use your own data,  [create](/powerapps/maker/common-data-service/data-platform-create-entity) a custom entity, and substitute your own entity for the example use here.

1. Download the AI Builder sample datasets solution.
1. In PowerApps, select **Solutions** in the left-side navigation pane, then select **Import** at the top of the screen.
1. In the popup screen, select **Choose File**, and then select **AIBuilderSampleDatasets_1_0_0_0.zip** that you downloaded in step 1.
1. Follow the on-screen instructions to import the solution, and then select **Close** after you finish.

Next, import the sample data into the entity. In this example, we use the Online Shopper Intention dataset:

1. In PowerApps, select **Entities** in the left-side navigation pane, select **Get data** > **Text/CSV**, and then copy and paste the following URL:
    >https://need.this.URL

1. Set the following properties, and then click **Next**:
    -  **On-premise data gateway**= *(none)*
    - **Authentication kind**= *Anonymous*
 
3. On the **Edit queries** screen, select **Transform table** and **Use first row as headers** in the dropdown menu, and then select **Next**.
10.	On the **Map entities** screen, make sure **Load to existing entity** is selected, and under **Destination entity**, select **aib_onlineshopperintention** in the drop down menu.
11.	Select the **Delete rows that no longer exist in the query output** checkbox, and then select the Auto-map function which is on the top right of the **Field mapping** screen.  Select **Next**.
12.	On the **Refresh settings** screen, select the **Refresh manually** checkbox, and then click **Create** to start the import process.

Allow some time for the import to complete. Then, make sure the data is imported correctly.
1. In PowerApps, go back to **Entities** under **Data**, and select **Online Shopper Intention**.
1. Select **Views**, and then select **Active Online Shopper Intention**.
14.	Add fields on the left side to validate that all the fields have been imported correctly. 
Select **Publish** to save the current view with the selected fields.

And you're done!


 

### Next steps
[Create a binary classification model](create-binary-classification-model.md) 
