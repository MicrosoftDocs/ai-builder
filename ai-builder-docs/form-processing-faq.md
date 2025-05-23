---
title: FAQ for document processing
description: Learn the answers to frequently asked questions about the document. processing model in AI Builder.
author: Phil-cmd
ms.topic: faq
ms.custom: 
ms.date: 05/23/2025
ms.author: plarrue
contributors:
  - Phil-cmd
  - antrodfr
  - v-aangie
ms.reviewer: angieandrews
---

# FAQ for document processing

This article consists of frequently asked questions about the document processing model in AI Builder. If you don't find your question here, review [Overview of the document processing AI model](form-processing-model-overview.md) or submit your question to the [Power Automate Community for AI Builder](https://powerusers.microsoft.com/t5/AI-Builder/bd-p/AIBuilder).

## Functionality

### What can I do with document processing?

With document processing, you can build a custom AI model to extract information from various kinds of documents.

- The **Fixed-template documents** option is ideal if the elements of your documents can be found in similar places. It's usually the case for invoices, purchase orders, delivery orders, and tax forms.
- **General documents** option is ideal for any kind of document, including the ones supported by the first option but also contracts, statement of work, letters, and others. This option can be more powerful to extract data, but requires longer training time.

Learn more in [Overview of the document processing model](form-processing-model-overview.md).

### What types of documents can document processing handle?

Supported file types are PDF, JPG, and PNG.

### What data can I extract from documents by using document processing?

Document processing can extract fields, tables, and checkboxes from documents.

Learn more in [Define information to extract](create-form-processing-model.md#define-information-to-extract).

### Can I extract handwritten text from documents?

Yes. Document processing can extract printed and handwritten text from your documents.

### How many samples do I need to train a document processing model?

For high-quality documents that use the same layout, five sample documents should be sufficient. For low-quality documents (for example, scans of poor quality), more sample documents might be necessary. To improve results, use 15 to 20 sample documents.

#### Best practices

- **For template documents**
    - One (1) layout per collection.
    - The layout must be identical within the same collection.
    - A minimum of five (5) and a maximum of 20 documents per collection (don't exceed this limit).

- **For general documents**
    - Create a single model for all variations of a document type including both structured and unstructured documents.
    - Label fields relevant to their values for better extraction accuracy.

        For example, use "supplier_id" for a supplier ID. Field names should match the document's language.
    - A minimum of five (5) and a maximum of 20 documents per collection (don't exceed this limit).

#### My model is currently published in v3.1 (GA), and I'm planning to retrain it using v4.0 (GA). Is it necessary to re-tag all of my documents?

Unless you're adding new fields, checkboxes, tables, signatures for data extraction, or new documents to the collection, you don't need to re-tag all the documents.

Before publishing your model, it's recommended to [quick test your model](form-processing-train.md#quick-test-your-model) using one or more samples to verify and ensure all your desired fields are properly extracted.
  
#### Can I switch from one document type to another?

Yes, when editing your model, you can switch between a fixed template document type and a general document type. However, this switch isn't supported for invoices.

### Can a single form-processing model extract information from documents that have different layouts or templates?

Yes. By using the collections feature, you train a single form-processing model to handle documents that have different layouts.

Learn more in [Group documents by collections](create-form-processing-model.md#group-documents-by-collections).

### Can document processing handle *multiple* forms in a *single* document?

Each form needs to be in a separate file. For example, if you have a PDF document with multiple invoices in it, create a separate file for each invoice before you send it to the document processing model.

You can also specify pages for the document processing model to handle. This way you can take advantage of the model's functionality to loop page by page, and process one form at a time.

Learn more in [Page range](form-processing-model-in-flow.md#page-range).

### I trained a document processing model but I'm not getting good results when it comes to extracted data. How can I improve the model?

If your model is returning poor results after you trained it, edit the model and provide more samples for training. The more samples you provide, the more the AI model learns how to extract data from your documents.

Learn more in [Improve the performance of your document processing model](improve-form-processing-performance.md).

## Limitations

### What is the maximum number of documents I can process?

You can process up to 360 documents per environment, every 60 seconds.

### Why do some characters get recognized incorrectly?

- It can happen that some characters get confused: 0 (number) and O (letter), 1 (number) and l (letter), 4 (number) and A (letter), and more.
- It can happen that some characters over or close to others get recognized incorrectly: O (letter) over a vertical line becomes a 0 (number), 5 (number) over a line becomes a $ (American dollar sign), l_ (lowercase letter, underscore) becomes an L (uppercase letter), and more.
- It can happen that some characters on documents of poor quality get recognized incorrectly, or not at all.

In the previous cases, nothing can be done in AI Builder to improve the recognition. We recommand to improve the quality and layout of the source document to solve similar issues.

> [!NOTE]
> Microsoft constantly improves the optical character recognition (OCR) technology to detect characters, so such issues happen less often.

### Can I create a model with many collections?

You can create up to 200 collections per model. However, training **General documents** models with tens of collections can take several hours and&mdash;in rare occasions&mdash;time out. If your model has a high number of collections, expect to wait up to 24 hours for model training completion.

### Can I create a model in a solution?

Currently, it isn't possible to create a model in a solution.

### Can I use contracts and letters in my documents processing model?

Yes, unstructured documents like contracts and letters are supported by document processing, using the **General documents** option.

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

You can start trying out document processing for free by starting a [trial](administer-licensing.md). After you evaluate it, you need to purchase AI Builder credits to use document processing. Every page you process with document processing consumes AI Builder credits, even if the page doesn't contain data to extract. AI Builder credits can be purchased through AI Builder add-ons.

Learn more in [AI Builder licensing](administer-licensing.md).
