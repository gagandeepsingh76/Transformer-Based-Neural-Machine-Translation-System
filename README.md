# 🌍 Neural Machine Translation System

<p align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Keras](https://img.shields.io/badge/Keras-NLP-red)
![License](https://img.shields.io/badge/License-OpenSource-yellow)

</p>

A **Deep Learning Natural Language Processing project** built using **Python, TensorFlow, Keras, and KerasNLP** that translates:

- 🇬🇧 English Sentences  
- 🇫🇷 French Sentences  

The system uses a **Transformer Neural Network architecture** to understand language context and generate accurate translations.

---

# 📊 Model Training Performance

<p align="center">
<img width="500" src="https://github.com/user-attachments/assets/9a60d2c2-6066-4b83-ab24-9b650a96f9fe">
</p>

The graph shows the **training accuracy vs validation accuracy** of the model during training.

Observations:

- Training accuracy steadily increases
- Validation accuracy stabilizes around **75%**
- Indicates proper learning behaviour without severe overfitting

---

# 📑 Table of Contents

- Features  
- Tech Stack  
- Installation  
- Usage  
- Project Structure  
- How the System Works  
- Code Highlights  
- Example Translation  
- Limitations  
- Future Improvements  
- Author  
- License  
- Conclusion  

---

# ✨ Features

✔ English ➜ French translation  
✔ Transformer-based neural network  
✔ Text preprocessing and normalization  
✔ Tokenization and sequence padding  
✔ Encoder–Decoder architecture  
✔ Early stopping during training  
✔ Training accuracy visualization  
✔ Custom translation function  

---

# 🛠 Tech Stack

<div align="center">

| Technology | Purpose |
|------------|--------|
| Python | Main programming language |
| TensorFlow | Deep learning framework |
| Keras | Model building |
| KerasNLP | Transformer layers |
| Pandas | Dataset processing |
| NumPy | Numerical computation |
| Matplotlib | Visualization |
| Seaborn | Accuracy plotting |

</div>

---

# ⚙ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/neural-machine-translation.git
cd neural-machine-translation
```

---

### 2️⃣ Install Dependencies

```bash
pip install tensorflow keras keras-nlp pandas numpy matplotlib seaborn
```

---

# ▶ Usage

Run the training script:

```bash
python nmt_transformer.py
```

After training completes, test the translation model.

Example:

```python
translate_text("Hello world")
```

---

# 📁 Project Structure

```
neural-machine-translation
│
├── Data
│   └── en-fr.txt
│
├── nmt_transformer.py
├── README.md
```

---

# 🧠 How the System Works

<div align="center">

```
English Sentence
       ↓
Text Cleaning
       ↓
Tokenization
       ↓
Sequence Padding
       ↓
Transformer Encoder
       ↓
Transformer Decoder
       ↓
Softmax Prediction
       ↓
French Translation Output
```

</div>

---

# 💻 Code Highlights

### Tokenization

```python
en_tokenizer = Tokenizer()
en_tokenizer.fit_on_texts(en)
```

---

### Padding Sequences

```python
en_x = pad_sequences(en_sequences, maxlen=sequence_len, padding='post')
```

---

### Transformer Encoder

```python
encoder_output = TransformerEncoder(embed_dim, num_heads)(x)
```

---

### Transformer Decoder

```python
x = TransformerDecoder(embed_dim, num_heads)(x, encoded_seq_input)
```

---

### Model Compilation

```python
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
```

---

# 📊 Example Translation

Example outputs from the trained model:

```
its fall now       → cest desormais tombe
im losing          → je suis en train de perdre
i love winning     → jadore gagner
lets hit the road  → cassonsnous
```

Example test:

```
Input:  Hello world
Output: salut le monde
```

---

# ⚠ Limitations

- Model trained on limited dataset (50k sentences)
- Some translations may not be perfectly accurate
- Transformer models require large datasets for best results
- Training can be computationally intensive

---

# 🚀 Future Improvements

Possible upgrades for this project:

✔ Larger multilingual datasets  
✔ Beam search decoding  
✔ Attention visualization  
✔ Web-based translation interface  
✔ REST API for translation  
✔ Support for multiple languages  
✔ Mobile translation app  

---

# 👨‍💻 Author

**Gagandeep Singh**

Computer Science Student  
Interested in **Artificial Intelligence, NLP, and Machine Learning**

---

# 📜 License

This project is **open-source and available for educational purposes.**

---

# 📌 Conclusion

This project demonstrates how **Transformer-based Neural Networks** can be used for **machine translation tasks**.

Even with a relatively small dataset, the model can produce meaningful translations between English and French. With larger datasets and further optimization, this system could evolve into a **high-performance multilingual translation engine similar to modern AI translation services.**

---
