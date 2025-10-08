---
title:  Feature availability by region 
description: Learn which AI Builder features are available in each region or US Government environment. Lists the release status for each feature by region or US Government environment.
author: Antoine2F
contributors:
  - Antoine2F
  - antrodfr
  - CedrickBellarosa
  - phil-cmd
  - chplanty
  - xiao-wang-paris
  - JoeFernandezMS
  - jekom1
  - v-aangie
  - antode
ms.topic: article
ms.date: 10/08/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Feature availability by region

AI Builder was initially released in Europe and the United States. Other regions continue to be added; however, the availability and release status of AI Builder features vary by location.

## Which region does my AI Builder subscription belong to?

Your AI Builder models are deployed in the region that hosts your Microsoft Power Platform environment. For example, if your environment is created in the Europe region, your AI Builder models are deployed in data centers in Europe and are subject to the availability status for Europe.  

## Availability and release status of features by region

The following tables show which AI Builder features are available in each region, and the release status (general availability or preview) for each feature. A dash (-) indicates that the feature isn't available.

### Prompts

In the following table, (GA) or (Preview) means that the feature is available but uses an Azure OpenAI service in another region. Learn more in [enabling data movement cross-regions](/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions).

| Feature                              | Asia        | Australia      | Canada         | Europe         | France         | Germany        | India         | Japan          | Norway         | Singapore      | South Africa   | South America  | Korea          | Sweden         | Switzerland    |United Arab Emirates|United Kingdom| United States  |
|--------------------------------------|-------------|----------------|----------------|----------------|----------------|----------------|---------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|--------------------|--------------|----------------|
| GPT-4.1 mini                         | GA          | GA             | (GA)           | (GA)           | (GA)           | (GA)           | GA            | (GA)           | (GA)           | GA             | (GA)           | (GA)           | (GA)           |  (GA)          | (GA)           | (GA)               | GA           | GA             |
| GPT-4.1                              | GA          | GA             | (GA)           | (GA)           | (GA)           | (GA)           | GA            | (GA)           | (GA)           | GA             | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)               | GA           | GA             |
| o3                                   | (GA)        | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)          | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)           | (GA)               |(GA)          | GA             |
| GPT-5 chat                          |      -       |       -         | -               | (Preview)      |  -             | -              |  -            |  -             |  -             |   -            |                |     -          |   -            | -              |  -             |  -                 |  -           | Preview        |
| GPT-5 reasoning      |  -          |  -             |   -            | (Preview)      |  -             |   -            |  -            |  -             |   -            | -              |  -             |   -            |  -             |   -            |   -            |   -                |              | Preview        |



### Custom models

| Feature                                            | Asia | Australia | Canada | Europe | France | Germany | India | Japan | Korea       | Norway | Singapore | South Africa | South America | Sweden | Switzerland | United Arab Emirates | United Kingdom | United States |
|----------------------------------------------------|------|-----------|--------|--------|--------|---------|-------|-------|-------------|--------|-----------|--------------|---------------|--------|-------------|----------------------|----------------|---------------|
| Prediction                                         | GA   | GA        | GA     | GA     | GA     | GA      | GA    | GA    | -           | -      | GA        | -            | GA            | GA     | GA          | GA                   | GA             | GA            |
| Category classification                            | GA   | GA        | GA     | GA     | GA     | GA      | GA    | GA    | -           | -      | -         | -            | GA            | GA     | GA          | GA                   | GA             | GA            |
| Entity extraction                                  | GA   | GA        | GA     | GA     | GA     | GA      | GA    | GA    | -           | -      | -         | -            | GA            | GA     | GA          | GA                   | GA             | GA            |
| Object detection                                   | GA   | GA        | -      | GA     | -      | -       | GA    | GA    | -           | -      | GA        | -            | -             | -      | -           | -                    | GA             | GA            |
| Document processing (for fixed-template documents) | GA   | GA        | GA     | GA     | GA     | GA      | GA    | GA    | GA          | GA     | GA        | GA           | GA            | GA     | GA          | GA                   | GA             | GA            |
| Document processing (for general documents)        | GA   | GA        | GA     | GA     | GA     | -       | GA    | GA    | -           | GA     | GA        | -            | GA            | -      | -           | -                    | GA             | GA            |

### Prebuilt models

