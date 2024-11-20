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

# Interpret confidence score for tables and table cells (Preview)

A confidence score for tables and cells in general documents quantifies how certain the model is about its predictions on structured data. Higher scores indicate greater confidence, while lower scores suggest uncertainty. These scores help prioritize reliable outputs, guide human review, and improve accuracy in applications like data extraction, validation, and automated reporting.

> [!NOTE]
> Confidence scores for tables and table cells are available in the Preview version for general documents


<!--Please let me know if this is copilot/AI, preview or GA.-->

## Use a quick test to retrieve the Confidence score value from the selected table

You can check the confidence score of a table by performing a predict in a quick test
1.	Sign in to **https://make.powerautomate.com**
2.	On the left pane, select **AI hub,** select **AI models**
3.	Select **<your_model>**, select **Quick test**, select **Upload from my device**, select **<your_file>**

Place your cursor over the relevant area of the table to view its confidence score.

:::image type="content" source="media/quick_test_confidence_score_table.png" alt-text="Quick test showing the confidence score of a table.":::

Select the table to view cells confidence score.

:::image type="content" source="media/quick_test_confidence_score_table_cells.png" alt-text="Quick test showing the confidence score of cells in a table.":::

## Use Confidence score in a cloud flow

1.	Select **+ Create**
2.	Select **Instant cloud flow**
3.	Select **Manually trigger a flow**
4.	Select the action Manually trigger a flow
5.	Select **+ Add an input**, select **File**
6.	Select **+ New step**
7.	Select **AI Builder**, select **Extract information from documents**
8.	In **AI Model**, select **<your_model>**
9.	In **Form type,** select your type, PDF, JPEG, PNG
10.	in **Form**, select **File conten**t from the Dynamic content list
11.	Select **+ New step**
12.	Search **Compose (Data operation)**
13.	in **Input**, select the confidence score value you want to see extracted


## Use the formula bar to retrieve the Confidence score value from the selected item in the Form Processor  control in Power Apps

In this example I have chosen to extract tabular information from my document with a Table that I named 'Table 1' with 4 columns 'Item', 'Qty'and 'Amount'.

Here’s some examples

This expression retrieves the confidence value of the amount from the first row of the invoice table in the results of FormProcessor1.

```power-fx
First(FormProcessor1.Results.'Table 1').Amount.Confidence
```

This expression retrieves the confidence value from the first item in the results of the `FormProcessor1` and multiplies it by 100 to convert it to a percentage format.

```power-fx
First(FormProcessor1.Results.'Table 1').Rate.Confidence *100
```

This expression concatenates the rounded confidence values of amounts in the invoice table, appending a percentage sign and a newline character after each value.

```power-fx
Concat(FormProcessor1.Results.'Table 1', Round(Amount.Confidence * 100,2) & "%", Char(10))
```

## Common questions

Q: Is it possible to see a confidence score for tables in Fixed templates document?
A: Confidence score for tables are only available for general documents.

Q: Is it possible to see a confidence score of a multipage table?
A: Yes.

Q: Can i see the confidence score of a table with column type text, Number, Date and Checkbox?
A: Yes, you can see the confidence score of these text data type.

Q: Is it possible to see a confidence score for rows in a table?
A: We do not provide this information.

Q: Is it possible to see a confidence score of a table in a Power app?
A: We do not provide a confidence score for an entire table; however we provide confidence scores for individual cells.

Q: What can I do if I have a low confidence score for a cell, table?
1.	Check that the table is tagged correctly in all the documents.
2.	Provide more sample documents for training where the table is present.


Related information
Use a document processing model in Power Automate
Use the form processor component in Power Apps

