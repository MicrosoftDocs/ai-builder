---
title: Improve the performance of your form processing model - AI Builder | Microsoft Docs
description: Provides tips to help you improve form processing model performance in AI Builder.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/29/2021
ms.author: jofernan
ms.reviewer: v-aangie
---

# Improve the performance of your form processing model

If your model performance isn't where you want it to be, for example you're getting bad results or low confidence scores, there are a few things you can try.

## Add more documents to the training data

The more documents you tag, the more AI Builder will learn how to better recognize the fields. To add more documents, edit your form processing model and upload more documents. You will find the option to edit the model on the details page of the model.

> [!div class="mx-imgBorder"]
> ![AI Builder home page.](media/form-processing-edit-model.png "Edit a form processing model")

## More tips

- For filled-in forms, use examples that have all of their fields filled in.
- Use forms with different values in each field.
- If your form images are of lower quality, use a larger data set (10-15 images, for example).
- If possible, use text-based PDF documents instead of image-based documents. Scanned PDFs are handled as images.
- When you create a form processing model, upload documents with the same layout where each document is a separate instance. For example, invoices from different months should be in separate documents and not all in the same one.
- Documents that have different layouts should go [into different collections](create-form-processing-model.md#group-documents-by-collections) when you upload samples for training. 
- If the form processing model is extracting values from neighboring fields from the one you want the model to extract, edit the model and tag adjacent values that are being wrongly picked up as being different fields. That way the model will better learn the boundaries for each field. 


### See also

- [Invoice processing prebuilt model](prebuilt-invoice-processing.md)
- [Receipt processing prebuilt model](prebuilt-receipt-processing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
