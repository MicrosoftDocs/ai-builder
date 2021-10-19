---
title: Requirements and limitations for form processing models - AI Builder | Microsoft Docs
description: Describes the requirements and limitations of form processing models in AI Builder.
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom:
ms.date: 10/06/2021
ms.author: jofernan
ms.reviewer: v-aangie
---

# Requirements and limitations for a form processing model

## Languages supported

English

## Requirements

Form processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- The combined file size of the documents used for training per collection must not exceed 50 MB. 
- For images, dimensions must be between 50 &times; 50 and 10,000 &times; 10,000 pixels.
- For PDF files, dimensions must be at most 17 x 17 inches, corresponding to Legal or A3 paper sizes and smaller.
- If scanned from paper documents, scans should be high-quality images.

 > [!NOTE]
 > AI Builder doesn't currently support the following types of form processing input data:
 >
 > - Signatures

## Optimization tips

Learn how to [improve the performance of form processing models](improve-form-processing-performance.md).


### Next step

[Create a form-processing model](create-form-processing-model.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
