# Image Captioning using Deep Learning (PyTorch)

This project implements an **image captioning system using deep learning** with PyTorch.

The goal of the project is to automatically generate natural language descriptions for images using a **vision-language model**.

The project was developed as part of a **Deep Learning / Machine Learning course**.

---

# Problem Description

Image captioning is a task at the intersection of:

• Computer Vision  
• Natural Language Processing  

Given an image, the model must generate a sentence describing its contents.

Example:

Image:

A picture of a dog playing with a ball.

Generated caption:

"A dog playing with a ball in the grass."

This requires the model to understand both **visual features** and **language structure**.

---

# Model Architecture

The system follows a **Vision-Language architecture** composed of two main components.

### Image Encoder

A convolutional neural network extracts visual features from the image.

Libraries used:

• torchvision  
• CLIP vision encoder  

The encoder transforms the image into a **feature representation vector**.

---

### Caption Decoder

A sequence model generates the caption word by word.

The decoder:

• receives encoded image features  
• predicts the next word in the sentence  

The model learns the probability:
P(word_t | image, previous_words)


---

# Tokenization

Text preprocessing is performed using **SentencePiece**, which converts text into subword tokens.

This improves vocabulary coverage and training stability.

---

# Training Pipeline

The training pipeline includes:

1️⃣ Dataset loading using PyTorch `Dataset` and `DataLoader`

2️⃣ Image preprocessing using `torchvision.transforms`

3️⃣ Feature extraction from the encoder

4️⃣ Caption generation using the decoder

5️⃣ Loss computation and backpropagation

---

# Evaluation Metrics

The generated captions are evaluated using:

• **BLEU Score**

Measures similarity between generated captions and reference captions.

• **BERTScore**

Uses contextual embeddings to measure semantic similarity.

---

# Technologies Used

• Python  
• PyTorch  
• Torchvision  
• CLIP  
• SentencePiece  
• TorchMetrics  
• NumPy / Pandas  

---

# Running the Notebook

Open the notebook:
Image_Captioning_Project.ipynb


Run all cells sequentially.

The notebook contains:

• dataset preprocessing  
• model definition  
• training loop  
• evaluation  
• visualization

---

# Applications

Image captioning systems are used in:

• Assistive technologies for visually impaired users  
• Image search engines  
• Content indexing  
• Autonomous systems  
• Multimedia understanding

