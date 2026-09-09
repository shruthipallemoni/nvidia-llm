# NVIDIA NIM Document Q&A

A Streamlit app that loads the PDFs in `us_census/`, creates a FAISS vector store with NVIDIA embeddings, and answers questions with the NVIDIA NIM Llama 3 model.

## Requirements

- Python 3.10 or newer
- An NVIDIA API key from [build.nvidia.com](https://build.nvidia.com/)

## Setup

Create and activate a virtual environment, then install the dependencies:

```powershell
python -m venv .venv
.\\.venv\\Scripts\\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Create a local `.env` file from `.env.example` and add your key:

```powershell
Copy-Item .env.example .env
```

Edit `.env` so it contains:

```text
NVIDIA_API_KEY=your_nvidia_api_key
```

## Run

```powershell
python -m streamlit run app1.py
```

Click **Documents Embedding** once after the app opens, then enter a question.

The PDF files in `us_census/` are included in this repository and are loaded locally. Do not commit `.env` or any API keys.

## GitHub

```powershell
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git push -u origin main
```