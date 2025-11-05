# 🖼️ Image Caption Generator using Deep Learning

This project is a **Deep Learning–based Image Caption Generator** built with **TensorFlow, Keras, and Streamlit**.  
It automatically generates meaningful captions for uploaded images using a pre-trained CNN + LSTM model.

## 🚀 Demo App

🌐 **Streamlit Web App:**  

> Upload an image and you will see the caption generate :
>
> 📦 image-caption-generator/
├── app.py                     # Streamlit frontend app
> 
├── best_model.h5 / best_model_fixed.keras   # Trained image caption model

├── tokenizer.pkl              # Tokenizer file (maps words <-> tokens)
├── Processed_Feature/
│   └── features.pkl           # Preprocessed VGG16 CNN features

├── captions.txt               # Original caption dataset (for tokenizer creation)

├── create_tokenizer.py        # Script to create and save tokenizer.pkl

├── requirements.txt           # Required Python dependencies

└── README.md                  # You’re reading it :)

🧠 How It Works: 

This model combines Computer Vision (VGG16) and Natural Language Processing (LSTM):

Feature Extraction:
Uses a pre-trained VGG16 CNN to extract image features (4096-d vector).

Sequence Modeling:
An LSTM-based sequence generator predicts the next word in a caption based on previous words and image context.

Beam Search / Greedy Decoding:
Generates captions word by word until the <endseq> token is reached.

Streamlit Frontend:
Lets you upload an image, view it, and display the generated caption in real time.


