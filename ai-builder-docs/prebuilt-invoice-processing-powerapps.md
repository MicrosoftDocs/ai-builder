---
title: Use invoice processing in Power Apps - AI Builder
description: Learn how to use AI Builder invoice processing in Power Apps.
author: phil-cmd
ms.topic: how-to
ms.custom: 
ms.date: 01/08/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use invoice processing in Power Apps

AI Builder invoice processing combined with Power Fx lets you extract key details from invoices like invoice ID, vendor names, and dates, quickly and accurately. This low-code solution simplifies data handling and streamlines financial processes.

**Supported document types**: Invoices

## Requirements

For best results, provide one clear photo or high-quality scan per document.

Learn more about requirements in the [Supported languages and files](prebuilt-invoice-processing.md#supported-languages-and-files) section in [Invoice processing prebuilt AI model](prebuilt-invoice-processing.md).

## Available fields

|Available fields|Type|
|----------------|----|
|AmountDue|Text|
|BillingAddress|Text|
|BillingAddressRecipient|Text|
|CustomerAddress|Text|
|CustomerAddressRecipient|Text|
|CustomerId|Text|
|CustomerName|Text|
|Customer TaxId|Text|
|DueDate|Text|
|InvoiceDate|Text|
|InvoiceId|Text|
|InvoiceTotal|Text|
|paymentTerms|Text|
|PreviousUnpaidBalance|Text|
|PurchaseOrder|Text|
|RemittanceAddress|Text|
|RemittanceAddressRecipient|Text|
|ServiceAddress|Text|
|ServiceAddressRecipient|Text|
|ServiceEndDate|Text|
|ServiceStartDate|Text|
|ShippingAddress|Text|
|ShippingAddressRecipient|Text|
|SubTotal|Text|
|TotalTax|Text|
|VendorAddress|Text|
|VendorAddressRecipient|Text|
|VendorName|Text|
|VendorTaxId|Text|

## Available table items

|Available items|Type|
|---------------|----|
|Amount|Text|
|Date|Text|
|Description|Text|
|ProductCode|Text|
|Quantity|Text|
|Tax|Text|
|Unit|Text|
|UnitPrice|Text|

## Build your canvas app

1. Sign in to [Power Apps](https://make.powerapps.com/).
1. On the left-side navigation pane, select **+Create**.
1. Select the **Canvas app from blank** tile.
1. Name your app, select either **Tablet** or **Phone** format, and then select **Create**.
1. In the app editor, from the left navigation pane, select **Data** > **Add data**, and then search **Invoice processing**.
1. Select **+Insert** > **Add picture**.
1. Select **+Insert** > **Text label**.
1. Select **Label1** and enter a formula like the following example, where `UploadedImage1` is the image container:

    ```power-fx
    'Invoice processing'.Predict(UploadedImage1.Image).Fields.InvoiceId.Value.Text
    ```

      You can select your desired field from the available field.

     :::image type="content" source="media/prebuilt-invoice-processing-powerapps/invoice-processing-all-available-field-formula.png" alt-text="Screenshot of all available text fields.":::
  
1. Select **Save**, and then select the play button.

    :::image type="content" source="media/prebuilt-invoice-processing-powerapps/invoice-processing-invoice-id-result.png" alt-text="Screenshot of the result of an invoice ID.":::
  
You can also use this formula to retrieve the first item from the result and extract the description of that item as a text string.

```power-fx
First('Invoice processing'.Predict(UploadedImage1.Image).Tables.Items.Rows).Description.Value.Text
```

 :::image type="content" source="media/prebuilt-invoice-processing-powerapps/invoice-processing-first-description-result.png" alt-text="Screenshot of the first item from the result.":::
  
This expression concatenates the text values from the **Description** field of each row in the prediction results of an image related to invoice, and separates each value with a comma and a space.

```power-fx
Concat('Invoice processing'.Predict(UploadedImage1.Image).Tables.Items.Rows, Description.Value.Text, Char(10))
```

:::image type="content" source="media/prebuilt-invoice-processing-powerapps/invoice-processing-concat-description-result.png" alt-text="Screenshot of all text values from the description field.":::

## Related information

- [Cookbook: How to use AI Builder Invoice Processing in Power Apps](https://community.powerplatform.com/galleries/gallery-posts/?postid=59a0bbb0-b4c6-ef11-b8e8-7c1e52182eb9)
- [Invoice processing overview](prebuilt-invoice-processing.md)
- [Power Fx formula reference overview](/power-platform/power-fx/formula-reference-overview)
