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

<!--note from editor: Can you suggest edits to the Readme file that accompanies this zip file? We don't want to use language codes in URLs, and we don't abbreviate "CDS." Also, it uses "text classification" instead of "category classification." The edit below assumes that Steps 1 and 2 under "Manual data setup" apply only to the three scenarios mentioned and not the others. But, how could that be? Don't you have to install the solution in a CDS environment no matter what??
***BEGIN EDIT***

AI Builder labs walk you through object detection, binary classification, text classification, form processing, and business card scenarios. Please visit [https://docs.microsoft.com/ai-builder/overview] to learn more about the scenarios and AI Builder.

To set up the environment to use AI Builder labs, follow these steps. SELF THIS IS CONFUSING.

For Binary Classification, Text Classification, and Object Detection scenarios you need sample data in Common Data Service.

Manual data setup

Step 1: Import AIBuilderLabSolution_1_0_0_0 to the Common Data Service environment.
        This will create three Common Data Service entities:
           Object Detection Product , Health Feedback, and Online Shopping Intent 

Step 2 : Upload data to the entities created in step 1.
o	Binary classification :	Follow the instructions [here](https://docs.microsoft.com/ai-builder/binary-classification-data-prep) to upload the Online Shopping Intent data.
o	Text Classification : Go to the Lab Data/Text Classification folder, and then upload data from pai_healthcare_feedbacks. Follow the instructions [here](https://docs.microsoft.com/ai-builder/before-you-build-text-classification-model).
o	Object Detection : Go to the Lab Data/ObjectDetection folder, upload data from aib_objectdetectionproducts, and follow the same instructions as the previous step.

For form processing, business card, and object detection labs, you'll need images and PDFs that are available in the Lab Images folder.


***END EDIT***
-->