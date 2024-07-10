---
title: Use the receipt processor component in Power Apps - AI Builder
description: Learn how to use the receipt processor component in Power Apps.
author: Phil-cmd
contributors:
  - Phil-cmd
  - v-aandrews
ms.topic: conceptual
ms.custom: 
ms.date: 06/25/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the receipt processor component in Power Apps

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The AI Builder receipt processor component scans and extracts information from receipts. You can take photos directly within the component or load images that have already taken. The data is recognized and extracted using the properties below.

For more information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started)

[!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]

## Requirements

The receipt processor component works best with sales receipts, those commonly used by restaurants, gas stations, and retailers, and others. Both print and handwritten text can be detected.

Only English receipts from the United States are currently supported.

In order to get the best results, provide one clear photo or scan per receipt.

- The image format must be JPEG, PNG, or PDF.
- The file size must be less than 20 MB.
- The image dimensions must be between 50 x 50 pixels and 10,000 x 10,000 pixels.
- PDF dimensions must be at most 17 x 17 inches, which is the equivalent of the legal or A3 paper sizes or smaller.
- For PDF documents, only the first 200 pages are processed.

## Receipt properties

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

>[!NOTE]
> Receipt values are returned as strings. To manipulate them as numbers, you can use the [Value](/powerapps/maker/canvas-apps/functions/function-value) function. To manipulate them as dates or times, you can use the [DateValue](/powerapps/maker/canvas-apps/functions/function-datevalue-timevalue) and [TimeValue](/powerapps/maker/canvas-apps/functions/function-datevalue-timevalue) functions. You can also specify the language of the text with a language tag, such as "en-US".

## Additional properties

|Property|Definition|
|---------|---------|
|**DetectedFields**|Additional information for each of the [receipt properties](#receipt-properties) <ul><li>**BoundingBox**: The coordinates of the field</li><li>**Confidence**: How confident the model is in the detection of the field</li><li>**PageNumber**: Which page the field is found on</li><li>**Value**: The value of the field</li></ul>|
|**DetectedText**|The list of all recognized lines of text on the receipt <ul><li>**BoundingBox**: The coordinates of the line of text</li><li>**PageNumber**: Which page the line of text is found on</li><li>**Value**: The line of text</li></ul>|
|**OriginalImage**|The original image before processing|
|**DisplayMode**|<ul><li>**Edit**: Allows user input</li><li>**View**: Only displays data</li><li>**Disabled**: Does not allow user input</li></ul>|
|**Height**|The height of the component|
|**ImageDisplayed**|Whether the component displays the image or not|
|**ShowBoundingBoxes**|Whether the component displays the bounding boxes or not|
|**Text**|The text that appears on the button that activates the receipt processor |
|**Visible**|Whether the component appears or is hidden|
|**Width**|The width of the component|
|**X**|The distance between the left edge of the component and the left edge of the parent container or screen|
|**Y**|The distance between the top edge of the component and the top edge of the parent container or screen|

Additional design properties are available in the **Advanced** panel.

## Accessibility guidelines

These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the text recognizer component.

## Use the formula bar to retrieve the text value from the selected item in the ReceiptProcessor control

Here are some examples.

This expression concatenates the values in the 'DetectedText' column of the 'ReceiptProcessor1' table, separated by a comma and a space.

```power-fx
Concat(ReceiptProcessor1.DetectedText,Value,", ")
```

This expression retrieves the `PurchasedItems` property from the `ReceiptProcessor1` variable.

1. Select **+ Insert** > **Data table (preview)**.
1. On the left pane, select **DataTable1**, and then enter the following in the formula bar:

    ```power-fx
    ReceiptProcessor1.PurchasedItems
    ```

1. Select **Fields** > **+ Add field**.
1. Select **Name** > **Price** > **Quantity** > **TotalPrice**.
1. Select **Add**.

## Related information

- [Receipt processing overview](prebuilt-receipt-processing.md)<br/> 
- [Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
- [Training: Process receipts with AI Builder (module)](/training/modules/ai-builder-receipt-processing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
