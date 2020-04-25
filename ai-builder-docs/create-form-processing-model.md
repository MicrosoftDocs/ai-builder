---
title: Create a form processing model -  AI Builder | Microsoft Docs
description: Provides step-by-step instructions on how to create a form processing model in AI Builder.
author: JoeFernandezMS
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/28/2020
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Create a form processing model

After you review the [requirements](form-processing-model-requirements.md), you can get started creating your form processing model

## Sign into AI Builder

Follow these steps to sign into AI Builder:
1. Go to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/signin) and sign in with your organizational account.
1. In the left pane, select **AI Builder > Build**.
1. Select **Form processing**.
1. Type a name for your model.
1. If you want to create your model by using your own documents, make sure that you have at least five examples that use the same layout. Otherwise, you can use sample data to create the model.
1. Select **Create**.


## Upload and analyze documents

You need some sample documents to train your model for the type of forms you'll be working with.

1. Select **Add documents**.
 
   > [!div class="mx-imgBorder"]
   > ![Add documents screen](media/form-add-documents.png "Add documents screen")

1. Select at least five sample documents of the type of form you want to train the model for. Only JPG, PNG, and PDF files are accepted.
1. Verify the selection, and then select **Upload documents**.
1. After the upload has completed, select **Close**.
1. Select **Analyze**.

  > [!div class="mx-imgBorder"]
  > ![Select 'Analyze'](media/form-analyze.png "Select 'Analyze'")



### Upload your documents

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://flow.microsoft.com) and then in the navigation pane select **AI Builder** > **Build**. Then, select the Form processing AI model type.
2. Enter a name for your model and then select **Create**. 
3. Select **Add documents**, select a minimum of five documents, and then select **Upload**.

For more information about requirements for input documents, see [Requirements and limitations](form-processing-model-requirements.md).

> [!NOTE] 
> After you upload these documents, you can still remove some of the documents or upload additional ones.

### Analyze

During the analysis step, AI Builder examines the documents that you upload, and detects the fields and tables in your document. The time to complete this operation depends on the number of documents provided, but in most cases, it should only take a few minutes.

When the analysis has finished, select the thumbnail to open the field selection experience.

## Review documents and extracted data

If the analysis succeeds, it means AI Builder detected structured text in your form documents. A failed analysis can mean AI Builder didn't detect structured text in your documents. In that case, check that the documents you updated follow the [requirements and optimization tips section](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).

## Select form fields

### Fields and tables that are automatically detected

To help you get started, some fields and tables have been automatically detected for you. They are shown by dotted rectangles. If you want your model to return those fields, you just have to click on them and validate the selection. 

### Fields that are not detected automatically

Some fields in your document might not have been automatically detected by AI Builder. Draw a rectangle around the field you are interested in, give it a name and validate the selection. 

When you over your mouse through the different words in your documents, light blue boxes will be shown. This indicates that you can draw a rectangle around those words to select a field.

  > [!div class="mx-imgBorder"]
  > ![Select fields](media/form-select-fields.png "Select fields")

When you draw a rectangle to indicate a field, if your initial selection did not pick all the words you wanted, or picked additional ones, you can adjust your selection.

### Resizing fields that are automatically detected

If a field that you want your model to return has been automatically selected, but does not contain all the values for that field, you can adjust the selection by selecting the field, resizing the selection and validating the selection.

### Hiding fields

If you are finding difficult to select fields because of automated detected field suggestions that are incorrect, or fields that are too close to each other, you can click on a selected or suggested field and hide it. To show all the hidden fields, click on the option for this that will appear on the top as you hide fields. 

### Rename fields

Both for automatically detected fields as well as fields that you manually draw, you have the option to rename so it easier to reference them.

### Confirming fields

If you have drawn new fields, or resized automatically detected fields, you will be presented with all the documents that you have uploaded. In this step you will need to draw the fields that are marked as pending on the right panel. By doing this you are teaching your AI Builder model to recognize these fields in documents of this type.

To draw a field on a document, just start drawing a selection on the document and you will be asked to which field it corresponds to. You can also select **Draw in document** on the fields list to the right to star the selection process for that field.

If a field is not present on one of the documents, select **Field not in document**. 


To start, choose the fields that matter to you:

 1. Select the detected template card: **\<*Your model name*> form**.
 1. To select the fields, hover over a rectangle that indicates a detected field in the document, or select the fields in the right-side pane.
 1. Select **Edit** next to the selected field if you want to rename fields to align with your needs or normalize the extracted labels.

    When you hover over a detected field, the following information appears:

    - **Field name**: The name of the label for the detected field.
    - **Field value**: The value for the detected field.
    - **Confidence level**: Confidence score of retrieving this field compared to the trained model.

### Next step

[Train and publish your form processing model](form-processing-train.md)

### Related topics

[Form processing model in Power Automate](form-processing-model-in-flow.md)

[Form processing model in Power Apps](form-processor-component-in-powerapps.md)
