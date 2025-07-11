# 🤖 Gemini-Free RAG Chatbot with Together.ai, FAISS, and Gradio (Colab)

A fully open-source Retrieval-Augmented Generation (RAG) chatbot built for Google Colab.  
It allows users to upload documents (PDF, DOCX, TXT, Images) and ask natural language questions.  
Powered by Together.ai LLMs, FAISS for retrieval, and Gradio for the chat UI.

---

## 🚀 Features

- 📂 Upload multiple documents (PDF, DOCX, TXT, PNG, JPG)
- 🔍 Asks natural questions and retrieves relevant answers from content
- 📚 Shows document sources used in each answer
- 💬 Chat interface with Markdown rendering
- 📊 Automatically summarizes uploaded files
- 🧹 Reset chat history anytime
- ⬇ Export full chat transcript as a markdown file
- 🔐 100% Colab-compatible and free to run (no GPU required)

---


---

## 🧠 How It Works

1. **Upload file(s)** → PDF, DOCX, TXT, Images
2. **Text extracted** and split into 1000-character chunks
3. Each chunk is embedded using `MiniLM-L6-v2` and stored in **FAISS**
4. On question, relevant chunks are retrieved from FAISS
5. Prompt is built using retrieved context + question
6. Final answer is generated using **Together.ai LLMs** (e.g. Mistral-7B-Instruct)
7. Answer + source info is displayed in the chatbot



## 🔧 Setup in Google Colab

1. Open the Colab Notebook  
2. Run all cells from top to bottom  
3. Enter your Together.ai API Key ([get one free here](https://app.together.ai/settings/api))
4. Upload files and start chatting!

---

## 🔐 Environment Variables

| Variable            | Description             |
|---------------------|-------------------------|
| `TOGETHER_API_KEY`  | Your Together.ai API key |

---

## 📦 Requirements (auto-installed in Colab)
together
faiss-cpu
langchain
langchain-community
sentence-transformers
pymupdf
python-docx
pytesseract
Pillow
gradio

---

## 📚 Credits & Tech Stack

- LLM: [Together.ai](https://together.ai/)
- Embeddings: `all-MiniLM-L6-v2` (via `sentence-transformers`)
- Vector DB: FAISS
- Prompting & chaining: LangChain
- UI: Gradio Blocks
- File Parsing: PyMuPDF, python-docx, PIL, pytesseract

---

## 🧱 Future Ideas

- 🧠 Add memory (multi-turn conversation)
- 🧾 Show exact source chunks in answer
- 💾 Save/reload FAISS index
- ☁️ Deploy to Hugging Face Spaces / Streamlit

---

## 📜 License

This project is free to use under the MIT License.

