---
title: Use the receipt processor component in Power Apps -  AI Builder | Microsoft Docs
description: Provides information about how to use the receipt processor component in Power Apps
author: jarennert

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 05/20/2020
ms.author: joshrenn
ms.reviewer: v-dehaas
---

# Use the receipt processor component in Power Apps

The AI Builder receipt processor component scans and extracts information from receipts. You can take photos directly within the component or load images that have already taken. The data is recognized and extracted using the properties below.

For more information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started)

## Requirements
The receipt processor component works best with sales receipts, those commonly used by restaurants, gas stations, and retailers, among others. Both print and handwritten text can be detected.

Only English receipts from the United States are currently supported.

In order to get the best results, provide one clear photo or scan per receipt.

- The image format must be JPEG, PNG, or PDF.
- The file size must be less than 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10000 x 10000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the Legal or A3 paper sizes or smaller.
- For PDF documents, only the first 200 pages are processed.

## Key properties
|Property|Definition|
|---------|---------|
|**MerchantAddress**|Merchant address|
|**MerchantName**|Merchant name|
|**MerchantPhone**|Merchant phone|
|**OriginalImage**|The original image before processing|
|**Subtotal**|Subtotal|
|**Tax**|Tax|
|**Tip**|Tip|
|**Total**|Total|
|**TransactionDate**|Transaction date|
|**TransactionTime**|Transaction time|
|**Items**|The list of purchased items <ul><li>**Name**: Name of the item</li><li>**Price**: Price of the item</li><li>**Quantity**: Quantity of the item</li><li>**TotalPrice**: Total price of the item</li></ul>|
|**Results**|The list of all detected lines of text on the receipt <ul><li>**BoundingBox**: The coordinates of the line of text</li><li>**PageNumber**: Which page the line of text is found on</li><li>**Text**: The line of text</li></ul>|

## Accessibility guidelines
These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the text recognizer component.

### Related topics

[Receipt processing overview](prebuilt-receipt-processing.md)

[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
