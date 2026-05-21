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

---

## 🛠️ Prerequisites & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/Text_Summarizer.git
cd Text_Summarizer
```

### 2. Set Up a Virtual Environment (Recommended)
This isolates the project dependencies from your system's global Python environment:

* **Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```
* **macOS / Linux:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🏃 Run the Application

Once your dependencies are installed, start the local development server with **Uvicorn**:

```bash
uvicorn app:app --reload
```

Once the server is running, open your web browser and navigate to:
* **Web App UI:** [http://127.0.0.1:8000](http://127.0.0.1:8000)
* **Interactive API Documentation (Swagger UI):** [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 🤖 Model & Training

The summarizer is powered by a **T5 Transformer** model:
* **Fine-Tuning:** The training pipeline is fully documented in [Text_Summarizer model Training.ipynb](Text_Summarizer%20model%20Training.ipynb). It includes steps for downloading a pre-trained T5 model, preprocessing data, training, evaluation, and saving model checkpoints.
* **Inference:** Loaded locally in the backend from the `./saved_model` directory to enable extremely fast offline summaries.

---

## ⚡ Tech Stack

* **Frontend:** Semantic HTML5, Vanilla CSS3 (responsive design), Modern ES6 Javascript (`Fetch API`).
* **Backend:** [FastAPI](https://fastapi.tiangolo.com/) (Python ASGI Framework), [Jinja2 Templates](https://jinja.palletsprojects.com/) (HTML rendering).
* **Deep Learning Engine:** [PyTorch](https://pytorch.org/), [HuggingFace Transformers](https://huggingface.co/docs/transformers/index).
* **Tokenizer Platform:** SentencePiece.
