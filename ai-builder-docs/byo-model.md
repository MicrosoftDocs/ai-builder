---
title: Bring your own model - AI Builder (preview) | Microsoft Docs
description: Provides information on how to use your own model in AI Builder.
author: Raj-Virk
ms.service: aibuilder
ms.topic: conceptual
ms.custom:
ms.date: 08/16/2021
ms.author: Raj-Virk
ms.reviewer: v-aangie
---

# Bring your own AI model into AI Builder (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

You can bring your own model into AI Builder so that it can function like any AI Builder custom model. You can use your model in Microsoft Power Platform by using Power Automate, or you can build apps using Power Apps.

When you use your own model, it's sometimes referred to as a *model endpoint*, which enables communication. When you use your own model, limitations apply. These [limitations](#limitations) are described later in this article.

## Create your own model

Apart from AI Builder, you can create your own model using Azure or *\<example>*. 

To be able to register and use your custom model in AI Builder, it has to meet certain requirements:

- Existing model in any machine language platform with an endpoint.

- API definition (also known as swagger).

## Register your own model

The first step in bringing your own model into AI Builder is to register it. To register, follow the procedure in [Bring your own model tutorial](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial), which is in GitHub. <!-- Where do you find RegisterModel.ipynb notebook in tutorial? -->

Once you register the model, you'll see it in the list of AI Builder models. On the model details page, the **Model source** will be **Imported** to show that the external model is registered to AI Builder using your imported model endpoint.

> [!div class="mx-imgBorder"]
> ![Form editor binding properties screen.](media/byom-imported.png "Form editor binding properties screen")

## Limitations

- The only authentication mechanism supported is [API keys](/azure/machine-learning/how-to-authenticate-web-service) using [Azure Machine Learning](/azure/machine-learning/overview-what-is-azure-machine-learning). <!--API keys is not a product. Is link correct? -->

- Swagger version 2.0 is supported.

- Maximum allowed batch size is 500 rows.

- Maximum allowed latency/timeout is 20 seconds.

- Open API data types supported are:
   - Integer
   - Number
   - Boolean
   - String

- Base64 encoded image is supported only for real-time prediction (not supported for batch prediction). <!-- MSFT doesn't eo real-time, right? -->
   - The name of the field should end with **image** (case insensitive).
   - The data type should be **String**.

You're now ready to use your own model in AI Builder. You can perform application lifecycle management tasks such as package your model in a solution, import your model into a target environment, and upgrade your model in source/target environments.

### See also

[Application lifecycle management](byom-alm.md)