---
title: Use your own data in a prompt
description: Learn how to use your own data in a prompt to get the answers you need.
author: CedrickBellarosa
contributors:
  - CedrickBellarosa
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 04/22/2024
ms.author: cdbellar
ms.reviewer: angieandrews
---

# Use your own data in a prompt

Custom prompts enable makers to use generative AI models addressing various type of content generation scenarios. These models use their default knowledge included in their training data to answer. However, this knowledge isn't sufficient to deal with use cases requiring business specific data context.

This point is where data Retrieval Augmented Generation (RAG) allows you to provide external information to augment the knowledge of the model. This augmentation can result in getting the answers you need.

## Add data and filter

Makers can use the **Data used** option to select one Dataverse table. The fields of the active view of this table are used by the generative model to get more knowledge while answering based on the custom prompt defined and inputs provided.

:::image type="content" source="media/use-your-own-prompt-data/add-data.png" alt-text="Screenshot of how to select a Dataverse table as data to be used in the prompt builder.":::

You can filter the data, which is retrieved by expanding the table and selecting the filtered field and **Filter value**. The value can be a free-form text, an input of the prompt, or when filtering on a *choice* or *option set* as one of its named values.

To learn more about choices and option sets, go to [Types of columns](/power-apps/maker/data-platform/types-of-fields).

:::image type="content" source="media/use-your-own-prompt-data/filter-data.png" alt-text="Sscreenshot of how to filter the 'Opportunity' table's 'Status' based on inputs defined in the prompt builder or a list of values.":::

## Insert data references in the prompt

You can also insert multiple data and related tables' data references in your prompt and use it with natural language by selecting **Insert** and navigating through the data and relationships.

Each data reference is used by the generative model to answer.

:::image type="content" source="media/use-your-own-prompt-data/insert-data.png" alt-text="Screenshot of how to insert 'Data' or 'Inputs' references directly in the prompt.":::

## Example of scenarios

The number of scenarios enabled by this capability is limited only by your creativity. The following list provides some examples.

- Create a summary of the account named `Name` using only these columns: `Account.Name`, `Account.Description`, `Account.Orders (Order).Name`, `Account.Orders (Order).Amount`.
- Classify the `Email` into one of these `Category.Name` matching based on `Category.Description`.
- Draft a reply to this `Problem` matching data from `FAQ.Topic` and getting inspiration from `FAQ.Solution`.

## Limitations

The following list describes the limitations of using your own data in a prompt.

- Data source is limited to Dataverse tables.
- Virtual table use isn't yet supported.
- You can use only one table as the data source. However, you can reference fields from multiple relationships of this table.
- Only the attributes with the following data types are available as **Filter attribute** and in **+ Insert**: `text`, `number`, `date and time`, `choice`, `currency`, and u`nique identifier`.
- We support only English US formats for filtering values. For example, Filter value=121.5 is supported, while 121,5 isn't. Filter value=2024-12-25 is supported while 25/12/2024 isn't.
- You can only use direct relationships of the table added as data source.

    For example, you can use `Account.'Company Name (Contact)'.Name` and `Account.'Preferred User (User)'.'Last Name'` but not `Account.'Company Name (Contact)'.'Connected To (Connection)'.'Connection Name'`.

- The total number of records that can be retrieved is limited to 1,000.