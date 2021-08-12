---
title: Application lifecycle management - AI Builder (preview) | Microsoft Docs
description: Provides information on how to use application lifecycle management in your own model imported into AI Builder.
author: Raj-Virk
ms.service: aibuilder
ms.topic: conceptual
ms.custom:
ms.date: 08/16/2021
ms.author: rajvirk
ms.reviewer: v-aangie
---

# Application lifecycle management (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Now that you've registered your model in AI Builder, you can perform application lifecycle management (ALM) tasks, such as:

- Package your model in a solution.
- Import your model into the target environment.
- Upgrade your model in source/target environments.

For ALM concepts in Microsoft Power Platform, go to [Overview of application lifecycle management](/power-platform/alm/overview-alm). To understand the components, tools, and processes needed to implement ALM with Power Platform, go to [ALM basics](/power-platform/alm/basics-alm).

## Package your own model in a solution

Solutions are used to transport apps and components from one environment to another. They are also used to apply a set of customizations to existing apps.

For solution features, go to [Solutions](/power-platform/alm/basics-alm).

1. Register model into source environment using AI Builder SDK. To register, follow the procedure in [Bring your own model tutorial](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial) (in GitHub). <!-- is this the same as "To register, follow the procedure in [Bring your own model tutorial](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial), which is in GitHub." If so, where do you find RegisterModel.ipynb notebook? -->

1. Create a solution to store the custom connector which is associated with the model:
   1. Select **Solutions** > **New solutions**.
   1. In the **New solution** dialog, complete the fields.
   1. Select **Create**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of a how to create a solution to store the custom connector.](media/byom-alm/alm-solution.png "Create a solution to store the custom connector")

1. Add an existing custom connector by selecting **Add** > **Automation** > **Custom connector**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of how to add an existing custom connector.](media/byom-alm/alm-add.png "Add an existing custom connector")

1. Select the custom connector associated with the model. The name will be in this format: \<model_name>-\<random number>-v\<version>.

   The version here helps distinguish which connector to add when updating a model.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the custom connector naming format.](media/byom-alm/alm-format.png "Custom connector naming format")

1. Export the solution:
   1. Select **Run** > **Next**. (If the solution isn't yet published, you must select **Publish** first.)
   1. Select **Managed** > **Export**.

1. Create a new solution to add the model and any other components.
   1. Select **Solutions** > **New solutions**.
   1. In the **New solution** dialog, complete the fields.
   1. Select **Create**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of a how to create a new solution to add the model and any other components.](media/byom-alm/alm-solution-new.png "Create a new solution to add the model and any other components")

1. Add an existing connection reference by selecting **Add** > **More** > **Connection Reference (preview)**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of how to add an existing connection reference.](media/byom-alm/alm-add-ref.png "Add an existing connection reference")

1. Add the existing connection reference associated with the model. The naming scheme here is the same as the custom connector in step 4: \<model_name>-\<random number>-v\<version>.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the connection reference naming format.](media/byom-alm/alm-ref-format.png "Connection reference naming format")

1. Add the AI model by selecting **Add** > **AI Model**.

   Your solution should contain the following components:

   > [!div class="mx-imgBorder"]
   > ![Screenshot of your model components.](media/byom-alm/alm-components.png "Model components")

1. (*Optional*) Add any desired components. To do this, repeat steps 6 through 9.

1. Export the solution:
   1. Select **Run** > **Next**. (If the solution isn't yet published, you must select **Publish** first.)
   1. Select **Managed** > **Export**.  

## Import your model into the target environment

Make sure you import only those solutions that you've obtained from a trusted source. In this example, you'll import the solution containing only the custom connector.

1.	Create the connection to your external endpoint. <!-- How do you get to this screen? -->
    1. If your endpoint is unsecured, select **Create**.
    1. If your endpoint is secured with an API key, enter it in the **API Key** field, and then select **Create**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the connection to an external endpoint.](media/byom-alm/alm-key.png "connection to an external endpoint")

1. Select **Import**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of the imported solution.](media/byom-alm/alm-import.png "Imported solution")

Your model is now ready to be consumed in your target environment.

