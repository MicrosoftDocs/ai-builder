---
title: AI Builder labs - AI Builder | Microsoft Docs
description: Provides information about resources to help you learn more about AI Builder 
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/05/2019
ms.author: npouhaer; mfotedar
ms.reviewer: v-dehaas
---

# AI Builder labs

Use AI Builder labs to gain experience with AI Builder and learn more about it. Links are added here as new resources become available.

AI Builder [hands-on labs](https://go.microsoft.com/fwlink/?linkid=2103171) walk through these features:

- Object detection
- Prediction
- Category classification
- Form processing
- Business card reader

The zip file that contains the hands-on labs includes the following folders and zip files:

- Lab data
- Lab images
- Lab scripts
- AIBuilderLabSolution_1_0_0_0.zip
- ProcessFeedback_Flow.zip

<!--note from editor: Can you suggest edits to the Readme file that accompanies this zip file? There shouldn't be language codes in URLs, we don't abbreviate "CDS," it looks like "text classification" should be "category classification" and "binary classification" should be "prediction". The edit below assumes that Steps 1 and 2 under "Manual data setup" apply only to the three scenarios mentioned and not the others. Note that the formatting is very old-school, with hard returns to keep the bulleted lists aligned. This is how we did Readmes in the old days, I'm not sure that it's still a best practice.
***BEGIN EDIT***

AI Builder labs walk you through prediction, category classification, object detection, form processing, and business card scenarios. Please visit [https://docs.microsoft.com/ai-builder/overview] to learn more about the scenarios and AI Builder.

For prediction, category classification, and object detection scenarios, you need sample data in Common Data Service.

Manual data setup

Step 1: Import AIBuilderLabSolution_1_0_0_0 to the Common Data Service environment.
        This will create three Common Data Service entities:
        o Object Detection Product
        o Health Feedback
        o Online Shopping Intent 

Step 2 : Upload data to the entities created in step 1.
        o Prediction: Follow the instructions in
          https://docs.microsoft.com/ai-builder/binary-classification-data-prep
          to upload the Online Shopping Intent data.
        o Category classification : Go to the Lab Data/Text Classification folder,
          and then upload data from pai_healthcare_feedbacks. Follow the instructions in
          https://docs.microsoft.com/ai-builder/before-you-build-text-classification-model.
        o Object Detection : Go to the Lab Data/ObjectDetection folder, upload data from
          aib_objectdetectionproducts, and follow the same instructions as the previous step.

For form processing, business card, and object detection labs, you'll need images and PDFs that
are available in the Lab Images folder.


***END EDIT***
-->