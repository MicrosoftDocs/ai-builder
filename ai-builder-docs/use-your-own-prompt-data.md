---
title: Add knowledge to your prompt
description: Learn how to add knowledge to your prompt to get the answers you need.
author: CedrickBellarosa
contributors:
  - chplanty
  - Antrodfr
  - CedrickBellarosa
  - v-aangie
ms.topic: concept-article
ms.collection: 
    - bap-ai-copilot
ms.date: 06/03/2025
ms.update-cycle: 180-days
ms.author: cdbellar
ms.reviewer: angieandrews
---

# Add knowledge to your prompt

Prompts enable you to use generative AI models addressing various types of content generation scenarios. These models use their default knowledge included in their training data to answer. However, this knowledge isn't sufficient to deal with use cases requiring business specific data context.

This point is where data Retrieval Augmented Generation (RAG) allows you to provide external information to augment the knowledge of the model. This augmentation can result in getting the answers you need.

## Add knowledge and filter

This section describes how to add knowledge to a prompt and filter it.

1. Type **/** or select **Add content** to choose a data source object from the **Knowledge** section.  

   :::image type="content" source="media/use-your-own-prompt-data/select-data-source.png" alt-text="Screenshot of how to select a data source.":::

1. Navigate the data source and select one or more columns. These are added as knowledge objects in the prompt.

    :::image type="content" source="media/use-your-own-prompt-data/add-data.png" alt-text="Screenshot of selected column.":::

1. Filter the retrieved knowledge by selecting the knowledge object, then select **Filter attribute**, and choose the field to filter in **Filter attribute**. Enter a free-form text or a prompt input in **Filter value**.

    :::image type="content" source="media/use-your-own-prompt-data/filter-data.png" alt-text="Screenshot of how to filter column value.":::

1. Filter using an input. Create a prompt that retrieves all accounts using the value of an input named **Question**.

    :::image type="content" source="media/use-your-own-prompt-data/question-data.png" alt-text="Screenshot of how to use the input to filter knowledge":::

   The prompt automatically filters all knowledge objects using the value of this input, expressed in natural language.

## Insert data references in the prompt

You can insert multiple data and related tables' data references in your prompt and use it with natural language. Do this by selecting **Insert** and navigating through the data and relationships.

The generative model uses each data reference to answer.

## Use connectors

You can select an existing connection to Salesforce, Oracle, SAP, or Zendesk. Then, select a table and insert one or several fields in the prompt, filtering the data on an attribute.

:::image type="content" source="media/use-your-own-prompt-data/use-connectors.png" alt-text="Screenshot of how to insert connectors references directly in the prompt.":::

## Example of scenarios

The number of scenarios enabled by this capability is limited only by your creativity. The following list provides some examples.

- Create a summary of the account named `Name` using only these columns: `Account.Name`, `Account.Description`, `Account.Orders (Order).Name`, `Account.Orders (Order).Amount`.
- Classify the `Email` into one of these `Category.Name` matching based on `Category.Description`.
- Draft a reply to this `Problem` matching data from `FAQ.Topic` and getting inspiration from `FAQ.Solution`.
- Get answers to the `Question` by providing information about `Account.Account Name`, `Account.Account Number`, `Account.Address 1`, and `Account.Address 1: City`.

## Limitations

The following list describes the limitations of using your own data in a prompt.

- Data sources are limited to Dataverse and Salesforce, Oracle, SAP, and ZenDesk connector tables.
- Connectors can only be used for prompts in Power Automate.
- Dataverse environment languages supported: English US, French, Japanese, Danish, Dutch, German, Italian, Brazilian Portuguese, Spanish, Simplified Chinese, Danish Norwegian, and Turkish.
- Virtual table use isn't yet supported.
- Only attributes with the following data types are available as **Filter attributes**: `text`, `number`, `date and time`, `choice`, `currency`, and `unique identifier`.
- Relationships are supported only for Dataverse. You can select up to two levels of relationships for the table added as a data source.

    For example, you can use `Account.'Company Name (Contact)'.Name` or `Account.'Company Name (Contact)'.'Connected To (Connection)'.'Connection Name'`.

- The number of records retrieved is 30 by default. You can increase this limit to 1,000 in the settings.

## Related information

- [Use your prompt actions in Microsoft Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Training: Create AI Builder prompts using your own Dataverse data (module)](/training/modules/ai-builder-grounded-prompts/)
