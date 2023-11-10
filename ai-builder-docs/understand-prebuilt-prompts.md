---
title: Understand prebuilt prompts (preview)
description: Learn the types of prompts, how to use and test them, and more.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: conceptual
ms.date: 11/15/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Understand prebuilt prompts (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

A prebuilt prompt is a predefined prompt that's created and optimized by Power Platform to help makers easily accomplish common tasks. Prebuilt prompts are designed to simplify interactions by offering templates to see how to use generative AI for various use cases.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - View our [preview terms](https://powerplatform.microsoft.com/en-us/legaldocs/supp-powerplatform-preview/).
> - This capability is only available in United States region.
> - This capability might be subject to usage limits or capacity throttling.

The following prebuilt prompts are currently available in Copilot Studio, Power Automate and Power Apps.

  | Prebuilt prompts | Description |
| --- | --- |
| Classify text | Useful for tasks such as topic modeling, genre detection, and more |
| Summarize text | Useful for tasks such as studying, reviewing, or simplifying a text |
| Extract action points from text | Useful for tasks such as project management, meeting notes, or email summaries |
| Extract information from text | Useful for tasks such as named entity recognition, information extraction, or data mining |
| Respond to a complaint | Useful for tasks such as customer service, social media, or personal communication |
| Sentiment analysis of text | Useful for tasks such as sentiment analysis, text mining, or content evaluation |
| Reminder email message about a task | Useful for tasks such as project management, task delegation, or follow-up communication |

## Text prebuilt prompt

The Text prebuilt prompt can assist you in generating text.

### Classify text

This prebuilt prompt is designed to help you classify a given text into one of the categories that you specify. It works by analyzing the text and comparing it with the category list to find the best match. If the text is too short or doesn't fit any of the categories, it tell s you that it can't categorize the text.


#### Prompt for 'Classify text'

Categorize ***&lt;TextToClassify&gt;*** into these given categories: ***&lt;CategoryList&gt;*** . When the text has less than a couple of words, answer that you can't categorize the text.

#### Inputs and sample data for 'Classify text'

***&lt;TextToClassify&gt;***

A player is offside if, when the ball is passed to them, fewer than two opposing players are between them and the goal.

***&lt;CategoryList&gt;***

Sport, Technology, Political, Lifestyle and Unknown.

#### Response for 'Classify text'

Based on the given CategoryList, the text "A player is offside if, when the ball is passed to them, fewer than two opposing players are between them and the goal" can be categorized as "Sport" since it discusses a rule in a sports game.

### Summarize text

This prebuilt prompt is designed to help you write a short summary of a given text. It works by extracting the main points and key details from the text and rewriting them in a simpler way.. If the text is too short to have enough information to make a summary, it will tell you that it cannot summarize a text that is too short.


#### Prompt for 'Summarize text'

Summarize *&lt;**TextToSumarize&gt;*** in fewer than two paragraphs without adding new information. Write the summary in an eighth-grade level. When the text seems too short to make at least one paragraph of summary, answer that you can't summarize a text that is too short.

#### Inputs and sample data for 'Summarize text'

***&lt;TextToSumarize&gt;***

Dear John, I hope this message finds you well. As per our recent discussions, I've been diligently reviewing the latest data sets and leveraging the most advanced methodologies available in the market. Over the past quarter, there's been a noticeable shift in global dynamics, marked by a significant uptick in multifactorial outcomes. The interplay between core determinants and peripheral variables has intensified, leading to an intricate mesh of fluctuating paradigms. Several think tanks are currently deliberating on these patterns, emphasizing the importance of optimizing synergistic frameworks to achieve harmonious synchronization. On the technological front, there's been a surge in the integration of next-generation platforms with legacy systems. This confluence has precipitated an array of novel challenges, while simultaneously unlocking unprecedented opportunities. As stakeholders grapple with the evolving landscape, the emphasis has increasingly pivoted to sustainability, scalability, and agility. The quantifiable metrics derived from iterative feedback loops have yielded intriguing insights, underscoring the potential of adaptive resonance in strategic alignment. In conclusion, as we move forward, the imperative remains to stay abreast of these multifaceted developments. The nexus of innovation and tradition is reaching an inflection point, and the convergence of diverse trajectories is poised to reshape conventional wisdom. Your invaluable insights and feedback on this matter will be instrumental in ensuring that we navigate this transformative phase with optimal efficacy and finesse. Warm regards, Mona

#### Response for 'Summarize text'

In this message, the sender, Mona, informs John about their recent discussions and the work they have been doing. They mention reviewing data sets and using advanced methodologies to analyze global dynamics. They also discuss the integration of new technology with existing systems, which presents both challenges and opportunities. The message emphasizes the importance of staying updated on these developments and seeks John's insights and feedback to navigate this transformative phase effectively.

### Extract action points from text

This prebuilt prompt is designed to help you identify and list the action points from a given text. It works by scanning the text and finding the sentences that contain verbs, commands, or instructions that imply a task or a goal. It then extracts the relevant information from these sentences and formats them as a numbered list. It also preserves any links to documents or URLs that might be useful for completing the action points. If the text is too short to have any action points, it will tell you that it cannot extract actions from text that is too short.


#### Prompt for 'Extract action points from text'

Extract as a numbered list the action points from the ***&lt;TextToExtract&gt;*** . This list should preserve key information from the text, such as links to documents or URL that might be useful for individuals to complete the action point that is assigned to them. If text has less than a couple of words, answer that you can't extract actions from text that is too short.

#### Inputs and sample data for 'Extract action points from text'

***&lt;TextToExtract&gt;***

Dear John, I hope this email finds you well. I would like to take this opportunity to communicate some important updates and reminders regarding our team's goals and expectations for the quarter. As part of our strategic goals, you should provide a brief overview of ongoing projects and their progress. Remind your reports of any imminent deadlines and ask for updates on their progress. Share any recent learnings or best practices in the field that you think would benefit the team. Encourage open communication and ask for feedback on your leadership and any suggestions for improvement. Show appreciation for your reports' hard work and achievements. Let's work together to make this quarter a success. If you have any questions or concerns, please don't hesitate to reach out. Best regards, Mona

#### Response for 'Extract action points from text'

Action Points:

1. Provide a brief overview of ongoing projects and their progress.
1. Remind your reports of any imminent deadlines and ask for updates on their progress.
1. Share any recent learnings or best practices in the field that would benefit the team.
1. Encourage open communication and ask for feedback on your leadership and any suggestions for improvement.
1. Show appreciation for your reports' hard work and achievements.
1. Work together to make this quarter a success.
1. Reach out if you have any questions or concerns.

### Extract information from text

This prebuilt prompt is designed to help you extract the name of an entity from a given text. It works by analyzing the text and finding the words or phrases that match the entity type that you specify. It then returns the entity name as the output. If the text is too short or does not contain any entity of the given type, it will tell you that it cannot extract information.


#### Prompt for 'Extract information from text'

Extract ***&lt;EntityName&gt;*** from ***&lt;TextToExtract&gt;*** . When the text has less than a couple of words, answer that you can't extract information.

#### Inputs and sample data for 'Extract information from text'

***&lt;EntityName&gt;***

container numbers

***&lt;TextToExtract&gt;***

Good morning Robin, We are pleased to inform you that the shipment clearances for the four containers listed below have been completed as of January 12, 2023, and are ready for collection: 1. A 10 ft. container number JKL8783828 with registration number OPQ5000938374575937 2. A 10 ft. container number JKL8783829 with registration number OPQ5000938374575938 3. A 20 ft. container number JKL8783830 with registration number OPQ5000938374575939 The address for collection is 3520 Contoso Avenue, Chicago, IL 60609. If you have any questions or queries, please do not hesitate to contact us. We look forward to hearing from you. Warm regards, Margie's Travel

#### Response for 'Extract information from text'

Based on the provided text, the value that can be extracted is the container numbers. The four container numbers mentioned in the text are: <!--I see only three.-->

1. Container number JKL8783828
1. Container number JKL8783829
1. Container number JKL8783830

These containers have completed shipment clearances and are ready for collection. If you have any further questions or queries, please feel free to contact us.

Customer Service prebuilt prompt that can help you to handle customer complaints more effectively and efficiently.

### Respond to a complaint

This prebuilt prompt is designed to help you generate a response in an apologetic tone to a given text. It works by understanding the text and the emotions it conveys, and then crafting a response that is humble and creative. The response, if there is any, should restate the problem to acknowledge the issue and indicate that the problem will be addressed shortly. If the text is too short or does not require an apology, it will tell you that it cannot generate an answer.


#### Prompt for 'Respond to a complaint'

Try to generate a response in an apologetic tone to ***&lt;TextToRespond&gt;*** . Be humble and creative with the response. The response, if there is any, should restate the problem to acknowledge the issue. The response, if there is any, should indicate that the problem will be addressed shortly. When the text has less than a couple of words, answer briefly that you can't generate an answer.

#### Inputs and sample data for 'Respond to a complaint'

***&lt;TextToRespond&gt;***

I am writing to express my deep dissatisfaction regarding our recent order (\#123456), which was not delivered as promised. This missed shipment has severely impacted our business operations, resulting in delayed production, upset customers, and financial losses. We relied on your commitment to meet our needs and are truly disappointed with this oversight. Immediate resolution is expected to prevent further detriment to our business.

#### Response for 'Respond to a complaint'

I apologize for the inconvenience caused by the missed shipment of your recent order (\#123456). I understand the impact it has had on your business operations, including delayed production, upset customers, and financial losses. Please be assured that we take this matter seriously and are actively working to address the issue. We are committed to finding an immediate resolution to prevent any further detriment to your business. Thank you for bringing this to our attention, and we appreciate your patience as we work to rectify the situation.

### Sentiment analysis of text

This prebuilt prompt is designed to help you identify the sentiment of a given text and the possible reasons for it. It works by analyzing the text and finding the words or phrases that express an emotion or attitude. It then assigns a label of positive, neutral, or negative to the text based on the overall tone. It also identifies the possible subject causes for the sentiment assessment, such as the topic, the event, the person, or the situation that the text is about. If the text is too short or does not have any sentiment, it will tell you that it cannot identify the sentiment on a text that is too short.


#### Prompt for 'Sentiment analysis of text'

Identify the sentiment of ***&lt;TextToAssess&gt;*** below as positive, neutral, or negative. Identify the possible subject causes for the sentiment assessment. When the text has less than a couple of words, answer that you can't identify the sentiment on a text that is too short.

#### Inputs and sample data for 'Sentiment analysis of text'

***&lt;TextToAssess&gt;***

I recently purchased this broom, and I'd say I'm moderately pleased with its performance. While it does the job and sweeps adequately, there are a few minor areas where it could be improved for better cleaning efficiency. However, when it comes to value for money, I'm genuinely impressed! At this price point, it's hard to find a broom that offers such decent quality. If you're on a budget and looking for a good deal, this is a great option to consider. Would recommend for those who want good value without breaking the bank!

#### Response for 'Sentiment analysis of text'

The sentiment of the text is positive.

Possible subject causes for the sentiment assessment include:

- The performance of the broom
- Areas for improvement in cleaning efficiency
- Value for money
- Decent quality
- Being on a budget and finding a good deal
- Good value without breaking the bank Overall, the text expresses satisfaction with the broom's performance and highlights its value for money.

## Task prebuilt prompt that helps you identify task to-dos

### Reminder email message about a task

This prebuilt prompt is designed to help you create a high priority email message to remind a person about an assigned task using the information that you provide. It works by using the information content to generate a subject line, a salutation, a body, and a closing for the email message. The email message, if there is any, should identify key attributes of the task that the recipient needs to make quick decisions, such as the deadline, the deliverables, the expectations, or the consequences. If there are less than a couple of words, it will tell you that it cannot generate an email.

This prebuilt prompt can be useful for tasks such as project management, task delegation, or follow-up communication.

#### Prompt for 'Reminder email message about a task'

Try to create a high priority email message to remind ***&lt;PersonName&gt;*** about an assigned task message using the ***&lt;InformationContent&gt;*** . In the email message, if there is any, identify key attributes of the task that the recipient needs to make quick decisions. When there are less than a couple of words, answer that you can't generate an email.

#### Inputs and sample data for 'Reminder email message about a task'

***&lt;PersonName&gt;***

Kevin Sturgis <!--Is this name approved or PII?-->

***&lt;InformationContent&gt;***

Tone: business, polite, Task Name: Bug in the login experience, Task Number: 2869262, Due Date: 1/31/2023

#### Response for 'Reminder email message about a task'

Subject: Reminder: Bug in the login experience - Task \#2869262

Dear Kevin Sturgis,  <!--Is this name approved or PII?-->

I hope this email finds you well. I am writing to remind you about the assigned task regarding the bug in the login experience. The details of the task are as follows:

Task Name: Bug in the login experience

Task Number: 2869262

Due Date: 1/31/2023

As the due date is approaching, it is important to address this issue promptly. The bug in the login experience may be causing inconvenience to our users and needs to be resolved as soon as possible.

To make quick decisions, please consider the following key attributes of the task:

1. Impact: The bug affects the login process, potentially hindering user access to our platform.
1. Severity: The bug has been identified as a high priority issue, requiring immediate attention.
1. User Feedback: We have received reports from several users regarding difficulties in logging in, emphasizing the urgency of this task.
1. Potential Solutions: Our development team has suggested a few possible solutions, including code updates and server configuration changes.

I kindly request you to prioritize this task and allocate the necessary resources to resolve the bug. If you require any additional information or assistance, please do not hesitate to reach out to me or the development team.

Thank you for your attention to this matter. Your prompt action will greatly contribute to improving the user experience on our platform. Best regards, \[Your Name\] \[Your Position/Role\] \[Your Contact Information\]

## FAQ

This section contains frequently asked questions and their answers.

### What languages are supported in prebuilt prompt?

Currently, only English is the language supported.

### Do you store my data that I add in the input parameter?

No, we don't store the data that you add in the input parameter. Your data is used only to generate the output that you request, and it isn't saved or shared with anyone. Your data privacy is very important to us.

### Do I need technical skills to use prebuilt prompt?

You don't need to have advanced technical skills. You should have some basic knowledge of how to work with AI language models and how to craft effective prompts.

### What are prebuilt prompts and how can I use them?

Prebuilt prompts are ready-made templates that can help you generate different types of content or perform various tasks with text. You can use them by filling in the parameters with your own input and then running the prompt to get the output.

### What prebuilt prompts can they do?

We're offering different prebuilt prompts in various use cases.

Feel free to try it out with your data and find out if the response suits your needs.

- **Categorize**: This prompt can help you categorize a given text into one of the categories that you specify.
- **Summarize**: This prompt can help you summarize a given text in fewer than two paragraphs without adding new information.
- **Extract**: This prompt can help you extract information from a given text, such as action points, entity names, or sentiment.
- **Respond**: This prompt can help you generate a response to a given text in a specific tone, such as apologetic, humorous, or formal.
- **Create**: This prompt can help you create a high priority email message to remind a person about an assigned task using the information that you provide.

### Can I edit a prebuilt prompt?

No, this feature isn't currently supported. Feel free to create your own custom prompt.

### Can I restrict the use of a prebuilt prompt in my environment?

We don't have DLP like controls yet.But we are actively working on those for upcoming updates.

### How can I provide feedback or suggestions for improving a prebuilt prompt?

Yes, we want to hear from you. Feel free to submit your feedback for this product.
