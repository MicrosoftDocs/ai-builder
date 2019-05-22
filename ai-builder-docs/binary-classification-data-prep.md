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
If you have data outside of Common Data Service that you want to import for training in AI Builder, you need to create an entity first.
 
1. In PowerApps, select **Entities** in the left-side navigation pane, then select **New entity** at the top of the screen.

2. On the **New entity** screen, in the **Display name** field, enter the desired entity name. For this example, use **Adult Income Census**. Note that the other fields will automatically be populated.
 
3. On the **Field properties** screen, type **Id** in the **Display name** and **Name** fields .
4. At the top of the screen, select **Add field**.
5.	On the **Field properties** screen, type **Age** in the **Display name** and **Name** fields, and select **Whole Number** in the **Data type** menu.
6. Repeat these steps to add additional fields using the method above to create the following fields :

|Name	|Data type|
|---|---|
|Capital loss|	Whole number|
|Hours per week|Whole number|
|ID|	Text|
|Income|	Text|
|Marital status|	Text|
|Native country|	Text|
|Occupation|	Text|
|Race|	Text|
|Relationship|	Text|
|Sex|	Text|
|Work class|	Text|

>[!NOTE]
>In our example dataset, the label is not formatted correctly to directly import as a two-option field, but if you format your label field to be true and false, then you can simply create a two-option data type in this step for the label.

## Import local data into your entity
 
1.	In PowerApps, select **Entities** in the left-side navigation pane, select the down-arrow to the right of **Get data**, and then select **Get data from excel**.
2.	Select **Upload** and then select the file that contains the sample **Adult Income Census** data.
3.	If a Mapping errors exist message appears under **Mapping status**, it's okay-  select **Map fields**.
4.	Map only the fields you created, to the corresponding fields in the import data, and select **Save changes**. You do not need to map any fields you did not create.

> !NOTE
> - There may be a bug where if you update the fields after the initial save, the fields available for mapping may not be updated. In this case just create the entity under a new name.
> - There may be a bug where if the text fields start with an empty space, the import will not work correctly. Please remove any preceding spaces in your dataset.

5.	Under **Mapping status**, when a **Mapping was successful** message appears,  click **Import**. This may take a while depending on data size.
6.	 To view your data,  go back to **Entities** under **Data** in PowerApps, select **Adult Census Income**, select **Views**, and then select **Active Adult Census Incomes**.
7.	 You can add fields on the left side to validate that all the fields have been imported correctly. Click **Publish** to save the current view with the selected fields.

## Data field considerations
There are scenarios where you may need to update the field you are predicting.
- No label field at all
- Label field doesn’t consist of two options
### Create a Two-option field
In the previous example, **Income** is actually the label field, but the current type is **Text**. However, AI Builder binary classification requires the Two-option data type.
> !NOTE
> 
>If you are creating a label field based on another field(s),  please make sure that  during field selection in AI Builder, you deselect the field(s) that were used to populate the label field. They may be perfectly predictive of your outcome and should not be used to generate features for training.

1.	In the **Adult Census Income entity** screen, select **Add field**, and set these values:
- **Display Name** - **Label**
- **Data type** - **Two Options**
- **Yes** option - **>50K**
- **No** option - **<=50K**
2.	At the bottom of the **field property** screen, select the **Calculated or Rollup** dropdown menu, and then select **Calculation**.
3.	Select **Yes** to save pending changes. Here you can add the following condition:


### Next steps
[Create a text classification model](create-text-classification-model.md) 

### See also
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[PowerApps docs](https://docs.microsoft.com/powerapps/)<br/>
[Microsoft Flow docs](https://docs.microsoft.com/flow/getting-started)
