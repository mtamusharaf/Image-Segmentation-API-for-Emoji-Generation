# Image-Segmentation-API-for-Emoji-Generation

This project provides an API for generating emoji-based images using a deep learning model for image segmentation. Built with FastAPI, the service processes image generation requests, applies segmentation to the images, and returns a URL to the generated image.

**Features**

* Image Generation: Generate emoji images from prompts using a pre-trained image segmentation model.
* GPU Optimization: The model utilizes GPU for efficient processing with threading and a lock to manage access.
* Authorization: Token-based authorization is used to manage access to the API.
* Image Segmentation: The API applies segmentation on the generated images to create unique emoji-like visuals.

**Installation**

Clone this repository:
**git clone https://github.com/mtamusharaf/Image-Segmentation-API-for-Emoji-Generation.git**
**cd Image-Segmentation-API-for-Emoji-Generation**

Install the required dependencies:
**pip install -r requirements.txt**

Run the API:
**uvicorn main:app --reload**

**API Endpoints**

POST /genemoji

Generate an emoji image.

* Request Body:
{
  "prompt": "Your emoji description",
  "guidance": 3.5,
  "seed": 12345,
  "strength": 1.0
}

* Response:
{
  "imageURL": "http://yourserver.com/images/unique_image.png"
}

GET /images/{filename}

Retrieve a generated image.
Example URL: **http://yourserver.com/images/{filename}**

**License**

This project is licensed under the MIT License - see the LICENSE file for details.
