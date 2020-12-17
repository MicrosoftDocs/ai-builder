---
title: Requirements and limitations - AI Builder | Microsoft Docs
description: Describes the requirements and limitations of form processing models in AI Builder.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Form processing model requirements and limitations

## Languages supported

Currently form processing works with documents in **English**.  

## Requirements

Form processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- The combined file size of the documents used for training per collection must not exceed 50 MB, and PDF documents shouldn't have more than 500 pages. 
- For images, dimensions must be between 50 &times; 50 and 10000 &times; 10000 pixels.
- For PDF files, dimensions must be at most 17 x 17 inches, corresponding to Legal or A3 paper sizes and smaller.
- If scanned from paper documents, scans should be high-quality images.
- Must use the Latin alphabet (English characters).

 > [!NOTE]
 > AI Builder doesn't currently support the following types of form processing input data:
 >
 > - Complex tables (nested tables, merged headers or cells, and so on)
 > - Check boxes or radio buttons
 > - Signatures
 > - Fillable PDFs 

## Optimization tips

Learn how to [improve the performance of form processing models](improve-form-processing-performance.md).


### Next step

[Create a form-processing model](create-form-processing-model.md)
