---
title: FAQ for text generation
description: Learn about the AI technology that's used in the text generation model, key considerations and details about how the AI is used, how it was tested and evaluated, and limitations.
ms.date: 011/15/2023
ms.custom: 
  - responsible-ai-faqs
ms.topic: conceptual
author: aashishb
ms.author: ashbhati
ms.reviewer: angieandrews
---

# FAQ for text generation

These frequently asked questions (FAQ) describe the AI impact of AI Builder's text generation feature.

## What is text generation?

The text generation capability in AI Builder offers users a versatile toolset for developing AI-powered workflows and applications. It allows for the creation of workflows and applications that summarize documents, create draft responses, classify text, and translate languages. This capability is powered by the Azure OpenAI Service, which utilizes Generative Pre-trained Transformer (GPT) technology. These models have been trained on vast amounts of text data, enabling them to generate text that resembles human-written content. To learn more about the Azure OpenAI Service, go to [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text).

## What are text generation’s capabilities?

The text generation model in AI Builder empowers users to build intelligent applications and workflows. The feature leverages the capabilities of pre-trained models, eliminating the need for customer model training. For example, if the intent is to build a workflow that summarizes incoming customer complaints and create a ticket in an incident management tool, based on the category of the incoming complaint, then makers can simply instruct the model to categorize and summarize the incoming complaint to create a new incident.

## What is text generation’s intended use?

The text generation model in AI Builder empowers you to build intelligent applications and workflows. The feature leverages the capabilities of pretrained models, which eliminates the need for customer model training. For example, the intent might be to build a workflow that summarizes incoming customer complaints and create a ticket in an incident management tool, based on the category of the incoming complaint. In this example, makers can simply instruct the model to categorize and summarize the incoming complaint to create a new incident.

List of use cases that are most popular use of this service:

List of use cases that are most popular use of this service:
- Summarization of emails, conversations, transcripts, documents, and more.
- Suggestions of draft responses to customer queries, complaints, email, and more.
- Extraction of information from contracts, emails, invoice, orders, and more.
- Classification of content in desired categories (for example, whether an email is an order, complaint, or a return).
- Sentiment analysis of a given text (for example, identifying sentiment of a product review).

In all these cases users are responsible for the final outcome of the system and are required to review the generated content for any potential inaccuracies of incompleteness prior to using it.

## How was text generation evaluated? What metrics are used to measure performance?

The evaluation of the text generation feature involves comprehensive testing across a range of safety parameters. This ensures that the feature aligns with our organization's responsible AI standards and principles. The service is also continually assessed for potential vulnerabilities. The performance metrics we use primarily involve the efficiency of content filtration and the degree of agreement between human and machine on filtered versus unfiltered content.

## What are the limitations of text generation? How can users minimize the impact of text generation limitations when using the system?

 The use of this technology must be in accordance with requirements in the [Code of conduct for Azure OpenAI Service](/legal/cognitive-services/openai/code-of-conduct). This technology must not be used for generating content associated with political propaganda, hate speech, misinformation, self-harm, discrimination, explicit sexual material, or other content prohibited by the Code of Conduct. Unsupported applications of this technology include providing advice, use for legal, financial, health-related guidance, or future predictions, as well as financial, scientific, or mathematical calculations, and any other unsupported usage mentioned in the [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text). Currently, the service is exclusively supported in the United States and is available only in the English language.

AI-generated content can have mistakes, hence Makers should inform the end users of their solution that the content generation by this model is created by AI in a transparent way. Clear communication of AI-generated content helps in avoiding overreliance. Maker should also infuse the possibility of human review step to make sure that the AI generated content is accurate and appropriate before using it.

## What operational factors and settings allow for effective and responsible use of the system?

Content generated by the AI model is probabilistic in nature, and hence model responses could vary for the same prompt. The response generated might be incorrect or misleading and could cause unintended outcomes from the flow or app. For example, business customers might receive wrong or incorrect information, recommendations or support. Makers should implement meaningful human oversight within their flows and apps, as well as test their prompts for the potential to lead to generating harmful behaviors or prohibited content as listed in Microsoft Code of Conduct. Low-code developers should also be transparent about the use of AI in their apps and flows to inform the business user, indicating that the content is generated by AI. Additionally, generated responses might not match low code developer’s expectations due to length restrictions, content filtering, or model selection.

## What are custom prompts and prebuilt prompts?

### Custom prompts

Custom prompts give makers the freedom to instruct the large language model (LLM) to behave in a certain way, or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the LLM model into a flexible tool to accomplish various tasks.

Example

With a language model, a custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.

### Prebuilt prompts

Prebuilt prompts are pre-configured prompts created and fine-tuned by the Microsoft team to assist makers in accomplishing common tasks easily. They offer templates to demonstrate how to use generative AI across various use cases, which simplifies interactions.

Example

A language model's prebuilt prompt could look like this:

Extract as a numbered list the action points from the: `[TextToExtract]`

In this case, the user only needs to supply the text in `[TextToExtract]` from which they want to extract action points. The prebuilt prompt takes care of the rest.

## See also

- [Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
- [Text generation model overview (preview)](prebuilt-azure-openai.md)

[!INCLUDE[footer-include](./includes/footer-banner.md)]
