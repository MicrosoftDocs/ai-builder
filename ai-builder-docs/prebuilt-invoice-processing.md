---
title: Invoice processing prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the invoice processing prebuilt AI model from AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 03/29/2021
ms.author: jofernan
ms.reviewer: v-aangie
---

# Invoice processing prebuilt model

The invoice processing prebuilt AI model extracts key invoice data to help automate the processing of invoices. The invoice processing model is optimized to recognize common invoice elements like invoice ID, invoice date, amount due, and more.

## Use in Power Apps

For information on how to use the invoice processing prebuilt model in Power Automate, go to [Use the invoice processing prebuilt model in Power Apps](prebuilt-invoice-processing-powerapps.md).

## Use in Power Automate

For information on how to use the invoice processing prebuilt model in Power Automate, go to [Use the invoice processing prebuilt model in Power Automate](flow-invoice-processing.md).  


## Supported languages and files

Only English language invoices from the United States are currently supported.

To get the best results, provide one clear photo or scan per invoice.

- The image format must be JPEG, PNG, or PDF.
- The file size must be less than 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10,000 x 10,000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the Legal or A3 paper sizes or smaller.

## Model output

If an invoice is detected, the invoice processing model will output the following information:

|     Property                                        |     Definition                                                                                                      |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
|     Amount due   (text)                             |     Amount due as written on the invoice.                                                                            |
|     Amount due   (number)                           |     Amount due in standardized number format. Example: 1234.98.                                                      |
|     Confidence of   amount due                      |     How confident the model is in its prediction. Score between 0 (low confidence) and 1 (high confidence).       |
|     Billing address                               |     Billing   address.                                                                                               |
|     Confidence of   billing address                 |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Billing   address recipient                     |     Billing   address recipient.                                                                                     |
|     Confidence of   billing address recipient       |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Customer   address                              |     Customer address.                                                                                                |
|     Confidence of   customer address                |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Customer   address recipient                    |     Customer address recipient.                                                                                      |
|     Confidence of   customer address recipient      |     How confident the model is in its prediction. Score between 0 (low confidence) and 1 (high   confidence).       |
|     Customer ID                                     |     Customer ID.                                                                                                     |
|     Confidence of   customer ID                     |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Customer name                                   |     Customer name.                                                                                                   |
|     Confidence of   customer name                   |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Due date   (text)                               |     Due date as written on the invoice.                                                                              |
|     Due date   (date)                               |     Due date in standardized   date format. Example: 2019-05-31.                                           |
|     Confidence of   due date                        |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Invoice date   (text)                           |     Invoice date   as written on the invoice.                                                                        |
|     Invoice date   (date)                           |     Invoice date   in standardized date format. Example: 2019-05-31.                                       |
|     Confidence of   invoice date                    |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Invoice ID                                      |     Invoice ID.                                                                                                      |
|     Confidence of   invoice ID                      |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Invoice total   (text)                          |     Invoice total   as written on the invoice.                                                                       |
|     Invoice total   (number)                        |     Invoice total   in standardized date format. Example: 2019-05-31.                                      |
|     Confidence of   invoice total                   |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Line Items                                      |     The line items extracted from the invoice. Confidence scores are available for each column.  <ul><li>**Line item amount**: Amount for a line item. Returned in text and number format.</li><li>**Line item description**: Description for a line item. Returned in text format.</li><li>**Line item quantity**: Quantity for a line item. Returned in text and number format.</li><li>**Line item unit price**: Unit price for a line item. Returned in text and number format.</li><li>**Line item product code**: Product code for a line item. Returned in text format.</li><li>**Line item unit**: Unit for a line item (for example, kg and lb). Returned in text format.</li><li>**Line item date**: Date for a line item. Returned in text and date format.</li><li>**Line item tax**: Tax for a line item. Returned in text and number format.</li><li>**Line item all columns**: Returns all the columns from the line item as a line of text.</li></ul>                                               |
|     Purchase   order                                |     Purchase   order.                                                                                                |
|     Confidence of   purchase order                  |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Previous unpaid balance (text)                  |     Previous unpaid balance as written on the invoice.                                                               |
|     Previous unpaid balance (number)                |     Previous unpaid balance in standardized number format. Example: 1234.98.                                         |
|     Confidence of   previous unpaid balance         |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Remittance   address                            |     Remittance   address.                                                                                            |
|     Confidence of   remittance address              |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Remittance   address recipient                  |     Remittance   address recipient.                                                                                  |
|     Confidence of   remittance address recipient    |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Service   address                               |     Service   address.                                                                                               |
|     Confidence of   service address                 |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Service   address recipient                     |     Service   address recipient.                                                                                     |
|     Confidence of   service address recipient       |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Service start date (text)                       |     Service start date as written on the invoice.                                                                   |
|     Service start date (date)                       |     Service start date in standardized   date format. Example: 2019-05-31.                                           |
|     Confidence of   service start date              |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Service end date (text)                         |     Service end date as written on the invoice.                                                                     |
|     Service end date (date)                         |     Service end date in standardized   date format. Example: 2019-05-31.                                             |
|     Confidence of   service end date                |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Shipping   address                              |     Shipping   address.                                                                                              |
|     Confidence of   shipping address                |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Shipping   address recipient                    |     Shipping   address recipient.                                                                                    |
|     Confidence of   shipping address recipient      |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Subtotal   (text)                               |     Subtotal as written on the invoice.                                                                              |
|     Subtotal   (number)                             |     Subtotal in standardized number format. Example: 1234.98.                                                        |
|     Confidence of   subtotal                        |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Total tax   (text)                              |     Total tax as written on the invoice.                                                                             |
|     Total tax   (number)                            |     Total tax in standardized number format. Example: 1234.98.                                                       |
|     Confidence of   total tax                       |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Vendor   address                                |     Vendor   address.                                                                                                |
|     Confidence of   vendor address                  |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Vendor   address recipient                      |     Vendor   address recipient.                                                                                      |
|     Confidence of   vendor address recipient        |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Vendor name                                     |     Vendor name.                                                                                                     |
|     Confidence of   vendor name                     |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Detected text                                   |     Line of recognized text from running OCR on an invoice. Returned as a part of a list of text.                   |
|     Page number   of detected text                  |     Page on which the line of recognized text was found. Returned as a part of a list of text.                      |


