---
title: Invoice processing prebuilt AI model
description: Learn about the invoice processing prebuilt AI model from AI Builder.
author: phil-cmd
contributors:
  - antrodfr
  - phil-cmd
  - JoeFernandezMS
  - v-aangie
ms.topic: article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 06/13/2025
ms.update-cycle: 180-days
ms.author: plarrue
ms.reviewer: angieandrews
---

# Invoice processing prebuilt AI model

The invoice processing prebuilt AI model extracts key invoice data to help automate the processing of invoices. The invoice processing model is optimized to recognize common invoice elements like invoice ID, invoice date, amount due, and more.

The **Invoices** model allows you to augment the default behavior by building a [custom Invoices model](create-form-processing-model.md#select-the-type-of-document).

## Use in Power Apps

Learn how to use the invoice processing prebuilt model in Power Apps in [Use the invoice processing prebuilt model in Power Apps](prebuilt-invoice-processing-powerapps.md).

## Use in Power Automate

Learn how to use the invoice processing prebuilt model in Power Automate in [Use the invoice processing prebuilt model in Power Automate](flow-invoice-processing.md).  

## Supported languages and files

The following languages are supported: Albanian (Albania), Czech (Czech Republic), Chinese (simplified) China, Chinese (traditional) Hong Kong SAR, Chinese (traditional) Taiwan, Danish (Denmark), Croatian (Bosnia and Herzegovina), Croatian (Croatia), Croatian (Serbia), Dutch (Netherlands), English (Australia), English (Canada), English (India), English (United Kingdom), English (United States), Estonian (Estonia), Finnish  (Finland), French (France), German (Germany), Hungarian (Hungary), Icelandic (Iceland), Italian (Italy), Japanese (Japan), Korean (Korea), Lithuanian (Lithuania), Latvian (Latvia), Malay (Malaysia), Norwegian (Norway), Polish (Poland), Portuguese (Portugal), Romanian (Romania), Slovak (Slovakia), Slovenian (Slovenia), Serbian (Serbia), Spanish (Spain), Swedish (Sweden).

To get the best results, provide one clear photo or scan per invoice.

- The image format must be JPEG, PNG, or PDF.
- The file size must not exceed 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10,000 x 10,000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the Legal or A3 paper sizes or smaller.
- For PDF documents, only the first 2,000 pages are processed.

## Model output

If an invoice is detected, the invoice processing model outputs the following information:

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
|     Customer tax ID                                 |     The taxpayer number associated with the customer.                                                                |
|     Confidence of customer tax ID                   |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
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
|     Payment terms                                   |     The terms of payment for the invoice.                                                                          |
|     Confidence of   payment terms                   |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
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
|     Vendor tax ID                                   |     The taxpayer number associated with the vendor.                                                                  |
|     Confidence of   vendor tax ID                   |     How confident the model is in its prediction. Score between 0 (low confidence)   and 1 (high confidence).       |
|     Detected text                                   |     Line of recognized text from running OCR on an invoice. Returned as a part of a list of text.                   |
|     Detected key                                    |     Key-value pairs are all the identified labels or keys and their associated responses or values. You can use these to extract additional values that aren't part of the predefined list of fields.                       |
|     Detected value                                  |     Key-value pairs are all the identified labels or keys and their associated responses or values. You can use these to extract additional values that aren't part of the predefined list of fields.                       |