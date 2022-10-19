---
title: Receipt processing prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the receipt processing prebuilt AI model from AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: 
ms.date: 08/30/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# Receipt processing prebuilt model

Receipt processing is a prebuilt model that uses state-of-the-art optical character recognition (OCR) to detect printed and handwritten text and extract key information from receipts.

## Use in Power Apps

The receipt processing prebuilt model is available in Power Apps by using the receipt processor component. For more information, see [Use the receipt processor component in Power Apps](prebuilt-receipt-processor-component-in-powerapps.md).

## Use in Power Automate

For information on how to use the receipt processing prebuilt model in Power Automate, see [Use the receipt processing prebuilt model in Power Automate](flow-receipt-processing.md).  

## Supported languages, markets, and files

Receipts from Australia (English), Canada (English), France (French), Germany (German), United States (English), Great Britain (English), India (English), Italy (Italian), Portugal (Portuguese) and Spain (Spanish) are supported.

To get the best results, provide one clear photo or scan per receipt.

- The image format must be JPEG, PNG, or PDF.
- The file size must not exceed 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10,000 x 10,000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the Legal or A3 paper sizes or smaller.
- For PDF documents, only the first 2,000 pages are processed.

## Model output

If a receipt is detected, the receipt processing model will output the following information:


|Property|Definition|
|---------|---------|
|**MerchantName**|Merchant name|
|**MerchantAddress**|Merchant address|
|**MerchantPhone**|Merchant phone number|
|**TransactionDate**|Transaction date|
|**TransactionTime**|Transaction time|
|**PurchasedItems**|The list of purchased items <ul><li>**Name**: Name of the purchased item</li><li>**Price**: Price of the purchased item</li><li>**Quantity**: Quantity of the purchased item</li><li>**TotalPrice**: Total price of the purchased item</li></ul>|
|**Subtotal**|Subtotal|
|**Tax**|Tax|
|**Tip**|Tip|
|**Total**|Total|
|**DetectedText**|The list of all recognized lines of text on the receipt|

## Limits 

The following applies to calls made per environment across document processing models including prebuilt models: receipt processing and invoice processing.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Calls (per environment)|360|60 seconds|


[!INCLUDE[footer-include](includes/footer-banner.md)]
