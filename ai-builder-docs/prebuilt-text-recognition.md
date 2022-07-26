---
title: Text recognition prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the text recognition prebuilt AI models that are available in AI Builder.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 03/29/2021
ms.author: alanab
ms.reviewer: angieandrews
---

# Text recognition prebuilt model

The text recognition prebuilt model extracts words from documents and images into machine-readable character streams. It uses state-of-the-art optical character recognition (OCR) to detect printed and handwritten text in images.

This model processes images and document files to extract lines of printed or handwritten text.

## Use in Power Apps

The text recognition prebuilt model is available in Power Apps by using the text recognizer component. More information: [Use the text recognizer component in Power Apps](prebuilt-text-recognizer-component-in-powerapps.md)

## Use in Power Automate

For information about how to use this model in Power Automate, see [Use the text recognition prebuilt model in Power Automate](flow-text-recognition.md).

## Supported language, format, and size

The files you can scan with the text recognition model must have these characteristics:

- **Language for print text**: Afrikaans, Albanian, Angika (Devanagiri), Arabic, Asturian, Awadhi-Hindi (Devanagiri), Azerbaijani (Latin), Bagheli, Basque, Belarusian (Cyrillic), Belarusian (Latin), Bhojpuri-Hindi (Devanagiri), Bislama, Bodo (Devanagiri), Bosnian (Latin), Brajbha, Breton, Bulgarian, Bundeli, Buryat (Cyrillic), Catalan, Cebuano, Chamling, Chamorro, Chhattisgarhi (Devanagiri), Chinese (Simplified), Chinese (Traditional), Cornish, Corsican, Crimean Tatar (Latin), Croatian, Czech, Danish, Dari, Dhimal (Devanagiri), Dogri (Devanagiri), Dutch, English, Erzya (Cyrillic), Estonian, Faroese, Fijian, Filipino, Finnish, French, Friulian, Gagauz (Latin), Galician, German, Gilbertese, Gondi (Devanagiri), Greenlandic, Gurung (Devanagiri), Haitian Creole, Halbi (Devanagiri), Hani, Haryanvi, Hawaiian, Hindi, Hmong Daw (Latin), Ho(Devanagiri), Hungarian, Icelandic, Inari Sami, Indonesian, Interlingua, Inuktitut (Latin), Irish, Italian, Japanese, Jaunsari (Devanagiri), Javanese, Kabuverdianu, Kachin (Latin), Kangri (Devanagiri), Karachay-Balkar, Kara-Kalpak (Cyrillic), Kara-Kalpak (Latin), Kashubian, Kazakh (Cyrillic), Kazakh (Latin), Khaling, Khasi, K'iche', Korean, Korku, Koryak, Kosraean, Kumyk (Cyrillic), Kurdish (Arabic), Kurdish (Latin), Kurukh (Devanagiri), Kyrgyz (Cyrillic), Lakota, Latin, Lithuanian, Lower Sorbian, Lule Sami, Luxembourgish, Mahasu Pahari (Devanagiri), Malay (Latin), Maltese, Malto (Devanagiri), Manx,	Maori, Marathi, Mongolian (Cyrillic), Montenegrin (Cyrillic), Montenegrin (Latin), Neapolitan, Nepali, Niuean, Nogay, Northern Sami (Latin), Norwegian, Occitan, Ossetic, Pashto, Persian, Polish, Portuguese, Punjabi (Arabic), Ripuarian, Romanian, Romansh, Russian, Sadri (Devanagiri), Samoan (Latin), Sanskrit (Devanagari), Santali (Devanagiri), Scots, Scottish Gaelic, Serbian (Latin), Sherpa (Devanagiri), Sirmauri (Devanagiri), Skolt Sami, Slovak, Slovenian, Somali (Arabic), Southern Sami, Spanish, Swahili (Latin), Swedish, Tajik (Cyrillic), Tatar (Latin), Tetum, Thangmi, Tongan, Turkish, Turkmen (Latin), Tuvan, Upper Sorbian, Urdu, Uyghur (Arabic), Uzbek (Arabic), Uzbek (Cyrillic), Uzbek (Latin), Volapük, Walser, Welsh, Western Frisian, Yucatec Maya, Zhuang, Zulu
- **Language for handwritten text**: English, Chinese (Simplified), French, German, Italian, Japanese, Korean, Portuguese, Spanish
- **Format**:
  - JPG
  - PNG
  - BMP
  - PDF
- **Size**: 50 MB maximum
- For PDF documents, only the first 2,000 pages are processed.

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
