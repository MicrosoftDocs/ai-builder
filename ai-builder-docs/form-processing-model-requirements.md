---
title: Requirements and limitations for document processing models - AI Builder | Microsoft Docs
description: Describes the requirements and limitations of document processing models in AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom:
ms.date: 05/31/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# Requirements and limitations for a document processing model

## Languages supported

The following languages are supported when training a document processing model and selecting **Structured and semi-structured documents** as document type: Afrikaans, Albanian, Asturian, Basque, Bislama, Breton, Catalan, Cebuano, Chamorro, Chinese (Simplified), Chinese (Traditional), Cornish, Corsican, Crimean Tatar (Latin), Czech, Danish, Dutch, English, Estonian, Fijian, Filipino, Finnish, French, Friulian, Galician, German, Gilbertese, Greenlandic, Haitian Creole, Hani, Hmong Daw (Latin), Hungarian, Indonesian, Interlingua, Inuktitut (Latin), Irish, Italian, Japanese, Javanese, K’iche’, Kabuverdianu, Kachin (Latin), Kara-Kalpak, Kashubian, Khasi, Korean, Kurdish (latin), Luxembourgish, Malay (Latin), Manx, Neapolitan, Norwegian, Occitan, Polish, Portuguese, Romansh, Scots, Scottish Gaelic, Slovenian, Spanish, Swahili (Latin), Swedish, Tatar (Latin), Tetum, Turkish, Upper Sorbian, Uzbek (Latin), Volapük, Walser, Western Frisian, Yucatec Maya, Zhuang, Zulu.

The following language is supported when training a document processing model and selecting **Unstructured and free-form documents** as document type: English

## Requirements

Document processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- TIFF files cannot be used for training. You will need to use documents in PDF, JPG or PNG format to train a model. Once the model has been trained, it can extract data from TIFF files when the model is used in a Power Automate cloud flow.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- The combined file size of the documents used for training per collection must not exceed 50 MB. 
- For images, dimensions must be between 50 &times; 50 and 10,000 &times; 10,000 pixels.
- If scanned from paper documents, scans should be high-quality images.
- You can create up to 200 collections per model when selecting structured and semi-structured as document type, and unlimited number of collections for unstructured documents.

 > [!NOTE]
 > Extracting signatures from documents is currently not supported.<br />
 > Fields that split across page boundaries are currently not supported.

## Optimization tips

Learn how to [improve the performance of document processing models](improve-form-processing-performance.md).

## Next step

[Create a form-processing model](create-form-processing-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
