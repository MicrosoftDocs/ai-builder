---
title: Interpret confidence score for tables and table cells
description: Learn how to interpret the confidence score for tables and table cells.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: how-to
ms.collection: 
- bap-ai-copilot
ms.date: 09/08/2025
ms.update-cycle: 180-days
ms.author: plarrue
ms.reviewer: angieandrews
---

# Interpret confidence score for tables and table cells

A confidence score for tables and cells in general documents quantifies how certain the model is about its predictions of structured data. Higher scores indicate greater confidence, and lower scores suggest uncertainty. These scores help prioritize reliable outputs, guide human review, and improve accuracy in applications like data extraction, validation, and automated reporting.

Confidence scores for tables and table cells are available for general documents.

## Use a quick test to retrieve the confidence score value of a table and table cells

You can check the confidence score of a table and table cells by performing a predict in a quick test.

1. Sign in to [Power Automate](https://make.powerautomate.com) or [Power Apps](https://make.powerapps.com).
1. On the left pane, select **... More** > **AI hub** > **AI models**.
1. Select ***<your_model>***.
1. Select **Quick test** > **Upload from my device**.
1. Select ***<your_file>***.

To view its confidence score, place your cursor over the relevant area of the table.

:::image type="content" source="media/interpret-confidence-score/quick-test-confidence-score-table.png" alt-text="Screenshot of a quick test showing the confidence score of a table.":::

Select the table to view cells confidence score.

:::image type="content" source="media/interpret-confidence-score/quick-test-confidence-score-table-cells.png" alt-text="Quick test showing the confidence score of cells in a table.":::

## Use the confidence score in a cloud flow

You can check the confidence score of a table and table cells by performing a predict in a cloud flow.

1. Select **+ Create** > **Instant cloud flow**.
1. Select **Manually trigger a flow** > **Create**.
1. Select the action **Manually trigger a flow** > **+ Add an input** > **File** > **Add an action**.
1. Select **AI Builder** > **Extract information from documents**.
1. In the **AI Model** field, select ***<your_published_model>***.
1. In the **Form type** field, select your type (JPEG image, PDF document, PNG image).
1. In the **Form** field, select **File content contentBytes** from the **Dynamic content** list.
1. Select **Add an action**.
1. Search **Compose (Data operation)**.
1. In the **Inputs** field, select the confidence score value you want extracted from the **Dynamic content** list.

    :::image type="content" source="media/interpret-confidence-score/document-processing-predict-confidence-score_cloud-flow.png" alt-text="Screenshot of predict showing the confidence score of cells and table in a cloud flow.":::

    To view the confidence score of the table and cells, test your cloud flow.

    :::image type="content" source="media/interpret-confidence-score/document-processing-predict-confidence-score-cloud-flow-result.png" alt-text="Predict showing the confidence score result of cells and table in a cloud flow.":::

    To view the confidence score results for other cells, select the next arrow (**>**) in the **Apply to Each** action. The table's confidence score remains unchanged in this scenario.

## Use the confidence score in a canvas app

To retrieve the confidence score value from the form processor control in Power Apps, use the formula bar.

The following example shows tabular information to be extracted from a document with a table named `Table 1` with three columns: `Item`, `Qty`, and `Amount`.

### Examples

This expression retrieves the confidence score value of the first row in the `Amount` column of the table `Table 1` in the results of **FormProcessor1**.

````power-fx
First(FormProcessor1.Results.'Table 1').Amount.Confidence
````

This expression retrieves the confidence score value of the first row in the `Qty` column of the table `Table 1` in the results of **FormProcessor1**, and multiplies it by 100 to convert it to a percentage format.

```power-fx
First(FormProcessor1.Results.'Table 1').Qty.Confidence *100
```

This expression concatenates the confidence score result for all rows in the `Amount` column of the table `Table 1`, appending a percentage sign and a newline character after each value.

```power-fx
Concat(FormProcessor1.Results.'Table 1', Round(Amount.Confidence * 100,2) & "%", Char(10))
```

## FAQ

The following are frequently asked questions about confidence scores for tables and table cells.

### How is the confidence score calculated?

The confidence score is calculated based on data characteristics observed in the training samples, such as how frequently this field has corresponding value present, and the specific document used during prediction. Some properties are dataset specific, while others are field specific. These properties are then utilized to calculate confidence scores for each field.

### Is it possible to get a confidence score for tables in fixed templates documents?

The confidence score for tables is available only for general documents.

### Is it possible to get a confidence score of a multipage table?

Yes.

### Can I get the confidence score of a table with column type text, number, date, and checkbox?

Yes, you can get the confidence score of these text data types.

### Is it possible to get a confidence score for rows in a table?

We don't provide this information.

### Is it possible to get a confidence score of a table in an app in Power Apps?

Currently, we don't provide a confidence score for an entire table; however, we do offer confidence scores for individual cells.

### What can I do if I have a low confidence score for a cell, table?

1. Check that the table is tagged correctly in all the documents.
1. Provide more sample documents for training where the table is present. Check [Best practices](form-processing-faq.md#best-practices).

## Related information

- [Use a document processing model in Power Automate](form-processing-model-in-flow.md)
- [Use the form processor component in Power Apps](form-processor-component-in-powerapps.md)

