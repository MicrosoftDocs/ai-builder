---
title: Text recognition prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the text recognition prebuilt AI models that are available in AI Builder.
author: alanabrito
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/29/2021
ms.author: alanab
ms.reviewer: v-aangie
---

# Text recognition prebuilt model

The text recognition prebuilt model extracts words from documents and images into machine-readable character streams. It uses state-of-the-art optical character recognition (OCR) to detect printed and handwritten text in images.

This model processes images and document files to extract lines of printed or handwritten text.

## Use in Power Apps

The text recognition prebuilt model is available in Power Apps by using the text recognizer component. More information: [Use the text recognizer component in Power Apps](prebuilt-text-recognizer-component-in-powerapps.md)

## Use in Power Automate

For information about how to use this model in Power Automate, see [Use the text recognition prebuilt model in Power Automate](flow-text-recognition.md).

## Supported languages, format, and size

The files you can scan with the text recognition model must have these characteristics:

- **Language**: Dutch, English, French, German, Italian, Portuguese, Spanish
- **Format**:
  - JPG
  - PNG
  - BMP
  - PDF
- **Size**: 20 MB maximum

## Model output

If a document is detected, the text recognition model outputs the following information:

- **Results**: A list of lines extracted from the input text.
- **Text**: Strings containing the line of text detected.
- **BoundingBox**: Four values representing the bounding box, described by using the top and left positions along with its width and height.

## Limits

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Text recognition calls (per environment)|480|60 seconds|


[!INCLUDE[footer-include](includes/footer-banner.md)]