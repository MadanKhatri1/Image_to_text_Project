# Image Captioning with Transformers
This project implements a Streamlit web application for generating captions for uploaded images using a pre-trained transformer model.

Features
  1. Upload an image (.jpg, .jpeg, or .png)
  
  2. Generate captions using a pre-trained image captioning model
  
  3. Display the uploaded image and generated caption


# Demo

https://github.com/MadanKhatri1/Image_to_text_Project/assets/167626709/d66d6e25-663a-4d43-a253-37cbdaa485d9


# Setup the project
  1. Clone the repository: git clone [https://github.com/MadanKhatri1/Image_to_text_Project](https://github.com/MadanKhatri1/Image_to_text_Project.git)
  2. CD to the Image to text project.
  3. Run: **pip install -r requirements.txt**
  4. Then type: **streamlit run project.py**


# How it Works - Deep Dive

This application leverages the power of pre-trained transformer models and Streamlit to create an image captioning experience. Here's a breakdown of the underlying technology:

# 1. Pre-trained Transformer Models:

The application employs a pre-trained image captioning model from the nlpconnect library. This model is specifically designed to analyze images and generate textual descriptions.
Internally, the model likely consists of two sub-components:

  . Vision Transformer (ViT): This part of the model takes an image as input and extracts visual features like shapes, colors, and object arrangements.
  
  . GPT-2 Decoder: This section receives the extracted features from ViT and translates them into a sequence of words, forming the caption.

       
# 2. Image Captioning Pipeline:

The code defines a pipeline named image_captioning_pipeline. This pipeline simplifies the image captioning process. It takes care of:
  Preprocessing the uploaded image using the ViTImageProcessor.
  
  Feeding the preprocessed image features to the transformer model.
  
  Decoding the model's output into human-readable text using the GPT2Tokenizer.
  
  This pipeline essentially streamlines the interaction with the pre-trained model for caption generation.

# 3. generate_caption Function:
   
  This function is responsible for taking an uploaded image and generating a caption.
  
  It utilizes the image_captioning_pipeline to perform the image captioning task.
  
  The function also limits the caption length to a maximum of 50 words using the max_new_tokens argument.

# 4. Streamlit for User Interaction:

  Streamlit acts as the web development framework, providing the user interface and handling user interactions.
  It offers components like:
  
  1. st.title to set the app's title.

  2. st.write to display text descriptions.
   
  3. st.file_uploader to create a file upload button for images.
   
  4. st.image to display the uploaded image.



# 6. Putting it Together:
  When you upload an image, Streamlit captures it and passes it to the generate_caption function.

  This function uses the image captioning pipeline to process the image through the ViT and GPT-2 components of the pre-trained model.
  
  The generated caption is then returned and displayed alongside the uploaded image within the Streamlit app.
  
  This approach demonstrates how pre-trained models and frameworks like Streamlit can be combined to create interactive and intelligent web applications.
