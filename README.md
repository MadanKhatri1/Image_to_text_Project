# Image Captioning with Transformers
This project implements a Streamlit web application for generating captions for uploaded images using a pre-trained transformer model.

Features
  1. Upload an image (.jpg, .jpeg, or .png)
  
  2. Generate captions using a pre-trained image captioning model
  
  3. Display the uploaded image and generated caption


# Setup the project
  1. Clone the repository: git clone [https://github.com/MadanKhatri1/Image_to_text_Project](https://github.com/MadanKhatri1/Image_to_text_Project.git)
  2. CD to the Image to text project.
  3. Run: **pip install -r requirements.txt**
  4. Then type: **streamlit run project.py**



# How it works:

The application utilizes pre-trained deep learning models from the Transformers library to understand and describe visual content. Here's a simplified breakdown:

  Pre-trained Transformer Models:
    The application employs a pre-trained image captioning model from the nlpconnect library. This model is specifically designed to analyze images and generate textual descriptions.
    Internally, the model likely consists of two sub-components:
    Vision Transformer (ViT): This part of the model takes an image as input and extracts visual features like shapes, colors, and object arrangements.
    GPT-2 Decoder: This section receives the extracted features from ViT and translates them into a sequence of words, forming the caption.

  Streamlit: This framework makes it easy to create web apps in Python. It provides components for user interaction and displaying information.
  
Open the application in your web browser.
  1. Click "Choose an image..." and select an image from your computer.
  2. Click "Upload".
     
The app will process the image and generate a caption.

You'll see the uploaded image alongside the generated caption.

This application is a great example of how artificial intelligence can be used for creative tasks like image captioning.
