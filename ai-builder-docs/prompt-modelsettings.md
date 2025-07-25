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
ms.date: 07/16/2025
ms.author: chplanty
ms.reviewer: angieandrews
---

# Change the model version and settings

This article explains how to change the model version and settings in the prompt builder. The model version and settings can affect the performance and behavior of the generative AI model.

## Model version

You can change the model version by selecting **Model** at the top of the prompt builder. The dropdown menu allows you to select from the generative AI models that generate answers to your custom prompt.

The default model as of July 2025 is GPT-4.1 mini (general availability, or GA). You can also use the more powerful GPT-4o model (GA), o3 model (GA), or GPT 4.1 model (paid public preview). The versions of these models might change.

Using prompts in Power Apps or Power Automate consumes AI Builder credits, while using prompts in Microsoft Copilot Studio consumes messages. Learn more in [AI Builder licensing and credit management](/ai-builder/credit-management).

### Models details

|GPT model  |Status   |Licensing rules   | Functionalities| Region availabilities |
|---------|---------|---------|---------|---------|
|GPT 4.1 mini | GA - Default model	| Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) <br>Consumes message in Microsoft Copilot Studio. More information: [Message in Copilot Studio](https://go.microsoft.com/fwlink/?linkid=2307400)  | Trained on data up to June 2024. Context allowed up to 128K tokens. | [Feature availability by regions for prompts](availability-region.md)
| GPT 4o | GA | Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)  <br>Consumes message in Copilot Studio. More information: [Message in Copilot Studio](https://go.microsoft.com/fwlink/?linkid=2307400) | Trained on data up to October 2023. Context allowed up to 128K tokens. | [Feature availability by regions for prompts](availability-region.md)|
| o3 | GA | Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130).   <br>Consumes message in Copilot Studio. More information: [Message in Copilot Studio](https://go.microsoft.com/fwlink/?linkid=2307400)  | Trained on data up to June 2024. Context allowed up to 200K tokens. | [Feature availability by regions for prompts](availability-region.md)|
| GPT 4.1 | Paid public preview | Consumes credits in Power Apps and Power Automate. <br>Consumes message in Copilot Studio. <br> GPT 4.1 model is a Standard model and consumes same rates as GPT 4o. | Trained on data up to June 2024. Context allowed up to 128K tokens.| [Feature availability by regions for prompts](availability-region.md)|

Choose between the model based on capabilities and scenarios.

### Models comparison

| Factors                     | GPT-4.1 mini  (default)      | GPT-4o, GPT 4.1   | o3         |
|---------------------------|----------------------|--------------------|------------|
| **Cost**                  | Basic pricing, more cost-effective           | Standard pricing              | Premium pricing (paid preview) |
| **Performance**           | Good for most tasks                  | Superior for complex tasks           | Trained for reasoning tasks          |
| **Speed**                 | Faster processing                    | Might be slower due to complexity    | Slower as it reasons before responding |
| **Use cases**             | Summarization, information tasks, image and document processing | Image and document processing, as well complex content creation tasks |  Complex data analysis and reasoning tasks, image and document processing |

### Decision narrative

When you need a cost-effective solution for moderately complex tasks, have limited computational resources, or require faster processing, choose GPT-4.1 Mini. It's ideal for projects with budget constraints and applications like customer support or efficient code analysis.

When you're dealing with highly complex, multimodal tasks that require superior performance and detailed analysis, choose GPT-4o or GPT 4.1. It's the better choice for large-scale projects where accuracy and advanced capabilities are crucial. Another scenario where it's a better choice is when you have the budget and computational resources to support it. GPT-4o / 4.1 is also preferable for long-term projects that might grow in complexity over time.

For projects requiring advanced reasoning capabilities, the o3 model excels. It's suitable for scenarios that demand sophisticated problem-solving and critical thinking. The o3 model excels in environments where nuanced reasoning, complex decision-making, and detailed analysis are important. 

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

- During the first week of July 2025, 4.1 mini model replaced 4o mini model. Existing prompts previously running on 4o mini now run on 4.1 mini.
  - 4.1 mini rates in credits and messages are the same as 4o mini.  
  - 4.1 mini supports image and document input.  
- o3 model replaced o1 model and is in general availability (GA). Existing prompts previously running on o1 now run on o3.
- 4.1 model will be in general availability (GA) in the second half of July 2025, and will replace 4o model. Existing prompts running on 4o will run on 4.1 after this update.

