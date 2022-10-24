---
title: Requirements and limitations for document processing models - AI Builder | Microsoft Docs
description: Describes the requirements and limitations of document processing models in AI Builder.
author: JoeFernandezMS
ms.topic: conceptual
ms.custom:
ms.date: 10/07/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# Requirements and limitations for a document processing model

## Languages supported

The following languages are supported when training a document processing model and selecting **Structured and semi-structured documents** as document type: Afrikaans, Albanian, Angika (Devanagari), Arabic, Asturian, Awadhi-Hindi (Devanagari), Azerbaijani (Latin), Bagheli, Basque, Belarusian (Cyrillic), Belarusian (Latin), Bhojpuri-Hindi (Devanagari), Bislama, Bodo (Devanagari), Bosnian (Latin), Brajbha, Breton, Bulgarian, Bundeli, Buryat (Cyrillic), Catalan, Cebuano, Chamling, Chamorro, Chhattisgarhi (Devanagari), Chinese Simplified, Chinese Traditional, Cornish, Corsican, Crimean Tatar (Latin), Croatian, Czech, Danish, Dari, Dhimal (Devanagari), Dogri (Devanagari), Dutch, English, Erzya (Cyrillic), Estonian, Faroese, Fijian, Filipino, Finnish, French, Friulian, Gagauz (Latin), Galician, German, Gilbertese, Gondi (Devanagari), Greenlandic, Gurung (Devanagari), Haitian Creole, Halbi (Devanagari), Hani, Haryanvi, Hawaiian, Hindi, Hmong Daw (Latin), Ho(Devanagiri), Hungarian, Icelandic, Inari Sami, Indonesian, Interlingua, Inuktitut (Latin), Irish, Italian, Japanese, Jaunsari (Devanagari), Javanese, Kabuverdianu, Kachin (Latin), Kangri (Devanagari), Karachay-Balkar, Kara-Kalpak (Cyrillic), Kara-Kalpak (Latin), Kashubian, Kazakh (Cyrillic), Kazakh (Latin), Khaling, Khasi, K'iche', Korean, Korku, Koryak, Kosraean, Kumyk (Cyrillic), Kurdish (Arabic), Kurdish (Latin), Kurukh (Devanagari), Kyrgyz (Cyrillic), Lakota, Latin, Lithuanian, Lower Sorbian, Lule Sami, Luxembourgish, Mahasu Pahari (Devanagari), Malay (Latin), Maltese, Malto (Devanagari), Manx, Maori, Marathi, Mongolian (Cyrillic), Montenegrin (Cyrillic), Montenegrin (Latin), Neapolitan, Nepali, Niuean, Nogay, Northern Sami (Latin), Norwegian, Occitan, Ossetic, Pashto, Persian, Polish, Portuguese, Punjabi (Arabic), Ripuarian, Romanian, Romansh, Russian, Sadri  (Devanagari), Samoan (Latin), Sanskrit (Devanagari), Santali(Devanagiri), Scots, Scottish Gaelic, Serbian (Latin), Sherpa (Devanagari), Sirmauri (Devanagari), Skolt Sami, Slovak, Slovenian, Somali (Arabic), Southern Sami, Spanish, Swahili (Latin), Swedish, Tajik (Cyrillic), Tatar (Latin), Tetum, Thangmi, Tongan, Turkish, Turkmen (Latin), Tuvan, Upper Sorbian, Urdu, Uyghur (Arabic), Uzbek (Arabic), Uzbek (Cyrillic), Uzbek (Latin), Volapük, Walser, Welsh, Western Frisian, Yucatec Maya, Zhuang, Zulu

The following language is supported when training a document processing model and selecting **Unstructured and free-form documents** as document type: English

## Requirements

Document processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- TIFF files can't be used for training. You'll need to use documents in PDF, JPG or PNG format to train a model. Once the model has been trained, it can extract data from TIFF files when the model is used in a Power Automate cloud flow.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- Maximum document size to process must not exceed 20 MB. 
- For images, dimensions must be between 50 &times; 50 and 10,000 &times; 10,000 pixels.
- If scanned from paper documents, scans should be high-quality images.
- You can create up to 200 collections per model when selecting structured and semi-structured as document type, and an unlimited number of collections for unstructured documents.

 > [!NOTE]
 > Extracting signatures from documents is currently not supported.<br />
 > Fields that split across page boundaries are currently not supported.

## Optimization tip

Learn how to [improve the performance of document processing models](improve-form-processing-performance.md).

## Next step

[Create a form-processing model](create-form-processing-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
