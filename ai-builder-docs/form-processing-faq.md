---
title: FAQ for document processing
description: Learn the answers to frequently asked questions about the document processing model in AI Builder.
author: Phil-cmd
ms.topic: faq
ms.custom:
ms.date: 11/23/2026
ms.author: petercools
contributors:
  - Phil-cmd
  - antrodfr
  - v-aangie
ms.reviewer: angieandrews
---

# FAQ for document processing

This article answers frequently asked questions about the document processing model in AI Builder. If you don't find your question here, review [Overview of the document processing AI model](form-processing-model-overview.md) or submit your question to the [Power Automate Community for AI Builder](https://powerusers.microsoft.com/t5/AI-Builder/bd-p/AIBuilder).

## Functionality

### What can I do with document processing?

With document processing, you can build a custom AI model to extract information from various kinds of documents.

- Use the **Fixed-template documents** option if the elements of your documents appear in similar places. This option works well for invoices, purchase orders, delivery orders, and tax forms.
- Use the **General documents** option for any kind of document, including the documents supported by the first option as well as contracts, statements of work, letters, and other documents. This option can be more powerful for extracting data but requires a longer training time.

Learn more in [Overview of the document processing model](form-processing-model-overview.md).

### What types of documents can document processing handle?

Supported file types are PDF, JPG, and PNG.

### What data can I extract from documents by using document processing?

Document processing can extract fields, tables, and checkboxes from documents.

Learn more in [Define information to extract](create-form-processing-model.md#define-information-to-extract).

### Can I extract handwritten text from documents?

Yes. Document processing can extract printed and handwritten text from your documents.

### How many samples do I need to train a document processing model?

For high-quality documents that use the same layout, five sample documents should be sufficient. For low-quality documents (for example, scans of poor quality), you might need more sample documents. Use 15 to 20 sample documents to improve results.

#### Best practices

- **For template documents**
    - One layout per collection.
    - The layout must be identical within the same collection.
    - A minimum of five and a maximum of 20 documents per collection (don't exceed this limit).

- **For general documents**
    - Create a single model for all variations of a document type, including both structured and unstructured documents.
    - Label fields relevant to their values for better extraction accuracy.

        For example, use `supplier_id` for a supplier ID. Field names should match the document's language.
    - A minimum of five and a maximum of 20 documents per collection (don't exceed this limit).

#### My model is currently published in v3.1 (GA), and I'm planning to retrain it by using v4.0 (GA). Is it necessary to re-tag all of my documents?

Unless you're adding new fields, checkboxes, tables, signatures for data extraction, or new documents to the collection, you don't need to re-tag all the documents.

Before publishing your model, [quick test your model](form-processing-train.md#quick-test-your-model) by using one or more samples to verify and ensure all your desired fields are properly extracted.

#### Can I switch from one document type to another?

Yes, when you edit your model, you can switch between a fixed template document type and a general document type. However, this switch isn't supported for invoices.

### Can a single form-processing model extract information from documents that have different layouts or templates?

Yes. By using the collections feature, you can train a single form-processing model to handle documents that have different layouts.

Learn more in [Group documents by collections](create-form-processing-model.md#group-documents-by-collections).

### Can document processing handle *multiple* forms in a *single* document?

Each form needs to be in a separate file. For example, if you have a PDF document with multiple invoices in it, create a separate file for each invoice before you send it to the document processing model.

You can also specify pages for the document processing model to handle. By using this approach, you can take advantage of the model's functionality to loop through pages and process one form at a time.

Learn more in [Page range](form-processing-model-in-flow.md#page-range).

### I trained a document processing model but I'm not getting good results when it comes to extracted data. How can I improve the model?

If your model returns poor results after you train it, edit the model and provide more samples for training. The more samples you provide, the more the AI model learns how to extract data from your documents.

Learn more in [Improve the performance of your document processing model](improve-form-processing-performance.md).

## Limitations

### What is the maximum number of documents I can process?

You can process up to 360 documents per environment every 60 seconds.

### Why does the model recognize some characters incorrectly?

- The model can confuse some characters, such as the number 0 and the letter O, the number 1 and the letter l, and the number 4 and the letter A.
- The model can misinterpret characters that appear over or close to other characters. For example, the letter O over a vertical line becomes the number 0, the number 5 over a line becomes the $ (American dollar sign), and the lowercase letter l with an underscore becomes the uppercase letter L.
- The model can recognize some characters incorrectly, or not at all, on documents of poor quality.

In these cases, you can't improve recognition in AI Builder. To resolve these issues, improve the quality and layout of the source document.

> [!NOTE]
> Microsoft constantly improves the optical character recognition (OCR) technology to detect characters, so these issues happen less often.

### Can I create a model with many collections?

You can create up to 200 collections per model. However, training **General documents** models with tens of collections can take several hours. Training stops with a timeout error if it doesn't finish within 10 hours. If your model has a high number of collections, reduce the number of collections or documents per collection to keep training under this limit.

### Can I create a model in a solution?

Currently, you can't create a model in a solution.

### Can I use contracts and letters in my document processing model?

Yes, document processing supports unstructured documents like contracts and letters when you use the **General documents** option.

## Comparisons

### What are the differences among document processing, invoice processing, receipt processing, identity document reader, business card reader, and text recognition?

Depending on your situation, you might need to use a particular model or a combination of them.

Use [text recognition](prebuilt-text-recognition.md) when you want to extract all the text present in an image or a PDF. You can then, for example, search for a keyword in the text that is extracted, or build some fixed rules to extract certain items.

If you want to extract information from invoices, receipts, passports, driver's licenses, or business cards, start with the corresponding prebuilt model:

- [Invoice processing](prebuilt-invoice-processing.md)
- [Receipt processing](prebuilt-receipt-processing.md)
- [Identity document reader](prebuilt-id-reader.md) (passports and driver's licenses)
- [Business card reader](prebuilt-business-card.md)

You can use these prebuilt models immediately, without having to create a new model. These models can extract common information found in their corresponding document type.

For any other document type, you can create a custom document processing model to extract the fields and tables you need. This also applies if you need additional information not provided by the prebuilt model.

Learn more in [Custom document processing model](form-processing-model-overview.md).

### What is the difference between AI Builder document processing and Azure Form Recognizer?

AI Builder document processing is built on top of Azure Form Recognizer. This provides both products with the latest advancements in Microsoft AI.

- AI Builder is part of [Microsoft Power Platform](/power-platform/). This enables anyone to add AI into apps and automation with an easy-to-use interface. *You don't need to be a developer or data scientist*.

- [Azure Form Recognizer](/azure/applied-ai-services/form-recognizer/overview) is *targeted to professional developers*. They can use simple REST APIs to add AI capabilities to their custom code solutions.

## Cost options

### How much does AI Builder document processing cost?

You can start trying document processing for free by starting a [trial](administer-licensing.md). After you evaluate it, you need to purchase AI Builder credits to use document processing. Every page you process with document processing consumes AI Builder credits, even if the page doesn't contain data to extract. You can purchase AI Builder credits through AI Builder add-ons.

Learn more in [AI Builder licensing](administer-licensing.md).
