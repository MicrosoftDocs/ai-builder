---
title: FAQ for prompts and text generation capabilities
description: Learn about the AI technology used in prompts, key considerations and details about how the AI is used, how it was tested and evaluated, and limitations.
ms.date: 08/27/2024
ms.custom: 
  - responsible-ai-faqs
ms.topic: conceptual
author: aashishb
contributors:
  - phil-cmd
  - aashishb
  - antoinecellerier
  - v-aangie
ms.author: plarrue
ms.reviewer: angieandrews
ms.collection: 
    - bap-ai-copilot
---

# FAQ for prompts and text generation capabilities

These frequently asked questions (FAQ) describe the AI impact of AI Builder's prompts feature.

## What are prompts?

The prompts feature in AI Builder offers users a versatile capability for developing AI-powered workflows, applications, data transformation, and customization of copilots. It allows for the creation of workflows and applications that summarize documents, create draft responses, classify text, and translate languages. This capability is powered by the Azure OpenAI Service, which utilizes Generative Pre-trained Transformer (GPT) technology. These models have been trained on vast amounts of text data, enabling them to generate text that resembles human-written content. To learn more about the Azure OpenAI Service, go to [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text).

## What are the intended use cases of prompts?

Prompts in AI Builder empower you to build intelligent applications, workflows, and extend copilots. They leverage the capabilities of pre-trained GPT models, which eliminates the need for custom model training. For example, the intent might be to build a workflow that summarizes incoming customer complaints. Then, it creates a ticket in an incident management tool based on the category of the incoming complaint. In this example, makers can simply instruct the model to categorize and summarize the incoming complaint to create a new incident.

The following list contains the most popular use cases for this service:

- Summarization of emails, conversations, transcripts, documents, and more.
- Suggestions of draft responses to customer queries, complaints, email, and more.
- Extraction of information from contracts, emails, invoice, orders, and more.
- Classification of content in desired categories (for example, whether an email is an order, complaint, or a return).
- Sentiment analysis of a given text (for example, identifying sentiment of a product review).

In all these cases, users are responsible for the final outcome of the system. They're required to review the generated content for any potential inaccuracies of incompleteness before using it.

## How was the readiness of the prompts feature evaluated? What metrics are used to measure performance?

The evaluation of this capability involves comprehensive testing across a range of safety parameters. This ensures that the feature aligns with our organization's responsible AI standards and principles. The service is also continually assessed for potential vulnerabilities. The performance metrics we use primarily involve the efficiency of content filtration and the degree of agreement between human and machine on filtered versus unfiltered content.

## What kind of content moderation is implemented for prompts?

The GPT models are trained on internet data, which is great for building a general world model. At the same time, it can inherit toxic, harmful, and biased content from the same sources. The models are trained to behave safely and not product harmful content, but sometimes it can generate toxic output. AI Builder prompts leverage [Azure AI Content Satefy](/azure/ai-services/content-safety/overview) service to bake state of the art content moderation capabilities within the AI prompts. This includes services to analyze the generated output with multi-severity text scanners and safety against prompt injection attacks. The output is also scanned for regurgitation of protected material.

## What are the limitations of the prompts feature? How can users minimize the impact of prompt limitations when using the system?

The use of this technology must be in accordance with requirements in the [Code of conduct for Azure OpenAI Service](/legal/cognitive-services/openai/code-of-conduct). This technology must not be used for generating content associated with political propaganda, hate speech, misinformation, self-harm, discrimination, explicit sexual material, or other content prohibited by the Code of Conduct. Unsupported applications of this technology include providing advice, use for legal, financial, health-related guidance, or future predictions, as well as financial, scientific, or mathematical calculations, and any other unsupported usage mentioned in the [Transparency Note for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?tabs=text). Currently, the service is exclusively supported in the United States and is available only in the English language.

AI-generated content can have mistakes, hence makers should inform the end users of their solution that the content generation by this model is created by AI in a transparent way. Clear communication of A generated content helps in avoiding overreliance. Makers should also infuse the possibility of the human review step to make sure that the AI generated content is accurate and appropriate before using it.

## What operational factors and settings allow for effective and responsible use of the system?

Content generated by the AI model is probabilistic in nature, and hence model responses could vary for the same prompt. The response generated might be incorrect or misleading and could cause unintended outcomes from the flow or app. For example, business customers might receive wrong or incorrect information, recommendations or support. Makers should implement meaningful human oversight within their flows and apps, as well as test their prompts for the potential to lead to generating harmful behaviors or prohibited content as listed in Microsoft Code of Conduct. Low-code developers should also be transparent about the use of AI in their apps and flows to inform the business user, indicating that the content is generated by AI. Additionally, generated responses might not match low code developer’s expectations due to length restrictions, content filtering, or model selection.

## What is the GPT model called, where is it hosted, and how can I access it?

The GPT-3.5 Turbo model is hosted on Azure OpenAI Service. To access it, you can use the Azure OpenAI Service REST APIs, Python SDK, or the web-based interface in Azure OpenAI Studio.

To learn more, go to [What's new in Azure OpenAI Service?](/azure/ai-services/openai/whats-new)

## Is my data used to train or improve the large language models available on AI Builder?

AI Builder prompts run on Azure OpenAI Service hosted by Microsoft. Customer data is not used to train or improve any of the Azure OpenAI Service foundation models. Microsoft does not share your customer data with a third party unless you’ve granted permission to do so. Neither customer prompts (input) with its grounding data nor the model responses (output) are used to train or improve Azure OpenAI Service foundation models.

## Is the content added to the 'Create text with GPT using a prompt' action publicly accessible?

The **About** tab for the action says, **This action provides access to your prompts leveraging GPT model running on Azure OpenAI Service.**

The prompts you add to the **Create text with GPT using a prompt** action in Power Automate are private by default. They're only visible and usable within your organization, not accessible to the world. The prompts are private and intended for internal use in your company.

Newly created prompts are private by default. This means they're visible and usable in Power Automate, Power Apps, and Microsoft Copilot Studio only by the person who created them. This allows the maker the time to test and evaluate them in apps or workflows and ensure their accuracy before sharing them.

If you want other users of the environment or groups to use your prompt in Power Apps or Power Automate, you need to share it.

To learn more, go to [Share your prompt](share-your-prompt.md).

## What are custom prompts and AI functions?

### Custom prompts

[Custom prompts](create-a-custom-prompt.md) give makers the freedom to instruct the large language model (LLM) to behave in a certain way, or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the LLM model into a flexible tool to accomplish various tasks.

**Example**

With a language model, a custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.

### AI functions

Prebuilt AI functions are preconfigured prompts created by the Microsoft team to assist makers in accomplishing common tasks easily. They offer ready-to-use AI capabilities across various use cases, which simplifies the maker experience to infuse intelligence in their solutions.

**Example**

A language model's prebuilt prompt could look like this:

Extract as a numbered list the action points from the: `[TextToExtract]`

In this case, the user only needs to supply the text in `[TextToExtract]` from which they want to extract action points. The prebuilt prompt takes care of the rest.

## Related information

- [Human review for automation with a prompt](azure-openai-human-review.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)

[!INCLUDE[footer-include](./includes/footer-banner.md)]