## Limits

The following applies to calls made per environment across form processing models including prebuilt models: receipt processing and invoice processing.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Calls (per environment)|360|60 seconds|

## Create a custom invoice processing solution

The invoice processing prebuilt AI model is designed to extract common fields found in invoices. Because every business is unique, you might want to extract fields other than those included in this prebuilt model. It can also be the case that some standard fields aren't well extracted for a particular type of invoice you work with. To address this, there are two options:

- **View raw OCR results**: Every time the invoice processing prebuilt AI model processes a file you provide, it also does an OCR operation to extract every word written on the file. You can access the raw OCR results on the detected text output provided by the model. A simple search on the content returned by detected text might be enough to get the data you need.
- **Use form processing**: With AI Builder, you can also build your own custom AI model to extract specific fields and tables you need for the documents you work with. Just [create a form processing model](form-processing-model-overview.md) and train it to extract all the information from an invoice that doesn’t work well with the invoice extraction model.

Once you train your custom form processing model, you can combine it with the invoice processing prebuilt model in a Power Automate flow.

Here are some examples:

### Use a custom form processing model to extract additional fields that aren't returned by the invoice processing prebuilt model

In this example, we've trained a custom form processing model to extract a *loyalty program number*, only present in invoices from providers Adatum and Contoso.

The flow is triggered when a new invoice is added to a SharePoint folder. It then calls the invoice processing prebuilt AI model to extract its data. Next, we check if the vendor for the invoice that has been processed is either from Adatum or Contoso. If it’s the case, we then call a custom form processing model that we’ve trained to get that loyalty number. Finally, we save the extracted data from the invoice in an Excel file.

   > [!div class="mx-imgBorder"]
   > ![Invoice and form processing flow.](media/invoice-and-form-process-flow.png "Create a flow that uses a form processing model")

### Use a custom form processing model if the confidence score for a field returned by the invoice processing prebuilt model is low

In this example, we've trained a custom form processing model to extract the total amount from invoices where we usually get a low confidence score when using the invoice processing prebuilt model.

The flow is triggered when a new invoice is added to a SharePoint folder. It then calls the invoice processing prebuilt AI model to extract its data. Next, we check if the confidence score for the *Invoice total value* property is less than 0.65. If it’s the case, we then call a custom form processing model that we’ve trained with invoices where we usually get a low confidence score for the total field. Finally, we save the extracted data from the invoice into an Excel file.

   > [!div class="mx-imgBorder"]
   > ![Invoice and form processing flow for low scores.](media/invoice-and-form-process-flow2.png "Create a flow that uses a form processing model for low scores")
 
### Use the invoice processing prebuilt model to handle invoices that a custom form processing model hasn’t been trained to handle

One way to use the invoice processing prebuilt model is to use it as a fallback model to handle invoices that you haven’t trained in your custom form processing model. For example, let's say you built a form processing model, and trained it to extract data from your top 20 invoice providers. You could then use the invoice processing prebuilt model to process all new invoices or lower volume invoices. Here’s an example of how you could do it:

This flow is triggered when a new invoice is added to a SharePoint folder. It then calls a custom form processing model to extract its data. Next, we check if the confidence score for the detected collection is less than 0.65. If it’s the case, it probably means the provided invoice isn't a good match for the custom model. We then call the prebuilt invoice processing model. Finally, we save the extracted data from the invoice in an Excel file.

   > [!div class="mx-imgBorder"]
   > ![Invoice and form processing flow for new invoices.](media/invoice-and-form-process-flow3.png "Create a flow that uses a form processing model for new invoices")


[!INCLUDE[footer-include](includes/footer-banner.md)]
