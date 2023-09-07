

## Image Description prebuilt model (preview)

In this article
•	Licensing requirements
•	Role requirements
•	Supported language, format, and size
•	Use in Power Apps
•	Use in Power Automate


## What Image description is used for
**Image description** is a powerful prebuilt model that analyzes an image and generates a user-friendly description based on its visual features. 
**Auto-captioning** of images that uses machine learning to automatically generate descriptive text for images.
**Security and Surveillance** by describing presence or person or an activity in video frame, it is possible to monitor or identify threats easily.
**SEO (Search engine optimization)** by describing images in a webpage to make the page more discoverable.
**Chatbots** can describe a given image and reason over it, thereby giving the illusion of a multi-modal capability.
**The retail environment** can be used to describe a product and help with inventory management or restocking


> [!NOTE]
> Important
> This is a preview feature.
> Preview features aren’t meant for production use and may have restricted functionality. 
> These features are available before an official release so that customers can get early access and provide feedback.

## Licensing requirements
This feature is currently in preview, so using it will not deduct any AI Builder credits.

## Role requirements
Users need to have the Basic User role to consume the Image description prebuilt model.

## Supported files
- Document formats accepted: .JPG, .JPEG, .PNG, .BMP
- Maximum document size: 4MB
- The dimensions of the image must be greater than 50 x 50 pixels

## Model output
If a valid image is detected, the model will try to locate and extract the following properties.


|Property  |Note  |
|---------|---------|
|Description     |    Description of the image    |
|Tags     |   The list of tags extracted from the image      |
|Confidence score     |    A confidence score represents the accuracy of a prediction as a percentage     |

Supported languages of Description and Tags: English (United States)


## Use in Power Apps

**Explore image description**
1. Sign in to [Power Apps](https://make.powerapps.com).
1. In the left pane, select AI models > + New AI model
1. Under AI Models >Explore> Select Image description	
1. In the Generate description of an image window, select + Upload new.

Select predefined image samples to analyze or add your own image by selecting + Upload new button and see how the model analyzes your image.
You can also use the prebuilt model in an application > Select Use in an app.

:::image type="content" source="media/use-in-app.png" alt-text="Screenshot of the Generate description of an image Use in app.":::

Select the play Button at the top right of the page

:::image type="content" source="media/select-play-button.png" alt-text="Screenshot of the play button.":::


Select **Tap or click to add a picture** from your local device.
You should be able to analyze the image extracted from the model with a description and a confidence score as it is illustrated in the image below.


:::image type="content" source="media/image-extracted-from-model.png" alt-text="Screenshot of the image extracted from the model.":::


**Use the formula bar**
You can integrate your AI Builder image description models in Power Apps Studio by using the formula bar. 
'Image description'.Predict(UploadedImage1.Image)

For more information, see [Use Power Fx in AI Builder models in Power Apps (preview)]([https://make.powerapps.com](https://learn.microsoft.com/ai-builder/powerfx-in-powerapps)https://learn.microsoft.com/ai-builder/powerfx-in-powerapps).


## Use in Power Automate
To learn how to use the image description prebuilt model in Power Automate, go to Use Image description prebuilt model in Power Automate.