| Feature                  | Asia    | Australia | Canada  | Europe  | France  | Germany | India   | Japan   | Korea   | Norway  | Singapore | South Africa | South America | Sweden  | Switzerland | United Arab Emirates | United Kingdom | United States |
|--------------------------|---------|-----------|---------|---------|---------|---------|---------|---------|---------|---------|-----------|--------------|---------------|---------|-------------|----------------------|----------------|---------------|
| Business card reader     | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Category classification  | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | -       | -       | -         | -            | GA            | GA      | GA          | GA                   | GA             | GA            |
| Entity extraction        | GA      | GA        | GA      | GA      | GA      | GA      | GA      | -       | -       | -       | -         | -            | GA            | GA      | GA          | GA                   | GA             | GA            |
| Identity document reader | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Image description        | Preview | Preview   | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview   | Preview      | Preview       | Preview | Preview     | Preview              | Preview        | Preview       |
| Contract processing        | Preview | Preview   | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview   | Preview      | Preview       | Preview | Preview     | Preview              | Preview        | Preview       |
| Health insurance card processing        | Preview | Preview   | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview | Preview   | Preview      | Preview       | Preview | Preview     | Preview              | Preview        | Preview       |
| Invoice processing       | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Key phrase extraction    | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Language detection       | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Receipt processing       | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Sentiment analysis       | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Text generation          | -       | -         | -       | -       | -       | -       | -       | -       | -       | -       | -         | -            | -             | -       | -           | -                    | -              | Preview       |
| Text recognition         | GA      | GA        | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA      | GA        | GA           | GA            | GA      | GA          | GA                   | GA             | GA            |
| Text translation         | -       | -         | -       | GA      | -       | -       | -       | -       | -       | -       | -         | -            | -             | -       | -           | -                    | -              | GA            |


## US Government

AI Builder is available in US Government environments with the features listed in the following tables. A dash (-) indicates that the feature isn't available.

> [!NOTE]
> Learn more about the Power Platform US Government environments and features in the following articles:
>
> - [Power Apps US Government](/power-platform/admin/powerapps-us-government)
> - [Power Automate US Government](/power-automate/us-govt)

### Prompts (US Government)

| Feature                                 | Government Community Cloud (GCC) | Government Community Cloud – High (GCC High) | Department of Defense (DoD) |
|:----------------------------------------|:--------------------------------:|:--------------------------------------------:|:---------------------------:|
| GPT-4o mini                             |               GA                 |                     GA                       |              -              |
| GPT-4o                                  |               GA                 |                     GA                       |              -              |
| GPT-4o using image or document as input |               -                  |                     -                        |              -              |
| o3                                      |               -                  |                     -                        |              -              |
| GPT-4.1 mini                            |               -                  |                     -                        |              -              |
| GPT-4.1                                 |               -                  |                     -                        |              -              |

### Custom models (US Government)

| Feature                                            | Government Community Cloud (GCC) | Government Community Cloud – High (GCC High) | Department of Defense (DoD) |
|:---------------------------------------------------|:--------------------------------:|:--------------------------------------------:|:---------------------------:|
| Prediction                                         |                GA                |                      GA                      |              -              |
| Category classification                            |                GA                |                      GA                      |              -              |
| Entity extraction                                  |                GA                |                      GA                      |              -              |
| Object detection                                   |                GA                |                      GA                      |              -              |
| Document processing (for fixed-template documents) |                GA                |                      GA                      |              -              |
| Document processing (for general documents)        |                GA                |                      GA                      |              -              |

### Prebuilt models (US Government)

| Feature                  | Government Community Cloud (GCC) | Government Community Cloud – High (GCC High) | Department of Defense (DoD) |
|:-------------------------|:--------------------------------:|:--------------------------------------------:|:---------------------------:|
| Business card reader     |                GA                |                      GA                      |              -              |
| Category classification  |             Preview              |                   Preview                    |              -              |
| Entity extraction        |                GA                |                      GA                      |              -              |
| Identity document reader |                GA                |                      GA                      |              -              |
| Invoice processing       |                GA                |                      GA                      |              -              |
| Key phrase extraction    |                GA                |                      GA                      |              -              |
| Language detection       |                GA                |                      GA                      |              -              |
| Receipt processing       |                GA                |                      GA                      |              -              |
| Sentiment analysis       |                GA                |                      GA                      |              -              |
| Text recognition         |                GA                |                      GA                      |              -              |
| Text translation         |                GA                |                      GA                      |              -              |

### US Government feature limitations

The following features available in the commercial version of AI Builder aren't available to US Government customers:

- 30-day user trials
- AI models copy across cloud boundaries (for example, between Public and GCC or between GCC and GCC High)
- [Document Automation](doc-automation.md) isn't available in GCC and GCC High
- [Add image or document input to a prompt](add-inputs-prompt.md) isn't available in GCC and GCC High

Learn about other limitations of Power Platform US Government in the following articles:

- [Power Apps US Government feature limitations](/power-platform/admin/powerapps-us-government#power-apps-us-government-feature-limitations)
- [Power Automate US Government feature limitations](/power-automate/us-govt#power-automate-us-government-feature-limitations)

## Related information

[AI model types](model-types.md)

