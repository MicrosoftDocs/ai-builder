---
title: View generated predictions - AI Builder | Microsoft Docs
description: Provides steps to view category classification predictions after you publish your model in AI Builder.
author: raaourik 
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: raaourik
ms.reviewer: v-dehaas
---

# View predictions

This section<!--Is this going to be a section someday, or should this simply be "topic"? --> shows you how to see the output of your prediction<!--Should this be "category classification"? I'm kind of confused by this topic. It seems like it should have more detail, and it should be more of an umbrella topic (that is, higher up in the TOC) if it applies to more than one type of model.--> model.

1. After you select **Use Model** and configure it to run on Common Data Service, the output location appears in the **Settings** pane under the **Run** pivot.

    The name shown in **Tags output** is the name of the entity and attribute that's created after publishing. It's a link that takes you to the entity viewer section where the new fields added by AI Builder appear.

2. In the **Views** section, see values of the output fields for the different records. Use the **Filter by** function in the lower-right side pane to filter for only the records that don't have a label.

3. Next, you can build a basic model-driven app to use the output. For information about how to build a model-driven app in Power Apps, see [model-driven app overview](/powerapps/maker/model-driven-apps/model-driven-app-overview).

### Next step

[Use generated tags](text-classification-model-use-tags.md)
