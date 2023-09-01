---
title:  Feature availability by region or US Government environment
description: Learn which AI Builder features are available in each region or US Government environment. Lists the release status for each feature by region or US Government environment.
author: JoeFernandezMS
contributors:
  - xiao-wang-paris
  - phil-cmd
  - JoeFernandezMS
  - jekom1
  - v-aangie
  - antode
ms.topic: conceptual
ms.custom: 
ms.date: 05/26/2023
ms.author: jofernan
ms.reviewer: angieandrews
---

# Feature availability by region

AI Builder was initially released in Europe and the United States. Other regions continue to be added; however, the availability and release status of AI Builder features vary by location.

## Which region does my AI Builder subscription belong to?

Your AI Builder models are deployed in the region that hosts your Microsoft Power Platform environment. For example, if your environment is created in the Europe region, your AI Builder models are deployed in data centers in Europe and are subject to the availability status for Europe.  

## Availability and release status of features by region

The following tables show which AI Builder features are available in each region, and the release status (general availability or preview) for each feature. A dash (-) indicates that the feature isn't available.

> [!NOTE]
> For a view of what's planned for AI Builder, including new features, release status, and regional availability, go to the [AI Builder release plans](/power-platform-release-plan/2020wave1/ai-builder/).

### Custom models

|Feature |Asia |Australia |Canada |Europe |France |Germany |India |Japan |Norway |South Africa |South America |South Korea |Switzerland |United Arab Emirates |United Kingdom |United States |
|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
|Prediction|GA|GA|GA|GA| GA|GA|GA|GA|-|-|GA|-|GA|GA|GA|GA|
|Category classification|GA|GA|GA|GA| GA|GA|GA|GA|-|-|GA|-|GA|GA|GA|GA|
|Entity extraction |GA|GA|GA|GA| GA|GA|GA|GA|-|-|GA|-|GA|GA|GA|GA|
|Object detection|GA|GA|-|GA| -|-|GA|GA| -|-|-|-|-|-|GA|GA|
|Document processing (for structured and semi-structured documents)  |GA|GA|GA|GA| GA|GA|GA|GA| GA|GA|GA| GA|GA|GA|GA|GA|
|Document processing (for unstructured documents) |GA|GA|GA|GA|GA|-|GA|GA|-|-|GA|-| -|-|GA|GA|

### Prebuilt models

|Feature |Asia |Australia |Canada |Europe |France |Germany |India |Japan |Norway |South Africa |South America |South Korea |Switzerland |United Arab Emirates |United Kingdom |United States |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
|Business card reader    |GA|GA|GA|GA| GA|GA|GA|GA| GA|GA|GA| GA|GA|GA|GA|GA|
|Category classification |GA |GA |GA |GA |GA |GA |GA |GA  |-|-|GA |-|GA |GA |GA |GA |
|Entity extraction |GA |GA |GA |GA |GA|GA|GA|-|-|-|GA|-|GA |GA |GA |GA |
|Identity document reader |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Invoice processing |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Key phrase extraction |GA|GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Language detection |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Receipt processing |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Sentiment analysis |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Text recognition   |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |GA |
|Text translation |- |- |- |GA |-|- |-|- |-|-|-|-|- |- |- |GA |

## US Government

AI Builder is available in US Government environments with the features listed in the following tables. A dash (-) indicates that the feature isn't available.

> [!NOTE]
> For more information on the Power Platform US Government environments and features, see these topics:
> - [Power Apps US Government](/power-platform/admin/powerapps-us-government)
> - [Power Automate US Government](/power-automate/us-govt)

### Custom models
|Feature |Government Community Cloud (GCC) |Government Community Cloud – High (GCC High) |Department of Defense (DoD) |
|:-------|:-------:|:-------:|:-------:|
|Prediction|GA|GA|-|
|Category classification|GA|GA|-|
|Entity extraction|GA|GA|-|
|Object detection|GA|GA|-|
|Document processing (for structured and semi-structured documents) |GA|GA|-|
|Document processing (for unstructured documents) |GA|GA|-|

### Prebuilt models
|Feature |Government Community Cloud (GCC) |Government Community Cloud – High (GCC High) |Department of Defense (DoD) |
|:-------|:-------:|:-------:|:-------:|
|Business card reader    |GA|GA|-|
|Category classification |Preview|Preview|-|
|Entity extraction |GA|GA|-|
|Identity document reader |GA|GA|-|
|Invoice processing |GA|GA|-|
|Key phrase extraction |GA|GA|-|
|Language detection |GA|GA|-|
|Receipt processing |GA|GA|-|
|Sentiment analysis |GA|GA|-|
|Text recognition   |GA|GA|-|
|Text translation   |GA|GA|-|

### US Government feature limitations

The following features available in the commercial version of AI Builder aren't available to US Government customers:

- 30-day user trials
- AI model copy across cloud boundaries (for example between Public and GCC or between GCC and GCC High)
- [Document Automation](doc-automation.md) isn't available in GCC and GCC High

For more information about other limitations of Power Platform US Government, go to these topics: 

- [Power Apps US Government feature limitations](/power-platform/admin/powerapps-us-government#power-apps-us-government-feature-limitations)
- [Power Automate US Government feature limitations](/power-automate/us-govt#power-automate-us-government-feature-limitations)

### See also

[AI model types](model-types.md)


