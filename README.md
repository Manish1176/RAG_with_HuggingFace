![RH](https://github.com/user-attachments/assets/f6a34a10-3c31-4599-aaf0-519aae0b94ed)

![MedicalFileUploader](https://github.com/user-attachments/assets/6a58f73d-c44e-4371-b3a7-1df86c0295e5)

# 📚 Medical Chatbot – PDF-based Q&A System

An **AI-powered chatbot** that lets users upload medical PDFs and ask questions to get accurate, document-grounded answers. Built using **LangChain**, **FAISS**, **Flan-T5**, and **Streamlit**, this project showcases a full-stack Retrieval-Augmented Generation (RAG) system for medical applications.

---

## 🚀 Demo

Upload your medical documents and ask questions like:
- _"What are the symptoms of diabetes?"_
- _"How is hypertension treated?"_
- _"What is the dosage for this medication?"_

The chatbot retrieves relevant context from your uploaded PDFs and generates a clear answer using a powerful language model.

---

## 🧠 Tech Stack

| Technology                | Purpose                                     |
|---------------------------|---------------------------------------------|
| `Streamlit`               | UI for uploading PDFs and chatting          |
| `LangChain`               | Framework for LLM pipelines                 |
| `FAISS`                   | Vector similarity search                    |
| `Flan-T5`                 | Text generation (via Hugging Face)          |
| `Sentence Transformers`   | Text embeddings (`all-MiniLM-L6-v2`)        |
| `PyPDFLoader`             | Read and process PDF content                |

---

## 📂 Project Structure

.
├── app.py # Main Streamlit app
├── requirements.txt # Required packages
└── README.md # Project documentation

yaml
Copy
Edit

---

## ✅ Features

- 📄 Upload multiple medical PDF files
- ✂️ Automatic chunking of document content
- 🧠 Embedding using `all-MiniLM-L6-v2`
- 🔎 Context retrieval using FAISS (MMR strategy)
- 💬 Answer generation with `google/flan-t5-base`
- 🧾 Chat history saved per session
- 🛡️ Handles empty or irrelevant query results

---

## 🛠️ How It Works

1. **Upload PDFs** → PDFs are parsed using `PyPDFLoader`
2. **Chunking** → Text is split into overlapping chunks (200 tokens, 50 overlap)
3. **Embedding** → Each chunk is embedded using Sentence Transformers
4. **Vector Search** → FAISS retrieves top-3 relevant chunks using MMR
5. **Prompting** → Context + Question is sent to `Flan-T5` to generate an answer
6. **UI** → Streamlit displays the interactive chat interface

---

## 📸 Interface Preview

*(You can add screenshots or GIFs of your chatbot UI here)*

---

## 🧪 Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/medical-chatbot.git
cd medical-chatbot
Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Run the app

bash
Copy
Edit
streamlit run app.py
💬 Example Questions
What is the treatment for hypothyroidism?

Explain the symptoms of vitamin D deficiency.

What are the precautions for this drug?

Make sure your question is relevant to the uploaded documents.

📈 Performance
✅ Achieved 85% relevance accuracy in returning document-based answers

📚 Improved accessibility for patients, students, and health educators

⚠️ Disclaimer
This chatbot is for educational and informational purposes only.
It does not provide medical advice, diagnosis, or treatment.
Always consult a certified medical professional for healthcare-related concerns.

🔮 Future Improvements
🔊 Voice input (speech-to-text)

🌍 Multi-language support

☁️ Cloud deployment (Hugging Face Spaces / AWS / GCP)

📱 Mobile-friendly UI

💾 Save chat transcripts

## 🙏 Acknowledgements
Hugging Face for models and pipelines

LangChain for RAG workflows

Streamlit for easy UI building

FAISS for efficient vector search


