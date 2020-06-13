---
title: Use sample data to do form processing - AI Builder | Microsoft Docs
description: Provides the information you need to try out a form processing model with sample data AI Builder.
author: JoeFernandezMS
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: JoeFernandezMS
ms.reviewer: v-dehaas
---

# Use sample data to do form processing

To explore the possibilities of form processing, you can get started by building and training a form-processing model that uses sample invoices.


## Get the sample data

Download [AI Builder Form Processing Sample Data.zip](https://go.microsoft.com/fwlink/?linkid=2128080), which contains the sample invoices.

## Build your model

1. Extract the downloaded files, and then go to **AI Builder Form Processing Sample Data\Invoices**, where you'll see two folders: **Train** and **Test**.
2. On the AI Builder **Build** screen, select **Form processing model**.
3. Enter a name, and then create your model.
4. When you're prompted to upload data, upload the five invoices from the **Train** folder.

   > [!div class="mx-imgBorder"]
   > ![Upload sample invoices](media/upload-forms.png "Upload sample invoices")

5. Next, select the detected fields you want your model to return.

   > [!div class="mx-imgBorder"]
   > ![Select fields](media/select-form-fields.png "Select fields")

6. After you train your model, do a quick test by using the invoice in the **Test** folder that you downloaded, to see how it works.

   > [!div class="mx-imgBorder"]
   > ![Quick test](media/quick-test-form.png "Quick test")

### See also

[Use a form-processing model in Power Automate](form-processing-model-in-flow.md)  
[Use the form-processor component in Power Apps](form-processor-component-in-powerapps.md)
