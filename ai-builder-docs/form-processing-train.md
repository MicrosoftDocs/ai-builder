---
title: Train and publish your document processing model in AI Builder
description: Learn how to train, validate, and test your document processing model in AI Builder.
author: jsowndarrajan02
contribuors:
  - jsowndarrajan02
  - angieandrews
ms.topic: conceptual
ms.custom: 
ms.date: 01/13/2025
ms.author: sjayapal
ms.reviewer: angieandrews
---

# Train and publish your document processing model

After you create your document processing model, you can train, test, and publish it to make it available.

## Train and validate your model

1. Select **Next** to check your selected form fields. If everything looks good, select **Train** to train your model.

1. When training is completed, select **Go to Details page** on the **Training complete** screen.

## Quick-test your model

1. On the details page, select **Quick test**.

1. You can either drag a document or select **Upload from my device** to upload your test file. The quick test should only take a few seconds before displaying the results.

1. Select **Start over** to run another test, or **Close** if you're finished.

### Limitation

If file processing exceeds 90 seconds during a quick test, you encounter a **408 - Dependency Timeout** error. The reason is that the quick test is designed with a 90-second time-out limit. To ensure smooth testing, use files with fewer pages and a smaller size.

For larger files, we recommend that you create a Power Automate flow to validate them. The Power Automate flow uses the `Predict` operation, which offers a 60-minute time-out. This makes it ideal for testing large files efficiently.

## Troubleshooting tips

If you have trouble training your model, try these suggestions:

- If you don't see your training document, go to [Training document isn't displayed on the document processing model details page](/troubleshoot/power-platform/ai-builder/the-training-document-is-not-displayed-on-the-form-processing-model-details-page) for a possible resolution.

- Make sure your data meets the guidelines listed in [document processing model requirements and limitations](form-processing-model-requirements.md).

- Learn how you can [improve the performance of your document processing model](improve-form-processing-performance.md).

- Download [sample material](https://go.microsoft.com/fwlink/?linkid=2103171) and use it for testing.

## Publish your model

If you're happy with your model, you can select **Publish** to publish it. When publishing is complete, your model is promoted as **Published** and is ready to be used. More information: [Publish your model in AI Builder](publish-model.md)

After publishing your form-processing model, you can use it in a [Power Apps canvas app](./form-processor-component-in-powerapps.md) or in [Power Automate](./form-processing-model-in-flow.md).

## Limits

The following limit applies to calls made per environment across document processing models including prebuilt models: receipt processing and invoice processing.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Calls (per environment)|360|60 seconds|

## Related information

- [Use a document processing model in Power Automate](form-processing-model-in-flow.md)  
- [Use the form processor component in Power Apps](form-processor-component-in-powerapps.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
