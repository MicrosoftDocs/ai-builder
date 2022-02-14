---
title: Data preparation - AI Builder | Microsoft Docs
description: Provides the steps you'll need to follow to prepare your data for AI Builder in Microsoft Dataverse. 
author: norliu
ms.topic: conceptual
ms.custom: 
ms.date: 07/29/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Data preparation

Before you create your prediction model, you'll want to make sure your data is in Microsoft Dataverse and that it's in the correct format.

## Create your custom table

Do you have data that you want to import into Dataverse for training in AI Builder? First, you have to create a table. In this example, we'll provide a solution that has predefined custom tables. To use your own data, [create a custom table](/powerapps/maker/data-platform/data-platform-create-entity) and use it instead of the example used here.

> [!NOTE]
> For best results, use a dataset that is less than 1.5 GB in size. Otherwise, AI Builder will use only 1.5 GB of your data to train and predict. Because you can’t control which data that exceeds the 1.5 GB limit won't be used, you should optimize your data to stay under 1.5 GB.

## Sample dataset for prediction model

1. Download the AI Builder sample dataset package:
   1. Select [AIBPredictionSample_simpledeploy_v4.21.3.zip](https://github.com/microsoft/PowerApps-Samples/blob/master/ai-builder/AIBPredictionSample_simpledeploy_v4.21.3.zip).
   1. Select the **Download** button.
   > [!div class="mx-imgBorder"]
   > ![Screenshot of the download screen in GitHub.](media/prep-download.png "Download screen in GitHub")

1. Ensure that the file isn't blocked after you download. To do this:
   1. In the Downloads folder, find the downloaded zip file, right-click, and then select **Properties**.
   1. On the General tab, select the **Unblock** checkbox, and then select **Apply**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the .zip file Properties.](media/prep-block.png "Properties screen")

1. Extract the .zip file, and look for **PackageDeployer.exe** in the extracted folder.

   > [!div class="mx-imgBorder"]
   > ![Screenshot showing PackageDeployer.exe selected.](media/prep-exe.png "The extracted folder file names")

1. Run **PackageDeployer.exe**. The following screen will appear.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the Package Deployer landing page.](media/prep-run-dp.png "Package Deployer landing page")

1. Select **Continue**.

1. Select **Office 365**, and then select **Login**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of signing in to the Package Deployer.](media/prep-dp-login.png "Login to Package Deployer screen")

1. Enter the credentials that you use to sign in to the Power Apps maker portal, and then select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of entering your credentials.](media/prep-credentials.png "Enter your credentials screen")

1. If the sign-in is successful, you'll see the Welcome screen. Read the message, and then select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of installing the AI Builder prediction sample dataset.](media/prep-welcome.png "Install the AI Builder prediction sample dataset screen")

1. On the **Ready to Install** screen, make sure you're installing the solution in the correct environment and then select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot showing the solution package to be installed and the organization name.](media/prep-install.png "Ssreen showing the solution package to be installed and organization name")

1. On the **Reading AIB Prediction Dataset Installer Configuration** screen, read the summary information for the data and solutions being imported and then select **Next**.

   It will take a few minutes to import the data. As each step is completed successfully, you'll see a green circle with a check mark next to the step.  

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the summary of the AI Builder prediction dataset installer configuration.](media/prep-config.png "Summary of the AI Builder prediction dataset installer configuration")

1. On the **Installation Complete** screen, select **Finish**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot showing installation complete.](media/prep-finish.png "Installation complete screen")

## How you can use the solutions you installed

The sample dataset installs two solutions in your environment. It also installs sample data for the included entities:

- **Brazilian Commerce:** Use for predicting multiple outcomes. Select **BC Orders** as the table, and **Delivery Timeliness** as the column when you pick what you want to predict.

- **AI Builder Online Shopper Intention:** Use for binary prediction and numerical prediction.
   - Select **Online Shopper Intentions** as the table, and **Revenue (Label)** as the column if you want to try out binary prediction.
   - Select **Online Shopper Intentions** as the table. Also select **ExitRates** or **BounceRates** as the column if you want to try out numerical prediction.

If you need help with creating a prediction model, follow the instructions in [Create a prediction model](prediction-create-model.md).

> [!div class="mx-imgBorder"]
> ![Screenshot of solution details.](media/prep-solutions.png "Solution details screen")

You're now ready to go to the next step.

### Next step

[Create a prediction model](prediction-create-model.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
