# 🖼️ Image Caption Generation using CNN–LSTM with Attention

This project implements an **Image Captioning system** that automatically generates natural language descriptions for images using deep learning techniques. It combines **Convolutional Neural Networks (CNN)** for image feature extraction and **Long Short-Term Memory (LSTM)** networks with an **Attention mechanism** for caption generation.

---

## 📌 Project Overview

The goal of this project is to translate visual content into meaningful textual descriptions.  
The system learns to associate image features with words and generates captions **word-by-word**.

---

## 🧠 Model Architecture

- **Encoder (CNN)**
  - Uses pre-extracted image features from **InceptionV3**
  - Converts visual features into embedding representations

- **Attention Layer (Bahdanau Attention)**
  - Focuses on relevant image regions at each time step
  - Improves caption relevance and context awareness

- **Decoder (LSTM)**
  - Generates captions sequentially
  - Uses attention context and previously generated words

---

## 📂 Dataset

- **Dataset Used:** Flickr8k
- **Total Images:** 8,000
- **Captions:** 5 human-written captions per image
- **Content:** Everyday scenes with diverse objects and actions

---

## ⚙️ Workflow

1. Dataset preparation and caption cleaning  
2. Image feature extraction using InceptionV3  
3. Tokenization and sequence generation  
4. Encoder–Decoder model with attention  
5. Custom training loop with teacher forcing  
6. Model training and loss monitoring  
7. Caption generation on unseen images  

---

## 🏋️ Model Training

- Optimizer: **Adam**
- Loss Function: **Sparse Categorical Crossentropy (masked)**
- Epochs: **20**
- Batch Size: **64**
- Training performed using **Google Colab (GPU)**

---

## 📊 Results

- The model successfully generates meaningful captions
- Loss decreases consistently across epochs
- Attention mechanism improves caption quality

---

## ⚠️ Challenges

- Limited dataset size affects generalization
- High computational cost for training
- Difficulty in understanding complex scenes
- Limited vocabulary richness
- Evaluation metrics may not fully capture semantic quality

---

## 📁 Saved Weights

- `encoder.weights.h5`
- `decoder.weights.h5`

These weights can be loaded later for caption generation or evaluation.

---

## 🚀 Future Improvements

- Train on larger datasets (Flickr30k / MS COCO)
- Use Transformer-based architectures
- Improve evaluation using CIDEr and METEOR
- Deploy as a web application

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- Google Colab
- NumPy
- InceptionV3

---

## 📌 Conclusion

This project demonstrates a complete end-to-end implementation of an image captioning system, covering data preparation, model building, training, and inference, providing strong practical exposure to deep learning concepts.

---

## 👥 Team Members
1. Sai Surya
2. Aastha Das
3. Priyanshu Prakash Sharma
4. Hima Sajeesh Kumar
5. Vansh Bharadwaj
6. T J John

---

## 📄 License

This project is for **educational and academic purposes only**.
