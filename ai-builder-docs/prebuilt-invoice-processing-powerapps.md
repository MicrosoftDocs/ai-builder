---
title: Use invoice processing in Power Apps - AI Builder
description: Learn how to use AI Builder invoice processing in Power Apps.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: 
ms.date: 11/20/2024
ms.author: jofernan
ms.reviewer: angieandrews
---

# Use invoice processing in Power Apps

AI Builder invoice processing combined with Power FX lets you extract key details from invoices like invoice ID, vendor names, dates, quickly and accurately. This low-code solution simplifies data handling and streamlines financial processes.

**Supported document types:**
•	Invoices

## Requirements

For best results, provide one clear photo or high-quality scan per document.
Go to the Invoice Processing Supported Languages and Files section for a clearer understanding of the requirements

## Available Fields

|Available Fields|Type|
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
1. Select **+Create** in the left-side navigation pane.
1. Select the **Canvas app from blank** tile. 
1. Name your app, select either **Tablet** or **Phone** format, and then select **Create**.
1. In the app editor, from the left navigation pane, select **Data**, select **Add data**, search **Invoice processing**
1. Select **+Insert**, select **Add picture**
1. Select **+Insert**, select **Text label **
1. Select **Label1**, enter a formula like the following example, where UploadedImage1 is the image container:
```power-fx
'Invoice processing'.Predict(UploadedImage1.Image).Fields.InvoiceId.Value.Text
```

  You can select your desired field from the available field

  :::image type="content" source="media/invoice_processing_all_available_fields_formula.png" alt-text="Screenshot of all available text Fields.":::
  
1. Select **Save**, and select the play button

  :::image type="content" source="media/invoice_processing_invoice_id_result.png" alt-text="Screenshot of the result of an invoice ID.":::
  

You can also use this formula to retrieve the first item from the result and extract the description of that item as a text string.

```power-fx
First('Invoice processing'.Predict(UploadedImage1.Image).Tables.Items.Rows).Description.Value.Text
```
 :::image type="content" source="media/invoice_processing_first_description_result.png" alt-text="Screenshot of the first item from the result.":::
  

This expression concatenates the text values from the "Description" field of each row in the prediction results of an image related to invoice, separating each value with a comma and a space.

```power-fx
Concat('Invoiceprocessing'.Predict(UploadedImage1.Image).Tables.Items.Rows,Description.Value.Text,", ")
```
 :::image type="content" source="media/invoice_processing_concat_description_result.png" alt-text="Screenshot of all text values from the description field.":::
 
 
## Related information

[Invoice processing overview](prebuilt-invoice-processing.md)

[Power FX formula reference overview](power-fx/formula-reference-overview.md)
