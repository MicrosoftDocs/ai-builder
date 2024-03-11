---
title: FAQ for Prompts and text generation capabilities
description: Learn about the AI technology that's used in the Prompts, key considerations and details about how the AI is used, how it was tested and evaluated, and limitations.
ms.date: 01/10/2024
ms.custom: 
  - responsible-ai-faqs
ms.topic: conceptual
author: aashishb
ms.author: ashbhati
ms.reviewer: angieandrews
---

# FAQ for Prompts and text generation capabilities

These frequently asked questions (FAQ) describe the AI impact of AI Builder's Prompts feature.

## What are prompts?

Prompts in AI Builder offers users a versatile capability for developing AI-powered workflows, applications, data transformation and customization of Copilots. It allows for the creation of workflows and applications that summarize documents, create draft responses, classify text, and translate languages. This capability is powered by the Azure OpenAI Service, which utilizes Generative Pre-trained Transformer (GPT) technology. These models have been trained on vast amounts of text data, enabling them to generate text that resembles human-written content. To learn more about the Azure OpenAI Service, go to [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text).


## What are the intended use cases of Prompts?

Prompts in AI Builder empowers you to build intelligent applications, workflows and extend copilots. They leverages the capabilities of pretrained GPT models, which eliminates the need for custom model training. For example, the intent might be to build a workflow that summarizes incoming customer complaints and create a ticket in an incident management tool, based on the category of the incoming complaint. In this example, makers can simply instruct the model to categorize and summarize the incoming complaint to create a new incident.

List of use cases that are most popular use of this service:
- Summarization of emails, conversations, transcripts, documents, and more.
- Suggestions of draft responses to customer queries, complaints, email, and more.
- Extraction of information from contracts, emails, invoice, orders, and more.
- Classification of content in desired categories (for example, whether an email is an order, complaint, or a return).
- Sentiment analysis of a given text (for example, identifying sentiment of a product review).

In all these cases users are responsible for the final outcome of the system and are required to review the generated content for any potential inaccuracies of incompleteness prior to using it.


## How was the readiness of the Prompts feature evaluated? What metrics are used to measure performance?

The evaluation of this capability involves comprehensive testing across a range of safety parameters. This ensures that the feature aligns with our organization's responsible AI standards and principles. The service is also continually assessed for potential vulnerabilities. The performance metrics we use primarily involve the efficiency of content filtration and the degree of agreement between human and machine on filtered versus unfiltered content.


## What kind of content moderation is implemented for Prompts?
The GPTs models are trained on internet data, which is great for building a general world model but at the same time can inherit toxic, harmful and biased content from the same sources. The models are trained to behave safely and not product harmful content, but some times it can generate toxic output. AI Builder Prompts leverage [Azure AI Content Satefy](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/overview) Service to bake state of the art content moderation capabilities within the AI Prompts. This includes services to analyze the generate output with multi-severity text scanners as well as safety against prompt injection attacks. The output is also scanned for regurgitation of protected material.


## What are the limitations of Prompts? How can users minimize the impact of Prompt limitations when using the system?

The use of this technology must be in accordance with requirements in the [Code of conduct for Azure OpenAI Service](/legal/cognitive-services/openai/code-of-conduct). This technology must not be used for generating content associated with political propaganda, hate speech, misinformation, self-harm, discrimination, explicit sexual material, or other content prohibited by the Code of Conduct. Unsupported applications of this technology include providing advice, use for legal, financial, health-related guidance, or future predictions, as well as financial, scientific, or mathematical calculations, and any other unsupported usage mentioned in the [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text). Currently, the service is exclusively supported in the United States and is available only in the English language.

AI-generated content can have mistakes, hence Makers should inform the end users of their solution that the content generation by this model is created by AI in a transparent way. Clear communication of AI-generated content helps in avoiding overreliance. Maker should also infuse the possibility of human review step to make sure that the AI generated content is accurate and appropriate before using it.


## What operational factors and settings allow for effective and responsible use of the system?

Content generated by the AI model is probabilistic in nature, and hence model responses could vary for the same prompt. The response generated might be incorrect or misleading and could cause unintended outcomes from the flow or app. For example, business customers might receive wrong or incorrect information, recommendations or support. Makers should implement meaningful human oversight within their flows and apps, as well as test their prompts for the potential to lead to generating harmful behaviors or prohibited content as listed in Microsoft Code of Conduct. Low-code developers should also be transparent about the use of AI in their apps and flows to inform the business user, indicating that the content is generated by AI. Additionally, generated responses might not match low code developer’s expectations due to length restrictions, content filtering, or model selection.

## What are custom prompts and AI functions?

### Custom prompts

[Custom prompts](create-a-custom-prompt.md) give makers the freedom to instruct the large language model (LLM) to behave in a certain way, or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the LLM model into a flexible tool to accomplish various tasks.

Example

With a language model, a custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.

### AI functions

Prebuilt AI functions are pre-configured prompts created by the Microsoft team to assist makers in accomplishing common tasks easily. They offer ready to use AI capabilities across various use cases, which simplifies maker experience to infuse intelligence in their solutions.

Example

A language model's prebuilt prompt could look like this:

Extract as a numbered list the action points from the: `[TextToExtract]`

In this case, the user only needs to supply the text in `[TextToExtract]` from which they want to extract action points. The prebuilt prompt takes care of the rest.

## See also

- [Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
- [Text generation model overview (preview)](prebuilt-azure-openai.md)

[!INCLUDE[footer-include](./includes/footer-banner.md)]
