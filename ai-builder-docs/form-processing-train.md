---
title: Train and publish your form processing model - AI Builder | Microsoft Docs
description: Walks you through the steps to train, validate, and test your form processing model in AI Builder.
author: JoeFernandezMS
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Train and publish your form processing model

After you create your form processing model, you can train, test, and publish it to make it available.

## Train and validate your model

1. Select **Next** to check your selected form fields. If everything looks good, select **Train** to train your model.
1. When training is completed, select **Go to Details page** on the **Training complete** screen.

## Quick-test your model

1. On the details page, select **Quick test**.
2. You can either drag a document or select **Upload from my device** to upload your test file. The quick-test should only take a few seconds before displaying the results.
3. Select **Start over** to run another test, or **Close** if you're finished.

## Troubleshooting tips

If you have trouble training your model, try these suggestions:

- Make sure your data meets the guidelines listed in [form processing model requirements and limitations](form-processing-model-requirements.md).
- Learn how you can [improve the performance of your form processing model](improve-form-processing-performance.md).
- Download [sample material](https://go.microsoft.com/fwlink/?linkid=2103171) and use it for testing.

## Publish your model

If you're happy with your model, you can select **Publish** to publish it. When publishing is complete, your model is promoted as **Published** and is ready to be used. More information: [Publish your model in AI Builder](publish-model.md)

After you've published your form-processing model, you can use it in a [Power Apps canvas app](/ai-builder/form-processor-component-in-powerapps) or in [Power Automate](/ai-builder/form-processing-model-in-flow).

### See also

[Use a form-processing model in Power Automate](form-processing-model-in-flow.md)  
[Use the form-processor component in Power Apps](form-processor-component-in-powerapps.md)
