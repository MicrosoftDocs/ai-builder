---
title: Language detection prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the language detection prebuilt AI models that are available in AI Builder.
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Preview: Text recognition model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The prebuilt text recognition model can be used to extract recognized words from documents and images into machine-readable character streams. It uses state-of-the-art optical character recognition (OCR) to detect embedded printed and handwritten text.

This prebuilt processes images and document files to extract lines of printed or handwritten text.

## Use in Power Apps

The text recognition prebuilt model is available in Power Apps by using the text recognizer component. For more information, see [Text recognizer component in Power Apps](prebuilt-text-recognizer-component-in-powerapps.md).

## Use in Power Automate

For information about how to use text recognition prebuilt model in Power Automate, see [Use text recognition model in Power Automate](flow-text-recognition.md).  

## Supported language, format and size

The documents you can scan with the text recognition model need these characteristics:

- **Language**: English
- **Format**:
    - JPG
    -.png
    - BMP
    - PDF
    - TIFF
- **Size**: 20 MB maximum

## Model output

If a document is detected, the text recognition model will output the following information:

- **Results**: A list of lines extracted from the input text.
- **Text**: Strings containing the line of text detected.
- **BoundingBox**: Four values representing the bounding box, described using the top and left positions along with its width and height.
