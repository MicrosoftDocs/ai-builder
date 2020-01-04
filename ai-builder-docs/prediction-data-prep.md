---
title: Data preparation -  AI Builder | Microsoft Docs
description: Provides the steps you'll need to follow to prepare your data for AI Builder in Common Data Service. 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 01/03/2020
ms.author: peterbi
ms.reviewer: v-dehaas
---

# Data preparation

Before you create your prediction model, you'll want to make sure your data is in Common Data Service, and that it's in the correct format.

## Create your custom entity

Do you have data that you want to import into Common Data Service for training in AI Builder? First, you have to create an entity. In this example, we’ll provide a solution that has predefined custom entities. To use your own data, [create a custom entity](/powerapps/maker/common-data-service/data-platform-create-entity) and substitute your own entity for the example used here.

> [!NOTE]
> For best results, use a dataset that is less than 1.5 GB in size. Otherwise, AI Builder uses only 1.5 GB of your data to train and predict. Since you can’t control which data exceeding the 1.5 GB limit is not used, you should optimize your data to stay under 1.5 GB.

1. Download the AI Builder sample datasets solution: [AIBuilderOnlineShopperIntention_1_0_0_0.zip](https://go.microsoft.com/fwlink/?linkid=2093415).
1. In Power Apps, select **Solutions** in the left-side navigation pane, then select **Import** at the top of the screen.
1. In the pop-up screen, select **Choose File**, and then select **AIBuilderOnlineShopperIntention_1_0_0_0.zip** that you downloaded in step 1.
1. Follow the on-screen instructions to import the solution, and then select **Close** after you finish.

Next, import the sample data into the entity. In this example, we use the **aib_onlineshopperintention.csv** file:

1. In the list of [AI Builder samples](https://go.microsoft.com/fwlink/?linkid=2093415), select the **aib_onlineshopperintention.csv** file, and then select **Download** to open the raw version of the file.

1. Copy the URL from the address bar in your browser. In this case, the URL to copy is: https://raw.githubusercontent.com/microsoft/PowerApps-Samples/master/ai-builder/aib_onlineshopperintention.csv.

1. In Power Apps, select **Entities** in the left-side navigation pane, select **Get data** > **Text/CSV**, and then paste the copied URL from the last step into the **File path** or **URL** box.

1. Set the following properties, and then select **Next**:

    - **On-premises data gateway** = *(none)*
    - **Authentication kind** = *Anonymous*

1. On the **Map entities** screen, make sure **Load to existing entity** is selected, and under **Destination entity**, select **aib_onlineshopperintention** in the drop-down menu.
1. Select the **Delete rows that no longer exist in the query output** check box.
1. Select the **Automap** function on the upper right of the **Field-mapping** screen and then select **Next**.
1. On the **Refresh settings** screen, select the **Refresh manually** check box, and then select **Create** to start the import process.

Allow some time for the import to complete. Then, make sure the data is imported correctly.

1. In Power Apps, go back to **Entities** under **Data** and select **Online Shopper Intention**.
1. Select **Views** and then select **Active Online Shopper Intention**.
1. Add fields on the left side to validate that all the fields have been imported correctly. 
1. Select **Publish** to save the current view with the selected fields.

And you're done!

### Next step
[Create a prediction model](prediction-create-model.md) 
