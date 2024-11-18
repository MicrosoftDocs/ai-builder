---
title: Interpret confidence score for tables and table cells
description: Learn how to interpret the confidence score for tables and table cells.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: 
- bap-ai-copilot
ms.date: 11/12/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Interpret confidence score for tables and table cells

A confidence score for tables and cells in general documents quantifies how certain the model is about its predictions on structured data. Higher scores indicate greater confidence, while lower scores suggest uncertainty. These scores help prioritize reliable outputs, guide human review, and improve accuracy in applications like data extraction, validation, and automated reporting.

> [!NOTE]
> Confidence scores for tables, and table cells are available with the Preview version for general documents


<!--Please let me know if this is copilot/AI, preview or GA.-->

## Use a quick test to retrieve the Confidence score value from the selected table

You can check the confidence score of a table by performing a predict in a quick test
1.	Sign in to https://make.powerautomate.com
2.	On the left pane, select AI hub, select AI models
3.	Select <your_model>, select Quick test, select Upload from my device, select <your_file>

Place your cursor over the relevant area of the table to view its confidence score.

<screenshot>

Select the table to view its confidence score.

<screenshot>

## Use Confidence score in a cloud flow


## Use the formula bar to retrieve the Confidence score value from the selected item in the Form Processor  control in Power Apps

In this example I have chosen to extract tabular information from my document with a Table that I named 'Table invoice' with 4 columns 'Item', 'Quantity', 'Rate' and 'Amount'

Here’s some examples

This expression retrieves the confidence value of the amount from the first row of the invoice table in the results of FormProcessor1.

```power-fx
First(FormProcessor1.Results.'Table invoice').Amount.Confidence
```

This expression retrieves the confidence value from the first item in the results of the `FormProcessor1` and multiplies it by 100 to convert it to a percentage format.

```power-fx
First(FormProcessor1.Results.'Table invoice').Item.Confidence *100
```

This expression concatenates the rounded confidence values of amounts in the invoice table, appending a percentage sign and a newline character after each value.

```power-fx
Concat(FormProcessor1.Results.'Table invoice', Round(Amount.Confidence * 100,2) & "%", Char(10))
```

## Common questions

Q: Is it possible to see a confidence score for tables in Fixed templates document?
A: Confidence score for tables are only available for general documents.

Q: Is it possible to see a confidence score of a multipage table?
A: Yes

Q: Is it possible to see a confidence score for rows in a table?
A: We do not provide this information


Q: What can I do if I have a low confidence score for a cell, table?
1.	Check that the table is tagged correctly in all the documents.
2.	Provide more sample documents for training where the table is present


Related information
Use a document processing model in Power Automate
Use the form processor component in Power Apps

