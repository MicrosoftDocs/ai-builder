---
title: Improve the performance of your document processing model - AI Builder
description: Learn tips to help you improve document processing model performance in AI Builder.
author: JoeFernandezMS
contributors:
  - Phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 01/10/2024
ms.author: jofernan
ms.reviewer: angieandrews
---

# Improve the performance of your document processing model

If your model performance isn't where you want it to be, for example you're getting bad results or low confidence scores, there are some things you can try.

## Interpret your model accuracy score

Interpret your accuracy score to identify what your model is struggling to extract. Model evaluations include recommendations for raising the score.

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com/).
1. On the left pane, select **... More** > **AI hub**.
1. Under **Discover an AI capability**, select **AI models**.

    *(Optional)* To keep **AI models** permanently on the menu for easy access, select the pin icon.
1. Open the document processing model you want to investigate. You should see the accuracy score.

    > [!NOTE]
    > In the following cases you won’t see accuracy scores for document processing models:
    > - If the model was trained by selecting ‘Unstructured and free-form documents’ as document type. Currently, accuracy scores are returned only for models of type ‘Structured and semi-structured documents’.
    > - Your model was imported from another environment.
    > - If your model was trained before January 1, 2022. In this case, you can retrain it.

1. On the model details page, you should see the general accuracy score.

    :::image type="content" source="media/improve-the-performance-of-your-form-processing-model/accuracy-score.png" alt-text="Screenshot of the accuracy score.":::

1. To get details, select **review full evaluation**.

    :::image type="content" source="media/improve-the-performance-of-your-form-processing-model/model-evaluation.png" alt-text="Screenshot of the 'Model evaluation' screen, 'Overview' tab.":::

    In this panel, you can navigate among different tabs to identify what your model is struggling to extract. You can browse the **Collection**, **Field**, **Table**, and **Checkbox** tabs to find what isn’t processed properly.

    Here's an example of the information in the **Field** tab.

    :::image type="content" source="media/improve-the-performance-of-your-form-processing-model/field-evaluation.png" alt-text="Screenshot of the 'Model evaluation' screen, 'Field' tab.":::

    In this example, you want to improve the accuracy of the **Vendor** information.

    :::image type="content" source="media/improve-the-performance-of-your-form-processing-model/field-evaluation-poor.png" alt-text="Screenshot of a poor accuracy score in the 'Field' tab.":::

    See suggestions on what you can do to improve your model by hovering over items with a poor accuracy score. For example, you might see a recommendation to [provide more sample documents](#add-more-documents-to-the-training-data) for training.

## Common questions

### What can I do if I have a low accuracy score for a field, table, or checkbox?

1. Check that the field, table, or checkbox has been tagged correctly in all the documents.
1. Provide more sample documents for training where the field, table, or checkbox is present.

### What can I do if I have a low accuracy score for a collection?

Check that the documents within the collection all have the same layout. To learn more about collections, go to [Group documents by collections](create-form-processing-model.md#group-documents-by-collections). 

## Add more documents to the training data

The more documents you tag, the more AI Builder will learn how to better recognize the fields. To add more documents, edit your document processing model and upload more documents. You'll find the option to edit the model on the details page of the model.

:::image type="content" source="media/improve-the-performance-of-your-form-processing-model/form-processing-edit-model.png" alt-text="Screenshot of the details page with the option to edit a document processing model.":::

## More tips

- For filled-in forms, use examples that have all of their fields filled in.
- Use forms with different values in each field.
- If your form images are of lower quality, use a larger data set (10-15 images, for example).
- If possible, use text-based PDF documents instead of image-based documents. Scanned PDFs are handled as images.
- When you create a document processing model, upload documents with the same layout where each document is a separate instance. For example, invoices from different months should be in separate documents and not all in the same one.
- Documents that have different layouts should go [into different collections](create-form-processing-model.md#group-documents-by-collections) when you upload samples for training. 
- If the document processing model is extracting values from neighboring fields from the one you want the model to extract, edit the model and tag adjacent values that are being picked up incorrectly as being different fields. By doing this, the model will better learn the boundaries for each field.

### See also

- [Invoice processing prebuilt model](prebuilt-invoice-processing.md)
- [Receipt processing prebuilt model](prebuilt-receipt-processing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
