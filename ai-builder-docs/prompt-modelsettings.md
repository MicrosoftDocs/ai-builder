---
title: Change the model version and settings
description: Learn about the settings in prompt builder.
author: Antoine2F
contributors:
  - chplanty
  - Phil-cmd
  - Antoine2F
  - antrod
  - v-aangie
ms.topic: article
ms.date: 08/07/2025
ms.author: antode
ms.reviewer: angieandrews
---

# Change the model version and settings

This article explains how to change the model version and settings in the prompt builder. The model version and settings can affect the performance and behavior of the generative AI model.

## Model selection

You can change the model by selecting **Model** at the top of the prompt builder. The dropdown menu allows you to select from the generative AI models that generate answers to your custom prompt.

The default model is GPT-4.1 mini. You can also use the more powerful GPT-4.1 model or o3 model. The versions of these models might change.  

In addition, we propose GPT-5 chat (preview) and GPT-5 reasoning (preview). Check availability of models by region in [Feature availability by regions for prompts](availability-region.md#prompts).

Using prompts in Power Apps or Power Automate consumes *AI Builder credits*, while using prompts in Microsoft Copilot Studio consumes *messages*. Learn more in [AI Builder licensing and credit management](credit-management.md).

### Models details

|GPT model  |Licensing rules   | Functionalities|
|-----------|------------------|----------------|
|GPT-4.1 mini <br> (Default model) | Charged at the **Basic** rate. <br> Consumes *messages* in Microsoft Copilot Studio (more information: [Message scenarios](https://go.microsoft.com/fwlink/?linkid=2307400)) and *AI Builder credits* in Power Apps and flows (more information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130))  | Trained on data up to June 2024. Context allowed up to 128K tokens. |
| GPT-4.1 | Charged at the **Standard** rate. <br> Consumes  *messages* in Microsoft Copilot Studio (more information: [Message scenarios](https://go.microsoft.com/fwlink/?linkid=2307400)) and *AI Builder credits* in Power Apps and flows (more information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)) | Trained on data up to June 2024. Context allowed up to 128K tokens.|
| o3 | Charged at the **Premium** rate. <br> Consumes  *messages* in Microsoft Copilot Studio (more information: [Message scenarios](https://go.microsoft.com/fwlink/?linkid=2307400)) and *AI Builder credits* in Power Apps and flows (more information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130))   | Trained on data up to June 2024. Context allowed up to 200K tokens. | 
| GPT-5 chat (preview) | Charged at the **Standard** rate. <br> Consumes  *messages* in Microsoft Copilot Studio (more information: [Message scenarios](https://go.microsoft.com/fwlink/?linkid=2307400)) and *AI Builder credits* in Power Apps and flows (more information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130))  | Trained on data up to Septembre 2024. Context allowed up to 400K tokens. |
| GPT-5 reasoning (preview) | Charged at the **Premium** rate. <br> Consumes  *messages* in Microsoft Copilot Studio (more information: [Message scenarios](https://go.microsoft.com/fwlink/?linkid=2307400)) and *AI Builder credits* in Power Apps and flows (more information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130))  | Trained on data up to October 2024. Context allowed up to 400K tokens. |

GPT-4o mini and GPT-4o continue to be used in U.S. government regions. These models follow licensing rules and offer functionalities comparable to GPT-4.1 mini and GPT-4.1, respectively.  

Choose between the models based on region availability, functionalities, and use cases. Check [Feature availability by regions for prompts](availability-region.md#prompts)  and the following [Models comparison](#models-comparison).

### Models comparison

| Factors                     | GPT-4.1 mini  (default)             | GPT-4.1                              | o3                                      | GPT-5 chat (preview)                  | GPT-5 reasoning (preview)            |
|---------------------------|---------------------------------------|--------------------------------------|-----------------------------------------|---------------------------------------|--------------------------------------|
| Cost                  | **Basic** pricing, more cost-effective| **Standard** pricing                 | **Premium** pricing                     |**Standard** pricing                   |   **Premium** pricing                |
| Performance           | Good for most tasks                   | Superior for complex tasks           | Trained for reasoning tasks             | Highest scores in document understanding and response accuracy|  Highest score in reasoning tasks like planning or complex analysis|
| Speed              | Faster processing                     | Might be slower due to complexity    | Slower, as it reasons before responding  | Enhanced, compared to GPT 4.1          | Slow, as it reasons before responding |
| Use cases            | Summarization, information tasks, image and document processing | Image and document processing, advanced content creation tasks |  Data analysis and reasoning tasks, image and document processing | More advanced document processing, responses requiring high accuracy | Handle highest  complexity of  data analysis and reasoning tasks |

### Decision narrative

When you need a cost-effective solution for moderately complex tasks, have limited computational resources, or require faster processing, choose GPT-4.1 Mini. It's ideal for projects with budget constraints and applications like customer support or efficient code analysis.

When you're dealing with highly complex, multimodal tasks that require superior performance and detailed analysis, choose GPT-4.1. It's the better choice for large-scale projects where accuracy and advanced capabilities are crucial. Another scenario where it's a better choice is when you have the budget and computational resources to support it. GPT-4.1 is also preferable for long-term projects that might grow in complexity over time.

For projects requiring advanced reasoning capabilities, the o3 model excels. It's suitable for scenarios that demand sophisticated problem-solving and critical thinking. The o3 model excels in environments where nuanced reasoning, complex decision-making, and detailed analysis are important.

GPT-5 chat and GPT-5 reasoning models are the most up-to-date model available, incorporating recent developments in AI about response accuracy, answers being more context aware, better document and image processing, or data analysis.

## Model settings

You can access the setting panel by selecting **...** > **Settings** at the top of the prompt builder. You can change the following settings:

- **Temperature**: Lower temperatures lead to predictable results, while higher temperatures allow more diverse or creative responses.
- **Record retrieval**: Number of records retrieved for your knowledge sources.
- **Include links in the response**: When selected, the response includes link citations for the retrieved records.

### Temperature

The slider allows you to select the temperature of the generative AI model. It varies between 0 and 1, and guides the generative AI model about how much creativity (1) vs deterministic answer (0) it should provide.

Temperature is a parameter that controls the randomness of the output generated by the AI model. A lower temperature results in more predictable and conservative outputs. To compare, a higher temperature allows for more creativity and diversity in the responses. It’s a way to fine-tune the balance between randomness and determinism in the model’s output.

By default, the temperature is 0, as in previously created prompts.

|Temperature  |Functionality| Use in|
|---------|---------|---------|
|0| More predictable and conservative outputs.<br>Responses are more consistent.| Prompts that require high accuracy and less variability.|
|1| More creativity and diversity in the responses. <br> More varied and sometimes more innovative responses.| Prompts that create new out-of-the-box content |

Adjusting the temperature can influence the model’s output, but it doesn't guarantee a specific result. The AI’s responses are inherently probabilistic and can vary even with the same temperature setting.

> [!NOTE]
> The temperature setting isn't available for the o1 model, so the slider is disabled when the o1 model is selected.

## Model updates

- During July 2025, the following models were updated:
  - GPT-4.1 mini model replaced GPT-4o mini model. Existing prompts previously running on GPT-4o mini now run on GPT-4.1 mini, using same **Basic** rates.
  - GPT-4.1 model replaced GPT-4o and is in GA. Existing prompts previously running on GPT-4o now run on GPT-4.1, using same **Standard** rates.
  - o3 model replaced o1 model and is in GA. Existing prompts previously running on o1 now run on o3, using same **Premium** rates.
- In August 2025, we added GPT-5 chat and GPT-5 reasoning to the model selector (preview).
