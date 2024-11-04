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
ms.date: 04/12/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Create a document processing custom model

After you review the [requirements](form-processing-model-requirements.md), you can get started creating your document processing model.

## Sign in to AI Builder

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com).
1. On the left pane, select **... More** > **AI hub**.
1. Under **Discover an AI capability**, select **AI models**.

    *(Optional)* To keep AI models permanently on the menu for easy access, select the pin icon.

1. Select **Extract custom information from documents**.
1. Select **Create custom model**.
1. A step-by-step wizard walks you through the process by asking you to list all data you want to extract from your document. If you want to create your model by using your own documents, make sure you have at least five examples that use the same layout. Otherwise, you can [use sample data](form-processing-sample-data.md) to create the model.
1. Select **Train**.
1. Test the model by selecting **Quick test**.

## Select the type of document

On the **Choose document type** step, select the type of document you want to build an AI model to automate data extraction. There are three options:

- **Fixed-template documents**: Previously known as Structured, this option is ideal when, for a given layout, the fields, tables, checkboxes, signatures and other items can be found in similar places. You can teach this model to extract data from structured documents that have different layouts. This model has a quick training time.
- **General documents**: Previously known as Unstructured, this option is ideal for any kind of documents, especially when there's no set structure, or when the format is complex. You can teach this model to extract data from structured or unstructured documents that have different layouts. This model is powerful, but has long training time.
- **Invoices**: Augment the behaviors of the prebuilt invoice processing model by adding new fields to be extracted in addition to the ones by [default](prebuilt-invoice-processing.md#model-output), or samples of documents not properly extracted.

    :::image type="content" source="media/create-form-processing-model/preview_toggle_no.png" alt-text="Screenshot of the tiles under 'Select the type of documents your model will process'.":::

## Try the new model version (Preview)

By selecting the toggle **Try the new model version (Preview)** you can try our latest preview model version for Fixed template documents and General documents

##### Benefits of using the Preview Model

**Enhanced Accuracy**: Expect higher accuracy in data extraction.

**Confidence Scores for Tables**: For custom models, users gain access to confidence scores for tables, table rows, and individual table cells

**Latest OCR Enhancements**: The preview model includes the latest Optical Character Recognition (OCR) updates, now in version 4.0. This update resolves many common OCR issues, especially when handling complex text formats like barcodes, QR codes, and watermarks.

:::image type="content" source="media/create-form-processing-model/try_preview_toggle_yes.png" alt-text="Screenshot of the tile try preview toggle to yes.":::

[!INCLUDE [cc_beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

### How to check the model version

You can easily verify the version used to train and publish your model.
Select **Settings**, and check **Published model version**, and **Last trained model version**

:::image type="content" source="media/create-form-processing-model/Last Published model version GA and last trained model version Preview.png" alt-text="Screenshot of the Model Settings to see the last published model version GA and the last trained model version in Preview.":::


### How to change the model version


You can	edit the last Published model version GA and train it with the Preview version

You can edit the last Trained model version (GA) and train it with the Preview version.


## Define information to extract

On the **Choose information to extract** screen, define the fields, tables, and checkboxes you want to teach your model to extract. Select the **+Add** button to start defining these.

:::image type="content" source="media/create-form-processing-model/define-information-to-extract.svg" alt-text="Screenshot of the step in the document processing wizard where you define the fields, tables, and checkboxes you want the AI model to extract.":::

1. For each **Text field**, provide a name for the field to use in the model.

1. For each **Number field**, provide a name for the field to use in the model.

    Also, define the format dot (**.**) or comma (**,**) as a decimal separator.

1. For each **Date field**, provide a name for the field to use in the model.

    Also, define the format (**Year**, **Month**, **Day**), or (**Monthly**, **Day**, **Year**), or (**Day**, **Month**, **Year**).

1. For each **Checkbox**, provide a name for the checkbox to use in the model.

    Define separate checkboxes for each item that can be checked in a document.

1. For each **Table**, provide the name for the table.

    Also, define the different columns that the model should extract.

 > [!NOTE]
 > The custom invoices model comes with default fields that can’t be edited.

## Group documents by collections

A *collection* is a group of documents that share the same layout. Create as many collections as document layouts that you want your model to process. For example, if you're building an AI model to process invoices from two different vendors, each having their own invoice template, create two collections.

:::image type="content" source="media/create-form-processing-model/form-processing-multiple-layout-create-collections.gif" alt-text="Animation of creating collections.":::

For each collection that you create, you need to upload at least five sample documents per collection. Files with formats JPG, PNG, and PDF files are currently accepted.

:::image type="content" source="media/create-form-processing-model/form-processing-multiple-layout-add-documents.gif" alt-text="Animation of uploading documents.":::

 > [!NOTE]
 > You can create up to 200 collections per model.

## Next step

[Tag documents in a document processing model](tag-form-processing-model.md)

## Related information

[Training: Process custom documents with AI Builder (module)](/training/modules/get-started-with-form-processing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
