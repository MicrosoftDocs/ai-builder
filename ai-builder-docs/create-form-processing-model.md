---
title: Create a document processing custom model in AI Builder
description: Learn how to create a document processing model in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - antrodfr
  - JoeFernandezMS
  - v-aangie
ms.topic: conceptual
ms.date: 12/12/2024
ms.author: plarrue
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

- **Fixed-template documents**: Previously known as *structured*, this option is ideal when, for a given layout, the fields, tables, checkboxes, signatures, and other items can be found in similar places. You can teach this model to extract data from structured documents that have different layouts. This model has a quick training time.
- **General documents**: Previously known as *unstructured*, this option is ideal for any kind of documents, especially when there's no set structure, or when the format is complex. You can teach this model to extract data from structured or unstructured documents that have different layouts. This model is powerful, but has long training time.
- **Invoices**: Augment the behaviors of the prebuilt invoice processing model by adding new fields to be extracted in addition to the ones by [default](prebuilt-invoice-processing.md#model-output), or samples of documents not properly extracted.

## Try the new model version (Preview)

By selecting the toggle **Try the new model version (Preview)**, you can try the latest preview model version for Fixed template documents and General documents.

> [!IMPORTANT]
> - The new model version is a preview release.
> - Preview releases aren't meant for production use and might have restricted functionality. These releases are subject to [supplemental terms of use](https://www.microsoft.com/en-us/business-applications/legal/supp-powerplatform-preview/), and are available before an official release so that customers can get early access and provide feedback.

:::image type="content" source="media/create-form-processing-model/try_preview_toggle_yes.png" alt-text="Screenshot of the tile try preview toggle to yes.":::

### Benefits of using the preview model

- **Enhanced accuracy**: Expect higher accuracy in data extraction.
- **Latest OCR enhancements**: The preview model includes the latest Optical Character Recognition (OCR) updates. This update resolves many common OCR issues, especially when handling complex text formats like barcodes, QR codes, and watermarks.
- **Confidence scores for tables**: You can get confidence scores for tables, table rows, and individual table cells

### How to check the model version

You can easily verify the version used to train and publish your model. Select **Settings** > **Published model version** > **Last trained model version**.

:::image type="content" source="media/create-form-processing-model/last-published-model-version-ga-last-trained-preview.png" alt-text="Screenshot of the 'Model settings' to get the last published model version GA and the last trained model version in preview.":::

### How to change the model version

You can edit the trained or published model version (preview) and train it with the general availability (GA) version.

1. Select **Edit model**.
1. Select **Try the new model version (Preview)**.
1. Select the **No** toggle.

:::image type="content" source="media/create-form-processing-model/select_documents_preview_toggle_No.png" alt-text="Screenshot of the tile try preview toggle to No.":::
  
You can edit the trained or published model general availability (GA) version and train it with the model version (Preview).

1. Select **Edit model**.
1. Select **Try the new model version (Preview)**.
1. Select the **Yes** toggle.

:::image type="content" source="media/create-form-processing-model/select_documents_preview_toggle_yes.png" alt-text="Screenshot showing the tile try preview toggle to yes.":::

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

- [Training: Process custom documents with AI Builder (module)](/training/modules/get-started-with-form-processing/)
- [Interpret confidence score for tables and table cells](interpret-confidence-score.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
