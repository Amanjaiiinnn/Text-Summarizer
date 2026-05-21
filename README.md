# 📝 AI Text Summarizer Web App

A modern, fast, and light-weight web application for text summarization. Built using **FastAPI** on the backend and powered by a fine-tuned **HuggingFace T5 (Text-to-Text Transfer Transformer)** model. 

This repository contains both the web application interface and the Jupyter notebook used to train/fine-tune the model.

---

## 🚀 Key Features

* **Advanced Summarization:** Utilizes a fine-tuned T5 model for high-quality text extraction and synthesis.
* **Modern Web Interface:** A clean, responsive single-page UI styled with a warm orange-palette theme.
* **Hardware Acceleration Auto-detection:** Automatic detection and utilization of PyTorch acceleration (NVIDIA GPU **CUDA**, Apple Silicon **MPS**, or fallback to **CPU**).
* **Robust Data Cleaning:** Integrated regex preprocessing to strip HTML tags, remove carriage returns, and clean whitespace.
* **Asynchronous Requests:** Smooth, non-blocking asynchronous communication between the frontend and the FastAPI backend.

---

## 📁 Project Structure

```text
Text_Summarizer/
├── saved_model/                         # Fine-tuned T5 weights and configuration files
│   ├── config.json
│   ├── model.safetensors
│   ├── tokenizer.json
│   └── tokenizer_config.json
├── Text_Summarizer model Training.ipynb  # Jupyter Notebook used to train/fine-tune the T5 model
├── app.py                               # FastAPI backend application & API routing
├── index.html                           # Single-page frontend template (Jinja2)
├── requirements.txt                     # Python packages required for the project
└── README.md                            # Project documentation

```

## 🤖 Model & Training

The summarizer is powered by a **T5 Transformer** model:
* **Fine-Tuning:** The training pipeline is fully documented in [Text_Summarizer model Training.ipynb](Text_Summarizer%20model%20Training.ipynb). It includes steps for downloading a pre-trained T5 model, preprocessing data, training, evaluation, and saving model checkpoints.
* **Inference:** Loaded locally in the backend from the `./saved_model` directory to enable extremely fast offline summaries.

---

## ⚡ Tech Stack

* **Frontend:** Semantic HTML5, CSS (responsive design), Modern ES6 Javascript (`Fetch API`).
* **Backend:** [FastAPI] (Python ASGI Framework), [Jinja2 Templates] (HTML rendering).
* **Deep Learning Engine:** [PyTorch], [HuggingFace Transformers].



---

##  Model can't be uploaded due its size use the Text_summarizer model Training to create your own model .
