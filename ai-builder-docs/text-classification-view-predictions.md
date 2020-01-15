---
title: View generated predictions -  AI Builder | Microsoft Docs
description: Provides steps to view text classification predictions after you publish your model in AI Builder.
author: raaourik 
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: raaourik
ms.reviewer: v-dehaas
---

# View predictions

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

This section shows you how to see output of your prediction model.

1. After you select **Use Model** and configure it to run on Common Data Service, the output location appears in the **Settings** pane under the **Run** pivot.

    The name shown in **Tags output** is the name of the entity and attribute that's created after publishing. It is a link that takes you to the entity viewer section where the new fields added by AI Builder appear.

2. In the **Views** section, see values of the output fields for the different records. Use the **Filter by** function in the lower right-side pane to filter for only the records that don't have a label.

3. Next, you can build a basic model-driven app to use the output. For information about how to build a model-driven app in Power Apps, see [model-driven app overview](/powerapps/maker/model-driven-apps/model-driven-app-overview) topic in the Power Apps docs.

### Next step

[Use generated tags](text-classification-model-use-tags.md)
