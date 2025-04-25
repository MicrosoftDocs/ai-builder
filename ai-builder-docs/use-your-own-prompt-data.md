---
title: Use your own data in a prompt
description: Learn how to use your own data in a prompt to get the answers you need.
author: CedrickBellarosa
contributors:
  - chplanty
  - Antrodfr
  - CedrickBellarosa
  - v-aangie
ms.topic: conceptual
ms.collection: 
    - bap-ai-copilot
ms.date: 01/24/2025
ms.author: cdbellar
ms.reviewer: angieandrews
---

# Add knowledge to a prompt

Prompts enable makers to use generative AI models addressing various types of content generation scenarios. These models use their default knowledge included in their training data to answer. However, this knowledge isn't sufficient to deal with use cases requiring business specific data context.

This point is where data Retrieval Augmented Generation (RAG) allows you to provide external information to augment the knowledge of the model. This augmentation can result in getting the answers you need.

## Add knwoledge and filter

1. By typing **/** or selecting **Add content**, users can select a data source object from the **Knowledge** section. 

   :::image type="content" source="media/use-your-own-prompt-data/select-data-source.png" alt-text="Screenshot of how to select a data source.":::

1. Users need to navigate in the data source and select one or multiple columns. They will be added as knowledge objects in the prompt.

    :::image type="content" source="media/use-your-own-prompt-data/add-data.png" alt-text="Screenshot of selected column.":::

1. You can filter the knowledge which is retrieved by clicking the knowledge object, then **Filter attribute** and selecting the field to filter in **Filter attribute**. You can set a free-form text or an input of the prompt inside **Filter value**.

    :::image type="content" source="media/use-your-own-prompt-data/filter-data.png" alt-text="Screenshot of how to filter column value.":::

1. You cane also filter using an input. Let's create a prompt that gets all the accounts using the value of an input called named **Question**. 

    :::image type="content" source="media/use-your-own-prompt-data/question-data.png" alt-text="Screenshot of how to use the input to filter knowledge":::

   The prompt will automatically filter all knowledge objects using the value of this input, which can be expressed with natural language.

## Insert data references in the prompt

You can also insert multiple data and related tables' data references in your prompt and use it with natural language by selecting **Insert** and navigating through the data and relationships.

Each data reference is used by the generative model to answer.

:::image type="content" source="media/use-your-own-prompt-data/insert-data.png" alt-text="Screenshot of how to insert 'Data' or 'Inputs' references directly in the prompt.":::

## Example of scenarios

The number of scenarios enabled by this capability is limited only by your creativity. The following list provides some examples.

- Create a summary of the account named `Name` using only these columns: `Account.Name`, `Account.Description`, `Account.Orders (Order).Name`, `Account.Orders (Order).Amount`.
- Classify the `Email` into one of these `Category.Name` matching based on `Category.Description`.
- Draft a reply to this `Problem` matching data from `FAQ.Topic` and getting inspiration from `FAQ.Solution`.
- Get answers to the `Question` by providing information about `Account.Account Name`, `Account.Account Number`, `Account.Address 1`, and `Account.Address 1: City`.

## Limitations

The following list describes the limitations of using your own data in a prompt.

- Data source is limited to Dataverse tables.
- Dataverse environment languages supported: English US, French, Japanese, Danish, Dutch, German, Italian, Brazilian Portuguese, Spanish, Simplified Chinese, Danish Norwegian, and Turkish.
- Virtual table use isn't yet supported.
- You can use only one table as the data source. However, you can reference fields from multiple relationships of this table.
- Only the attributes with the following data types are available as **Filter attribute** and in **+ Insert**: `text`, `number`, `date and time`, `choice`, `currency`, and u`nique identifier`.
- We support only English US formats for filtering values. For example, Filter value=121.5 is supported, while 121,5 isn't. Filter value=2024-12-25 is supported while 25/12/2024 isn't.
- You can only use direct relationships of the table added as data source.

    For example, you can use `Account.'Company Name (Contact)'.Name` and `Account.'Preferred User (User)'.'Last Name'` but not `Account.'Company Name (Contact)'.'Connected To (Connection)'.'Connection Name'`.

- The total number of records that can be retrieved is limited to 1,000.

## Related information

[Training: Create AI Builder prompts using your own Dataverse data (module)](/training/modules/ai-builder-grounded-prompts/)
