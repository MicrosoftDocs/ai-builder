---
title: Process multipage tables in form processor (experimental) - AI Builder | Microsoft Docs
description: This topic provides information about how to build and use form processing models in AI Builder.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 09/09/2021
ms.author: jofernan
ms.reviewer: v-aangie
---

# Process multipage tables in form processor (experimental)

[This topic is pre-release documentation and is subject to change.]

> [!IMPORTANT]
> - This is an experimental feature, meaning it’s a work in progress.
> - Experimental features aren’t meant for production use and may have restricted functionality. These features are available before moving up to the preview stage so that early adopter customers can try out something useful or help test the feature.

Depending on how many pages your table can span, there are many options you can leverage. If the table you want to extract:

- Is fom an invoice
- Spans up to two pages
- Spans more than two pages

## Extract a table from an invoice

If the invoice you are looking to process is an English invoice from the United States, the invoice processing prebuilt model can extract line items than span multiple pages without to need to train a model.

For instructions, go to [Invoice processing prebuilt model](prebuilt-invoice-processing.md).

## Extract a table that spans up to two pages

By enabling the multipage table experimental feature, you can train a form processing model to extract data from tables than span up to two pages.

1. [Create a new form processing model](create-form-processing-model.md).

1. The first step is to [define fields and tables to extract](create-form-processing-model.md#define-fields-and-tables-to-extract). On the **Choose information to extract** screen, select **Add** > **Multipage table (experimental)** to enable the experimental feature.

1. Follow all steps in [Create a new form processing model](create-form-processing-model.md) before you train your model.

    When uploading sample documents to train, upload as many documents with tables spanning up to two pages as possible.

## Extract a table that spans more than two pages

For tables that span beyond two pages, do the following:

1. [Tag the table](create-form-processing-model.md#tag-tables) on the first page where it's present.

1. After the model has been trained, process the document page by page by leveraging the [page range](form-processing-model-in-flow.md#page-range) feature.

1. Capture all the tables across all pages and merge them in a single table.

The following steps will guide you on how to achieve this:

1.	[Create a new form processing model](create-form-processing-model.md).

2.	The first step is to [define fields and tables to extract](create-form-processing-model.md#define-fields-and-tables-to-extract). Depending on how your table is placed on the document, do one of the following in the first step on the **Choose information to extract** screen:

    - If the first occurrence of the table has different surrounding elements than the tables in the following pages, select **Add** > **Multipage table (experimental)** to enable the experimental feature.

        > [!div class="mx-imgBorder"]
        > ![Screenshot of page 1 with different surrounding elements than pages 2 and 3.](media/form-processing-multipage/table-page-1.png "Page 1 with different surrounding elements")

    - If the tables look the same and have similar looking surrounding elements in all pages, select **Add** > **Single page table**.

        > [!div class="mx-imgBorder"]
        > ![Screenshot of all pages with similar surrounding elements.](media/form-processing-multipage/table-all-pages.png "All pages with similar surrounding elements")

1.	Follow all the steps to [train the form processing model](form-processing-train.md). 
    - If you selected **Multipage table (experimental)**, tag the first two pages of the document where the table is present. 
    
    - If you selected **Single page table**, tag only the first page where the table is present.

1.	After your form processing model is [trained and published](form-processing-train.md), you can use it in a cloud flow in Power Automate and process documents one page at a time to extract the tables for all pages.

Here's an example that iterates across all pages on the document.

1.	Go to the following [cloud flow template](https://preview.flow.microsoft.com/en-us/galleries/public/templates/59284c1735b745dda07032720f31de47/use-form-processing-to-extract-tables-than-span-across-multiple-pages/) and select **Continue**.

1. Specify the form processing model you have trained on the **Extract information from forms** action.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of all pages with similar surrounding elements.](media/form-processing-multipage/extract-info.png "All pages with similar surrounding elements")

1. On the first **Apply to each** action, add the entries from your table in the input.
    - You should select **{table name} entries**.
    - Replace **{table name}** with the name of the table in your model.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of all pages with similar surrounding elements.](media/form-processing-multipage/apply-to-each.png "All pages with similar surrounding elements")

1. The last **Apply to each 2** action iterates through the table that contains all the rows that have been extracted across all pages. Here you can add any action where you want to save the extracted data. To reference the columns you want to extract, you must use the following expression:

    **items('Apply_to_each_2')?['{column name}']?['value']**

    Replace **{column name}** by the name of the column in your table.

   > [!div class="mx-imgBorder"]
    > ![Screenshot of all pages with similar surrounding elements.](media/form-processing-multipage/apply-to-each-2.png "All pages with similar surrounding elements")

You can now save and test this flow to see it in action. You can then customize it to meet your needs.

For information on testing, go to [Quick-test your model](form-processing-train.md).