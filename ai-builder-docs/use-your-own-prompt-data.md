---
title: Use your own data in a prompt
description: Learn how to use your own data in a prompt to get the answers you need.
author: CedrickBellarosa
contributors:
  - CedrickBellarosa
  - Antrodfr
  - v-aangie
ms.topic: conceptual
ms.collection: bap-ai-copilot
ms.custom: ignite-2024
ms.date: 11/18/2024
ms.author: cdbellar
ms.reviewer: angieandrews
---

# Use your own data in a prompt

Custom prompts enable makers to use generative AI models addressing various types of content generation scenarios. These models use their default knowledge included in their training data to answer. However, this knowledge isn't sufficient to deal with use cases requiring business specific data context.

This point is where data Retrieval Augmented Generation (RAG) allows you to provide external information to augment the knowledge of the model. This augmentation can result in getting the answers you need.

## Add data and filter

You can use the **Data used** option to select one or several Dataverse tables. The fields in these tables are used by the generative model to get more knowledge while answering based on the custom prompt defined and inputs provided.

> [!NOTE]
> Your prompt might produce better results after saving and when indexing is complete. You can check the indexing status icon in the **Data used** panel.

:::image type="content" source="media/use-your-own-prompt-data/add-data.png" alt-text="Screenshot of how to select a Dataverse table as data to be used in the prompt builder.":::

You can filter the data, which is retrieved by expanding the table and selecting the filtered field and **Filter value**. The value can be free-form text or an input of the prompt.

:::image type="content" source="media/use-your-own-prompt-data/filter-data.png" alt-text="Sscreenshot of how to filter the 'Opportunity' table's 'Status' based on inputs defined in the prompt builder or a list of values.":::

You can filter by creating an input named **Question**. The data matching the question in all the tables added is used. Your question can be expressed with natural language, for example, *Which are my accounts in Seattle?*

:::image type="content" source="media/use-your-own-prompt-data/account-qa.png" alt-text="Screenshot of how to filter using a 'Question' input.":::

## Insert data references in the prompt

You can also insert multiple data and related tables' data references in your prompt and use it with natural language by selecting **Insert** and navigating through the data and relationships.

Each data reference is used by the generative model to answer.

:::image type="content" source="media/use-your-own-prompt-data/insert-data.png" alt-text="Screenshot of how to insert 'Data' or 'Inputs' references directly in the prompt.":::

## Examples of scenarios

The number of scenarios enabled by this capability is limited only by your creativity. The following list provides some examples.

- Create a summary of the account named `Name` using only these columns: `Account.Name`, `Account.Description`, `Account.Orders (Order).Name`, `Account.Orders (Order).Amount`.
- Classify the `Email` into one of these `Category.Name` matching based on `Category.Description`.
- Draft a reply to this `Problem` matching data from `FAQ.Topic` and getting inspiration from `FAQ.Solution`.
- Answer to the **Question** input by providing information about `Account.Account Name`, `Account.Account Number`, `Account.Address 1`, and `Account.Address 1: City`.

## Limitations

The following list describes the limitations of using your own data in a prompt.

- Data source is limited to Dataverse tables.
- Virtual table use isn't yet supported.
- You can use only two levels of relationships for each table added as data source.
    For example, you can use use `Account.'Company Name (Contact)'.Name` or `Account.'Company Name (Contact)'.'Connected To (Connection)'.'Connection Name'`.
- The total number of records that can be retrieved is limited to 30.
- Filtering on choice/option set column isn't supported yet.

## Related information

[Training: Create AI Builder prompts using your own Dataverse data (module)](/training/modules/ai-builder-grounded-prompts/)
