---
title: Requirements and limitations for document processing models - AI Builder
description: Learn about the requirements and limitations of document processing models in AI Builder.
author: JoeFernandezMS
contributors:
  - Phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom:
ms.date: 04/11/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Requirements and limitations for a document processing model

## Languages supported

### Model for Fixed-template documents

The following languages are supported when training a document processing model and selecting **Fixed-template documents** as document type:

Abaza, Abkhazian, Achinese, Acoli, Adangme, Adyghe, Afar, Afrikaans, Akan, Albanian, Algonquin, Angika (Devanagari), Arabic, Asturian, Asu (Tanzania), Avaric, Awadhi-Hindi (Devanagari), Aymara, Azerbaijani (Latin), Bafia, Bagheli, Bambara, Bashkir, Basque, Belarusian (Cyrillic), Belarusian (Latin), Bemba (Zambia), Bemba (Zambia), Bhojpuri-Hindi (Devanagari), Bikol, Bini, Bislama, Bodo (Devanagari), Bosnian (Latin), Brajbha, Breton, Bulgarian, Bundeli, Buryat (Cyrillic), Catalan, Cebuano, Chamling, Chamorro, Chechen, Chhattisgarhi (Devanagari), Chiga, Chinese Simplified, Chinese Traditional, Choctaw, Chukot, Chuvash, Cornish, Corsican, Cree, Creek, Crimean Tatar (Latin), Croatian, Crow, Czech, Danish, Dargwa, Dari, Dhimal (Devanagari), Dogri (Devanagari), Duala, Dungan, Dutch, Efik, English, Erzya (Cyrillic), Estonian, Faroese, Fijian, Filipino, Finnish, Fon, French, Friulian, Ga, Gagauz (Latin), Galician, Ganda, Gayo, German, Gilbertese, Gondi (Devanagari), Greek, Greenlandic, Guarani, Gurung (Devanagari), Gusii, Haitian Creole, Halbi (Devanagari), Hani, Haryanvi, Hawaiian, Hebrew, Herero, Hiligaynon, Hindi, Hmong Daw (Latin), Ho (Devanagiri), Hungarian, Iban, Icelandic, Igbo, Iloko, Inari Sami, Indonesian, Ingush, Interlingua, Inuktitut (Latin), Irish, Italian, Japanese, Jaunsari (Devanagari), Javanese, Jola-Fonyi, Kabardian, Kabuverdianu, Kachin (Latin), Kalenjin, Kalmyk, Kangri (Devanagari), Kanuri, Karachay-Balkar, Kara-Kalpak (Cyrillic), Kara-Kalpak (Latin), Kashubian, Kazakh (Cyrillic), Kazakh (Latin), Khakas, Khaling, Khasi, K'iche', Kikuyu, Kildin Sami, Kinyarwanda, Komi, Kongo, Korean, Korku, Koryak, Kosraean, Kpelle, Kuanyama, Kumyk (Cyrillic), Kurdish (Arabic), Kurdish (Latin), Kurukh (Devanagari), Kyrgyz (Cyrillic), Lak, Lakota, Latin, Latvian, Lezghian, Lingala, Lithuanian, Lower Sorbian, Lozi, Lule Sami, Luo (Kenya and Tanzania), Luxembourgish, Luyia	luy, Macedonian, Machame, Madurese, Mahasu Pahari (Devanagari), Makhuwa-Meetto, Makonde, Malagasy, Malay (Latin), Maltese, Malto (Devanagari), Mandinka, Manx, Maori, Mapudungun, Marathi, Mari (Russia), Masai, Mende (Sierra Leone), Meru, Meta', Minangkabau, 
Mohawk, Mongolian (Cyrillic), Mongondow, Montenegrin (Cyrillic), Montenegrin (Latin), Morisyen, Mundang, Nahuatl, Navajo, Ndonga, Neapolitan, Nepali, Ngomba, Niuean, Nogay, North Ndebele, Northern Sami (Latin), Norwegian, Nyanja, Nyankole, Nzima, Occitan, Ojibwa, Oromo, Ossetic, Pampanga, Pangasinan, Papiamento, Pashto, Pedi, Persian, Polish, Portuguese, Punjabi (Arabic), Quechua, Ripuarian, Romanian, Romansh, Rundi, Russian, Rwa, Sadri  (Devanagari), Sakha, Samburu, Samoan (Latin), Sango, Sangu (Gabon), Sanskrit (Devanagari), Santali(Devanagiri), Scots, Scottish Gaelic, Sena, Serbian (Cyrillic), Serbian (Latin), Shambala, Sherpa (Devanagari), Shona, Siksika, Sirmauri (Devanagari), Skolt Sami, Slovak, Slovenian, Soga, Somali (Arabic), Somali (Latin), Songhai, South Ndebele, Southern Altai, Southern Sami, Southern Sotho, Spanish, Sundanese, Swahili (Latin), Swati, Swedish, Tabassaran, Tachelhit, Tahitian, Taita, Tajik (Cyrillic), Tamil, Tatar (Cyrillic), Tatar (Latin), Teso, Tetum, Thai, Thangmi, Tok Pisin, Tongan, Tsonga, Tswana, Turkish, Turkmen (Latin), Tuvan, Udmurt, Uighur (Cyrillic), Ukrainian, Upper Sorbian, Urdu, Uyghur (Arabic), Uzbek (Arabic), Uzbek (Cyrillic), Uzbek (Latin), Vietnamese, Volapük, Vunjo, Walser, Welsh, Western Frisian, Wolof, Xhosa, Yucatec Maya, Zapotec, Zarma, Zhuang, Zulu

### Model for General documents

The following languages are supported when training a document processing model and selecting **General documents** as document type.

Afrikaans, Albanian, Arabic, Bulgarian, Chinese (Han (Simplified variant)), Chinese (Han (Traditional variant)), Croatian, Czech, Danish, Dutch, Estonian, Finnish, French, German, Hebrew, Hindi, Hungarian, Indonesian, Italian, Japanese, Korean, Latvian, Lithuanian, Macedonian, Marathi, Modern Greek (1453-), Nepali (macrolanguage), Norwegian, Panjabi, Persian, Polish, Portuguese, Romanian, Russian, Slovak, Slovenian, Somali (Arabic), Somali (Latin), Spanish, Swahili (macrolanguage), Swedish, Tamil, Thai, Turkish, Ukrainian, Urdu, Vietnamese

## Requirements

Document processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text-embedded PDFs are better, because there won't be any errors in character extraction and location.
- TIFF files can't be used for training. You'll need to use documents in PDF, JPG or PNG format to train a model. Once the model has been trained, it can extract data from TIFF files when the model is used in a Power Automate cloud flow.
- If your PDFs are password-locked, you must remove the lock before submitting them.
- Maximum document size to process must not exceed 20 MB. 
- For images, dimensions must be between 50 &times; 50 and 10,000 &times; 10,000 pixels.
- If scanned from paper documents, scans should be high-quality images.
- You can create up to 200 collections per model.
- In a cloud flow, the limit of fields that can be tagged for document processing is 300.

> [!NOTE]
> - Extracting signatures from documents isn't currently supported.<br />
> - Fields that split across page boundaries aren't currently supported.<br />
> - Rows that break from one page to another aren't currently supported.

## Optimization tip

Learn how to [improve the performance of document processing models](improve-form-processing-performance.md).

## Next step

[Create a form-processing model](create-form-processing-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
