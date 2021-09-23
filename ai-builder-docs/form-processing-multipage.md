---
title: Process multipage tables in form processor (experimental) - AI Builder | Microsoft Docs
description: This topic provides information on how extract tables from an invoice, and tables that span fewer or greater than two pages, in AI Builder.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 09/10/2021
ms.author: jofernan
ms.reviewer: v-aangie
---

# Process multipage tables in form processor (experimental)

[This topic is pre-release documentation and is subject to change.]

> [!IMPORTANT]
> - This is an experimental feature. Experimental features aren't meant for production use and might have restricted functionality. These features are available before moving up to the preview stage so that early adopter customers can try out something useful or help test the feature.
> 
> - For more information about experimental features and how to enable them, go to [Understand experimental, preview, and retired features in Power Apps](/powerapps/maker/canvas-apps/working-with-experimental-preview).

Depending on how many pages your table can span, you can choose from the following options to extract a table that:<!--note from editor: Edit to fix misplaced modifier, and to avoid "there are" and "leverage" (both via Microsoft Writing Style Guide).-->

- [Is from an invoice](#extract-a-table-from-an-invoice).
- [Spans up to two pages](#extract-a-table-that-spans-up-to-two-pages).
- [Spans more than two pages](#extract-a-table-that-spans-more-than-two-pages).

## Extract a table from an invoice

If the invoice you're looking to process is an English-language<!--note from editor: Suggested.--> invoice from the United States, the invoice processing prebuilt model can extract line items and then span multiple pages without your needing to train a model.

For instructions, go to [Invoice processing prebuilt model](prebuilt-invoice-processing.md).

## Extract a table that spans up to two pages

1. [Create a new form processing model](create-form-processing-model.md).

1. Perform the steps in [Define fields and tables to extract](create-form-processing-model.md#define-fields-and-tables-to-extract). On the **Choose information to extract** screen, select **Add** > **Multipage table (experimental)** to enable the experimental feature.

1. Follow the rest of the steps in [Create a new form processing model](create-form-processing-model.md) before you train your model.

    When uploading sample documents to train, upload as many documents as possible with tables that span up to two pages.

## Extract a table that spans more than two pages
<!--note from editor: Recommend not using "we recommend" because this is a new feature that the reader probably knows nothing about yet, so there aren't a lot of alternative methods floating around. Also, I couldn't figure out how these first steps related to the procedure that follows. -->
The general steps for extracting a table that span more than two pages are:

- [Tag the table](create-form-processing-model.md#tag-tables) on the first page where it's present.

- After the model has been trained, process the document page-by-page by using the [page range](form-processing-model-in-flow.md#page-range) feature.

- Capture all the tables across all pages and merge them in a single table.

Follow these steps:<!--note from editor: I don't know what this procedure heading should say because I'm not sure how much it covers of the process described above.-->

1.	[Create a new form processing model](create-form-processing-model.md).

2.	Perform the steps in [Define fields and tables to extract](create-form-processing-model.md#define-fields-and-tables-to-extract).

    On the **Choose information to extract** screen, do one of the following:

    - If the first occurrence of the table has different surrounding elements than the tables on the following pages, select **Add** > **Multipage table (experimental)** to enable the experimental feature.

        > [!div class="mx-imgBorder"]
        > ![Screenshot of page 1 with different surrounding elements than pages 2 and 3.](media/form-processing-multipage/table-page-1.png "Page 1 with different surrounding elements")

    - If the tables look the same and have similar-looking surrounding elements on all pages, select **Add** > **Single page table**.

        > [!div class="mx-imgBorder"]
        > ![Screenshot of all pages with similar surrounding elements.](media/form-processing-multipage/table-all-pages.png "All pages with similar surrounding elements")

1.	Follow the rest of the steps in [Create a new form processing model](create-form-processing-model.md).<!--note from editor: Edit okay? I thought this should echo the previous procedure. Also, the form-processing-train.md topic doesn't actually address tagging. -->

    - If you selected **Multipage table (experimental)**, tag the first two pages of the document where the table is present. 

    - If you selected **Single page table**, tag only the first page where the table is present.

After your form processing model is [trained and published](form-processing-train.md), you can use it in a cloud flow in Power Automate and process documents one page at a time to extract the tables for all pages.

### Use a cloud flow to process all pages in the document

The sample template in this procedure iterates through all the pages in the document. If you know the page range where you'd like to iterate, you can update the logic on the **Do until** loop.
<!--note from editor: I removed "en-us" because this link works without it. Note that there's a typo in the name of the template ("than-span" should be "that-span...") - is there any way to fix that?-->
1. Select [this cloud flow template](https://preview.flow.microsoft.com/galleries/public/templates/59284c1735b745dda07032720f31de47/use-form-processing-to-extract-tables-than-span-across-multiple-pages/) > **Continue**.

1. On the **Extract information from forms** action, specify the form processing model you've trained.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the AI model you've trained on the Extract information from forms action.](media/form-processing-multipage/extract-info.png "AI model you've trained on the 'Extract information from forms' action")

1. On the first **Apply to each** action, add the input entries from your table. Select *{table name}* entries, replacing *{table name}* with the name of the table in your model.<!--note from editor: Edit okay? I wasn't sure what these two bullets were saying. If this isn't right, is "should" the right word? It should <haha> be reserved for something that's optional but recommended.-->

    > [!div class="mx-imgBorder"]
    > ![Screenshot of output in the Apply to each action.](media/form-processing-multipage/apply-to-each.png "Output in the 'Apply to each' action")

1. The last **Apply to each 2** action iterates through the table that contains all the rows that have been extracted across all pages. Here you can add any action where you want to save the extracted data.<!--note from editor: I'm not sure what "where" means here. Does it mean you can add an action to define the location where the data should be saved?--> To reference the columns<!--note from editor: Is plural correct here? If so, would it be helpful to give an example of that type of expression also?--> you want to extract, use the following expression and replace *{column name}* with the name of the column in your table:

    items('Apply_to_each_2')?['*{column name}*']?['value']

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the last Apply to each 2 action.](media/form-processing-multipage/apply-to-each-2.png "The last 'Apply to each 2' action")

You can now save and test this flow to see it in action. You can then customize it to meet your needs.

### Extract fields for specific pages

You can extract fields for specific pages. For example, you might want header fields from the first page.

1. Add a **Do until** loop after the **Extract information from forms** action.

1. Select the **Current Iteration Index** condition.

1. Select **is equal to** from the dropdown list.

1. Enter the *{page number}* &minus; 1.

   For example, the condition for the first page would be **Current Iteration Index is equal to 0**.

> [!div class="mx-imgBorder"]
> ![Screenshot of a Do until loop.](media/form-processing-multipage/do-until.png "Example of the 'Do until' loop")

## Limitation

Rows that cut across pages<!--note from editor: What does this mean?--> aren't supported.

### See also

[Use a form processing model in Power Automate](form-processing-model-in-flow.md)
