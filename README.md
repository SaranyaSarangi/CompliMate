# CompliMate
**AI-powered compliance assistant with role-based search, semantic retrieval, and a Streamlit chat UI for quick access to regulatory information.**
Click to view demo👇🏻:
<p align="center">
  <a href="">
    <img src="" alt="Demo Preview" width="600"/>
  </a>
</p>

Or checkout the demo👉🏻 **[DEMO📹]()**

---

## 🚀 About the Project

- Your smart companion for quick lookups, clear insights and summarization from dense regulatory files.
- **CompliMate** was created as part of an internship program for **Reliance BP Mobility Limited (d/b/a Jio-bp)**.
- This project processes DOCX and PDF regulatory documents using python-docx and pdf2docx, converts their content into searchable embeddings with sentence-transformers,uses FAISS for fast similarity search to quickly find relevant sections and uses **Phi-2**'s quantized version (hugging face model) to generate AI summarization. It efficiently manages document metadata and caching to ensure smooth performance.

## ✨ Features

- Uploaded petroleum regulatory files (docx/pdf) are searched through, relevant information as per user queries are retrieved and answered by AI.
- Chatbot style responses
- Cloud-hosted: Runs on Streamlit Community Cloud for easy access without complex setup.
- Has lite version **[CompliMate Lite](https://github.com/SaranyaSarangi/CompliMate_Lite)** 

## 🛠️ Tech Stack

**Frontend & UI**
- [Streamlit](https://streamlit.io/) – for building the interactive user interface

**Document Processing**
- [python-docx](https://python-docx.readthedocs.io/) – for reading DOCX files
- [pdf2docx](https://pypi.org/project/pdf2docx/) – for converting PDF files to DOCX format(process includes conversion of PDF file to DOCX for better retrieval)

**Search & Retrieval**
- [FAISS](https://faiss.ai/) – for efficient similarity search
- [sentence-transformers](https://www.sbert.net/) – for generating text embeddings
- [difflib](https://docs.python.org/3/library/difflib.html) – for fuzzy matching of text

**Large Language Model (LLM)**
- LLaMA.cpp via llama_cpp_python – for running the Phi-2 (1.66 GB GGUF) model for context-based answer generation
- Hugging Face Hub – for downloading and caching the GGUF model when not stored locally

**Data Handling**
- `os`, `json`, `hashlib`, `pickle` – for file handling, metadata storage, caching, and hashing
- Role-based access mapping – for controlling which sections are visible to specific user roles (retail, non_retail)

**Version Control & Deployment**
- [Git](https://git-scm.com/) & [GitHub](https://github.com/) – for version control and code hosting
- [Streamlit Community Cloud](https://streamlit.io/cloud) – for deployment with auto-updates from GitHub

**Source code language**
- 🐍Python

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.10+ (preferably 3.11)
- Streamlit (`pip install streamlit`)
- Other dependencies the app uses (`pip install -r requirements.txt`)

### Installation

1. Clone the repo  
```bash
git clone https://github.com/SaranyaSarangi/CompliMate_Lite
cd your-repo-name
```

2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Run the app locally
```bash
streamlit run app.py
```
---

## 📦 Usage
- How users can use the app:
Users can enter words or phrases for their concerned topic and click 'Submit'.

- What output or feedback to expect
CompliMate Lite will return relevant sections from the files uploaded in RAG folder.

---

## 🛠️ Deployment
- This app is deployed via Streamlit Community Cloud.
- For live app visit : [CompliMate Lite](https://complimatelite-ccfsz8qvsmmjfqvrjkkbqq.streamlit.app/)
- App auto-updates whenever code is pushed to the main branch on GitHub.

You can also deploy locally or on your preferred cloud platform.

---

## 🤝 Contributing
Contributions are welcome! Please fork the repo, create a new branch for your feature/fix, and submit a pull request.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact
- Email – sharanya.sarangi@gmail.com
- LinkedIn - linkedin.com/in/saranya-sarangi-5b3745374
- Source Code : https://github.com/SaranyaSarangi/CompliMate_Lite

## 🎉 Acknowledgments
I would like to sincerely thank **Reliance BP Mobility Limited (d/b/a Jio-bp)** for providing me the valuable opportunity to work on this project as part of their internship program. Their support and guidance were instrumental in bringing this project to life.
