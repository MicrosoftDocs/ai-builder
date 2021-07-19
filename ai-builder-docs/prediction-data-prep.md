---
title: Data preparation - AI Builder | Microsoft Docs
description: Provides the steps you'll need to follow to prepare your data for AI Builder in Microsoft Dataverse. 
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 07/23/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Data preparation

Before you create your prediction model, you'll want to make sure your data is in Microsoft Dataverse and that it's in the correct format.

## Create your custom table

Do you have data that you want to import into Dataverse for training in AI Builder? First, you have to create a table. In this example, we'll provide a solution that has predefined custom tables. To use your own data, [create a custom table](/powerapps/maker/common-data-service/data-platform-create-entity) and use your own table instead of the the example used here.

> [!NOTE]
>For best results, use a dataset that is less than 1.5 GB in size. Otherwise, AI Builder uses only 1.5 GB of your data to train and predict. Since you can’t control which data exceeding the 1.5 GB limit isn't used, you should optimize your data to stay under 1.5 GB.

## Sample dataset for prediction model

1. Download the AI Builder sample dataset package: [AIBPredictionSample_simpledeploy_v4.21.3.zip](https://microsoft.sharepoint.com/:u:/t/PowerAppsAI/EaBYOtfuvc5OqK4qh1-drvoBD_mCfM4hyLz3zJ0EwDqGjg?e=aI2aue)

1. Ensure the file isn't blocked after download. To do this:
   1. Locate the downloaded zip file, right-click, and select **Properties**.
   1. Place a check in the **Unblock** checkbox and select **Apply**.

   > [!div class="mx-imgBorder"]
   > ![Properties screen](media/prep-block.png "Properties screen")

1. Extract the .zip and look for **PackageDeployer.exe** in the extracted folder.

   > [!div class="mx-imgBorder"]
   > ![The extracted folder file names](media/prep-exe.png "The extracted folder file names")

1. Run **PackageDeployer.exe**. You'll see the following screen:

   > [!div class="mx-imgBorder"]
   > ![Package Deployer landing page](media/prep-run-dp.png "Package Deployer landing page")

1. Select **Continue**.

1. Select **Office 365** > **Login**.

   > [!div class="mx-imgBorder"]
   > ![Login to Package Deployer screen](media/prep-dp-login.png "Login to Package Deployer screen")

1. Enter the credentials that you use to log in to the Power Apps maker portal and then select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Enter your credentials screen](media/prep-credentials.png "Enter your credentials screen")

1. If the login is successful, you'll see the Welcome screen. Read the message and select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Install the AI Builder prediction sample dataset screen](media/prep-welcome.png "Install the AI Builder prediction sample dataset screen")

1. In the **Ready to Install** screen, make sure you're installing the solution in the correct environment and then select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Screen showing the solution package to be installed and organization name](media/prep-install.png "Ssreen showing the solution package to be installed and organization name")

1. In the **Reading AIB Prediction Dataset Installer Configuration** screen, read the summary information for the data and solutions being imported and then select **Next**.

   It will take a few minutes to import the data. As each step is completed successfully, you'll see a green circle with a check mark next to the step.  

   > [!div class="mx-imgBorder"]
   > ![Summary of the AI Builder prediction dataset installer configuration](media/prep-config.png "Summary of the AI Builder prediction dataset installer configuration")

1. In the **Installation Complete** screen, complete the process by selecting **Finish**.

   > [!div class="mx-imgBorder"]
   > ![Installation complete screen](media/prep-finish.png "Installation complete screen")

## How you can use the solutions you installed

The sample dataset installs two (2) solutions in your environment. It also installs sample data for the included entities:

- **Brazilian Commerce:** Use for predicting multiple outcomes.

- **AI Builder Online Shopper Intention:** Use for binary prediction and numerical prediction

> [!div class="mx-imgBorder"]
> ![Solution details screen](media/prep-solutions.png "Solution details screen")

You'are now ready to go to the next step.

### Next step

[Create a prediction model](prediction-create-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
