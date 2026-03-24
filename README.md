# 🖼️ Visual Caption Generator — CNN–LSTM with Attention

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat-square&logo=tensorflow)
![Dataset](https://img.shields.io/badge/Dataset-Flickr8k-green?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-yellow?style=flat-square&logo=googlecolab)
![License](https://img.shields.io/badge/License-Academic%20Use-lightgrey?style=flat-square)

> Automatically generate natural language descriptions for images using a CNN encoder, Bahdanau Attention, and an LSTM decoder — trained on the Flickr8k dataset.

---

## 📌 Overview

This project builds an end-to-end **Image Captioning** system that learns to associate visual content with meaningful textual descriptions. Given an image, the model generates a caption **word-by-word**, guided by an attention mechanism that focuses on relevant regions of the image at each step.

---

## 🧠 Model Architecture

```
Image ──► InceptionV3 (CNN Encoder) ──► Feature Embeddings
                                               │
                                     Bahdanau Attention
                                               │
                                       LSTM Decoder ──► Caption
```

| Component | Details |
|---|---|
| **Encoder** | InceptionV3 (pre-trained), outputs visual feature embeddings |
| **Attention** | Bahdanau Attention — focuses on relevant image regions per time step |
| **Decoder** | LSTM — generates captions sequentially using attention context |

---

## 📂 Dataset

| Property | Details |
|---|---|
| **Name** | Flickr8k |
| **Images** | 8,000 |
| **Captions** | 5 human-written captions per image |
| **Content** | Everyday scenes with diverse objects and actions |

---

## ⚙️ Workflow

```
1. Dataset preparation & caption cleaning
2. Image feature extraction using InceptionV3
3. Tokenization & sequence generation
4. Encoder–Decoder model with Attention
5. Custom training loop with Teacher Forcing
6. Model training & loss monitoring
7. Caption generation on unseen images
```

---

## 🏋️ Training Configuration

| Hyperparameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy (masked) |
| Epochs | 20 |
| Batch Size | 64 |
| Platform | Google Colab (GPU) |

---

## 📊 Results

- ✅ Model generates **meaningful and contextually relevant** captions
- 📉 Loss decreases **consistently** across all 20 epochs
- 🔍 Attention mechanism **visibly improves** caption quality and focus

---

## ⚠️ Challenges

- Limited dataset size affects generalization to unseen scenes
- High computational cost for training
- Difficulty understanding complex or abstract scenes
- Limited vocabulary richness
- Standard metrics (BLEU) may not fully capture semantic quality

---

## 💾 Saved Weights

The trained model weights are saved and can be reloaded for inference or evaluation:

```
encoder.weights.h5
decoder.weights.h5
```

**To load and generate a caption:**
```python
encoder.load_weights('encoder.weights.h5')
decoder.load_weights('decoder.weights.h5')
```

---

## 🚀 Future Improvements

- [ ] Train on larger datasets (Flickr30k / MS COCO)
- [ ] Replace LSTM with Transformer-based architecture
- [ ] Evaluate using CIDEr and METEOR metrics
- [ ] Deploy as a web application (Flask / Streamlit)

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.8+ | Core language |
| TensorFlow / Keras | Model building & training |
| InceptionV3 | Image feature extraction |
| NumPy | Data processing |
| Google Colab | GPU-accelerated training |

---

## 📌 Conclusion

This project demonstrates a complete end-to-end implementation of an image captioning system — from data preparation and feature extraction to model training and inference. It provides strong practical exposure to **multi-modal deep learning**, **sequence modeling**, and **attention mechanisms**.

---

## 👥 Team Members

| # | Name |
|---|---|
| 1 | Sai Surya |
| 2 | Aastha Das |
| 3 | Priyanshu Prakash Sharma |
| 4 | Hima Sajeesh Kumar |
| 5 | Vansh Bharadwaj |
| 6 | T J John |

---

## 📄 License

This project is intended for **educational and academic purposes only**.
