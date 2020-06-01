---
title: Requirements and limitations - AI Builder | Microsoft Docs
description: Describes the requirements and limitations of form processing models in AI Builder.
author: JoeFernandezMS
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Form-processing model requirements and limitations

## Requirements

Form processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- The combined file size of the documents used for training must not exceed 50 MB, and PDF documents shouldn't have more than 500 pages.
- For images, dimensions must be between 530 &times; 100 and 4200 &times; 4200 pixels.
- If scanned from paper documents, scans should be high-quality images.
- Must use the Latin alphabet (English characters).

## Optimization tips

- Use forms with different values in each field.
- When you create a new form-processing model, upload documents with the same layout where each document is a separate instance. For example, you might have invoices from the same provider, but each uploaded invoice is from a different month.
- If you're getting bad results or low confidence scores for certain fields, create a new form-processing model and upload more documents. The more documents you tag, the more AI Builder will learn how to better recognize the fields. 
- You can optimize PDF files by using the **Print** > **Print to PDF** option to select certain pages within your document.

 > [!NOTE]
 > AI Builder doesn't currently support the following types of form-processing input data:
 >
 > - Complex tables (nested tables, merged headers or cells, and so on)
 > - Check boxes or radio buttons
 > - Signatures
 > - Fillable PDFs 

### Next step

[Create a form-processing model](create-form-processing-model.md)
