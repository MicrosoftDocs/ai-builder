---
title: Receipt processing prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the receipt processing prebuilt AI model from AI Builder.
author: jarennert

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 05/20/2020
ms.author: joshrenn
ms.reviewer: v-dehaas
---

# Receipt processing model

Prebuilt receipt processing models extract key information from receipts. It uses state-of-the-art optical character recognition (OCR) to detect printed and handwritten text in images.

## Use in Power Apps

The receipt processing prebuilt model is available in Power Apps by using the receipt processor component. For more information, see Receipt processor component in Power Apps.

## Use in Power Automate

For information on how to use the receipt processing prebuilt model in Power Automate, see Use receipt processing model in Power Automate.  

## Supported languages and files

Only English receipts from the United States are currently supported.

In order to get the best results, provide one clear photo or scan per receipt.

- The image format must be JPEG, PNG, or PDF.
- The file size must be less than 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10000 x 10000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the Legal or A3 paper sizes or smaller.
- For PDF documents, only the first 200 pages are processed.

## Model output

If a receipt is detected, the receipt processing model will output the following information:

|Property|Definition|
|---------|---------|
|**MerchantAddress**|Merchant address|
|**MerchantName**|Merchant name|
|**MerchantPhone**|Merchant phone|
|**Subtotal**|Subtotal|
|**Tax**|Tax|
|**Tip**|Tip|
|**Total**|Total|
|**TransactionDate**|Transaction date|
|**TransactionTime**|Transaction time|
|**Items**|The list of purchased items <ul><li>**Name**: Name of the item</li><li>**Price**: Price of the item</li><li>**Quantity**: Quantity of the item</li><li>**TotalPrice**: Total price of the item</li></ul>|
|**Results**|The list of all detected lines of text on the receipt <ul><li>**BoundingBox**: The coordinates of the line of text</li><li>**PageNumber**: Which page the line of text is found on</li><li>**Text**: The line of text</li></ul>|
