---
title: Improve the performance of your form processing model - AI Builder | Microsoft Docs
description: Provides tips to help you improve form processing model performance in AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 03/31/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# Improve the performance of your form processing model

If your model performance isn't where you want it to be, for example you're getting bad results or low confidence scores, there are some things you can try.

## Interpret your model accuracy score

Interpret your accuracy score to identify what your model is struggling to extract. Model evaluations include recommendations for raising the score.

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/signin).

1. In the left pane, select **AI Builder** > **Models**.

1. Open the form processing model you want to investigate. You should see the accuracy score. If you don’t see the accuracy score, your model might not have been trained since January 1, 2022. In this case, you can retrain it. Another reason you won't see the accuracy score is that your model has been imported from another environment.

    > [!NOTE]
    >
    > If you don't see the accuracy score, your model might not have been trained since January 1, 2022 or it includes functionality that's in preview. We recommend that you retrain your model and go back to the page once done.

1. On the model details page, you should see the general accuracy score. <!--Is this the same score as in step 2-->

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the accuracy score.](media/improve-the-performance-of-your-form-processing-model/accuracy-score.png "Accuracy score")

1. To get details, select **review full evaluation**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Model evaluation screen, Overview tab.](media/improve-the-performance-of-your-form-processing-model/model-evaluation.png "Model evaluation screen, Overview tab")

    In this panel, you can navigate among different tabs to identify what your model is struggling to extract. You can browse the **Collection**, **Field**, **Table**, and **Checkbox** tabs to find what isn’t processed properly.

    Here's an example of the information in the **Field** tab.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Model evaluation screen, Field tab.](media/improve-the-performance-of-your-form-processing-model/field-evaluation.png "Model evaluation screen, Field tab")

    In this example, you'll want to improve the accuracy of the **Vendor** information.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of a poor accuracy score in the Field tab.](media/improve-the-performance-of-your-form-processing-model/field-evaluation-poor.png "Poor accuracy score in the Field tab")

    See suggestions on what you can do to improve your model by hovering over items with a poor accuracy score. For example, you might see a recommendation to [provide more sample documents](#add-more-documents-to-the-training-data) for training.

### Common questions

**What can I do if I have a low accuracy score for a field, table, or checkbox?**

1. Check that the field, table, or checkbox has been tagged correctly in all the documents.

1. Provide more sample documents for training where the field, table, or checkbox is present. 

**What can I do if I have a low accuracy score for a collection?**

Check that the documents within the collection all have the same layout. To learn more about collections, go to [Group documents by collections](create-form-processing-model.md#group-documents-by-collections). 

## Add more documents to the training data

The more documents you tag, the more AI Builder will learn how to better recognize the fields. To add more documents, edit your form processing model and upload more documents. You'll find the option to edit the model on the details page of the model.

> [!div class="mx-imgBorder"]
> ![Screenshot of the details page with the option to edit a form processing model.](media/improve-the-performance-of-your-form-processing-model/form-processing-edit-model.png "Details page with the option to edit a form processing model")

## More tips

- For filled-in forms, use examples that have all of their fields filled in.
- Use forms with different values in each field.
- If your form images are of lower quality, use a larger data set (10-15 images, for example).
- If possible, use text-based PDF documents instead of image-based documents. Scanned PDFs are handled as images.
- When you create a form processing model, upload documents with the same layout where each document is a separate instance. For example, invoices from different months should be in separate documents and not all in the same one.
- Documents that have different layouts should go [into different collections](create-form-processing-model.md#group-documents-by-collections) when you upload samples for training. 
- If the form processing model is extracting values from neighboring fields from the one you want the model to extract, edit the model and tag adjacent values that are being picked up incorrectly as being different fields. By doing this, the model will better learn the boundaries for each field.

### See also

- [Invoice processing prebuilt model](prebuilt-invoice-processing.md)
- [Receipt processing prebuilt model](prebuilt-receipt-processing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
