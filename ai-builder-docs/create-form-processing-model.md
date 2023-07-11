---
title: Create a document processing custom model in AI Builder
description: Learn how to create a document processing model in AI Builder.
author: JoeFernandezMS
contributors:
  - antrodfr
  - JoeFernandezMS
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 10/28/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# Create a document processing custom model

After you review the [requirements](form-processing-model-requirements.md), you can get started creating your document processing model.

## Sign in to AI Builder

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com).

1. On the left pane, select **AI Builder** > **Explore**.

1. Select **Extract custom information from documents**.

1. Select **Get Started**.

1. A step-by-step wizard walks you through the process by asking you to list all data you want to extract from your document. If you want to create your model by using your own documents, make sure you have at least five examples that use the same layout. Otherwise, you can [use sample data](form-processing-sample-data.md) to create the model.

1. Select **Train**.
 
1. Test the model by selecting **Quick test**.

## Select the type of document

On the **Choose document type** step, select the type of document you want to build an AI model to automate data extraction. There are two options:

- **Structured and semi-structured documents**. Structured and semi-structured documents are those where for a given layout, the fields, tables, checkboxes, and other items can be found in similar places. Examples of structured and semi-structured documents are invoices, purchase orders, delivery orders, tax documents, and more.

- **Unstructured and free-form documents**. Unstructured documents are those where there's no set structure, usually free documents with a varying number of paragraphs. Examples of unstructured documents are contracts, statement of work, letters, and more.

- **Invoices (preview)**. Augment the behaviors of the prebuilt invoice processing model by adding new fields to be extracted in addition to the ones by [default](prebuilt-invoice-processing.md#model-output), or samples of documents not properly extracted.

    :::image type="content" source="media/document-processing-choose-document-type.png" alt-text="Screenshot of the tiles under 'Select the type of documents your model will process'.":::

## Define information to extract

On the **Choose information to extract** screen, define the fields, tables, and checkboxes you want to teach your model to extract. Select the **+Add** button to start defining these.

:::image type="content" source="media/document-processing-choose-information-to-extract-step.png" alt-text="Screenshot of the step in the document processing wizard where to define the fields, tables, or checkboxes we want the AI model to extract.":::

- For each **Field**, provide a name you'd like the field to have in the model.

- For each **Checkbox**, provide a name you'd like the checkbox to have in the model. Define separate checkboxes for each item that can be checked in a document.

- For each **Table**, provide the name you'd like the table to have. Also, define the different columns that the model should extract.

 > [!NOTE]
 > The custom invoices model comes with default fields that can’t be edited.

## Group documents by collections

A collection is a group of documents that share the same layout. Create as many collections as document layouts that you want your model to process. For example, if you're building an AI model to process invoices from two different vendors, each having their own invoice template, create two collections.

:::image type="content" source="media/form-processing-multiple-layout-create-collections.gif" alt-text="Animation of creating collections.":::

For each collection that you create, you need to upload at least five sample documents per collection. Files with formats JPG, PNG, and PDF files are currently accepted.

:::image type="content" source="media/form-processing-multiple-layout-add-documents.gif" alt-text="Animation of uploading documents.":::

 > [!NOTE]
 > You can create up to 200 collections per model.

## Next step

[Tag documents in a document processing model](tag-form-processing-model.md)

### See also

[Training: Process custom documents with AI Builder (module)](/training/modules/get-started-with-form-processing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