If you experience issues with your import, go to [Troubleshooting solution import](/powerapps/maker/data-platform/import-update-export-solutions).

## Upgrade your model

Upgrade your solution to the latest version so that it rolls up all previous patches in one step. Any components associated to the previous solution version that are not in the newer solution version will be deleted. This will ensure components that are no longer part of the solution are removed.

For more information on upgrading, go to [Upgrade or update a solution](/powerapps/maker/data-platform/update-solutions).

### Upgrade your model in the source environment

1.	Register your new model endpoint in AI Builder SDK using the same model name and passing override=True. <!-- Where is the override? Not in the tutorial. --> To register, follow the procedure in [Bring your own model tutorial](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial) (in GitHub). <!-- is this the same as "To register, follow the procedure in [Bring your own model tutorial](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial)" If so, where do you find RegisterModel.ipynb notebook? -->

1.	Select the solution containing only the custom connector.
    1. Add a new existing custom connector by selecting **Add**.
    1. Complete the fields and enter the new version. In this example, it's v2 since this is the second version.
    
1. Remove the older version of the custom connector from the solution:
    1. Select the three dots next to the older version.
    1. Select **Remove** > **Remove from this solution**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of removing an older version from a solution.](media/byom-alm/alm-remove.png "Remove an older version from a solution")

1.	Export the solution by selecting **Export**. The version is incremented by default when exporting.

1.	In the solution containing the model, connection reference, and any other components, update the connection reference to the latest version, matching the custom connector name from previous step. In this example, v2 is the latest version.

    To do this, remove the older version of the connection reference from the solution by selecting the name to remove, and then selecting **Remove** > **Remove from this solution**.

1. Export the solution by selecting **Export**. The AI model and any component referencing the model are automatically updated to point to the latest version.

### Upgrade your model in the target environment

1. Import the solution containing only the connector by selecting **Import**.

1. Accept the default action, **Upgrade**. <!--I don't see this. -->

1.	Import the solution containing the model, connection reference, and any other component by selecting **Import**.

1. Accept the default action, **Upgrade**.

1. Create new connections to the new endpoint.
    1. If your endpoint is unsecured, select **Create**.
    1. If your endpoint is secured with an API key, enter it in the **API Key** field, and then select **Create**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the connection to a new endpoint.](media/byom-alm/alm-key-v2.png "connection to a new endpoint")

The model now will reference the new endpoint in the target environment.

## Stage your model for upgrade

You'll want to stage your model for upgrade so that the newest version of the model is referenced in all components in the environment.

1. Import the solution containing only the connector by selecting **Import**. 

1. Accept the default action, **Upgrade**. <!--I don't see this. -->

1. Import the solution containing the model, connection reference, and any other components by selecting **Import**.

1. Select **Stage for Upgrade**.

1. Create new connections to the new endpoint.
    1. If your endpoint is unsecured, select **Create**.
    1. If your endpoint is secured with an API key, enter it in the **API Key** field, and then select **Create**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the connection to a new endpoint.](media/byom-alm/alm-key-v2.png "connection to a new endpoint")

You'll see two versions of the solution: the *base* and the *upgrade*. Any component in the environment outside of these solutions will still reference the old version of the model. Components inside of these solutions will reference the version of the model contained in the corresponding solution.

In the following example, the cloud flow in the base solution references the old version and the cloud flow in the new solution references the new version.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of models before they are staged for upgrade.](media/byom-alm/alm-stage-1.png "Models before they are staged for upgrade")

To upgrade the old version, select **Apply upgrade**.

In the following example, all components in the environment now reference the new version of the model.

   > [!div class="mx-imgBorder"]
   > ![Screenshot of models after the upgrade is applied.](media/byom-alm/alm-stage-2.png "Models after the upgrade is applied")

### See also

[Overview of application lifecycle management](/power-platform/alm/overview-alm)<br/>
[ALM basics](/power-platform/alm/basics-alm)<br/>
[Import solutions](/powerapps/maker/data-platform/import-update-export-solutions)<br/>
[Upgrade or update a solution](/powerapps/maker/data-platform/update-solutions)