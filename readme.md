# 📚 AI PDF Tutor - Multilingual Question Answering System

## 📖 About the Project
A multilingual question answering system that extracts knowledge from PDF documents using semantic search and generative AI.

## 🌟 Features

- **Multilingual Support** Answers questions in English + detected language (Telugu, Tamil, Hindi)
- **PDF Text Extraction** (both digital and scanned documents)
- **Semantic Chunk Retrieval** Finds most relevant text chunks using FAISS vector similarity
- **AI-Powered Answers** via Gemini 1.5 Flash
- **Web Interface** Simple Flask web app with user-friendly UI styling
- **OCR Fallback** for image-based PDFs

## 🛠️ Technologies Used
-**Component**	                    **Technology**	              **Purpose**
Backend	                             Python/Flask	        Web application framework
Embeddings	                     Sentence Transformers	      Text vectorization
Vector Search                         FAISS	                Efficient similarity search
Generative AI	                 Gemini 1.5 Flash	          Answer generation
PDF Processing	               PyPDF2 + pytesseract	        Text extraction from PDFs
Frontend	                       Bootstrap 5	                  Responsive UI
Deployment	                     flaskrun +Ngrok	          Temporary public tunneling

Ngrok is a tool that creates a temporary public tunneling to expose your local server to the internet.
embedding model **all-MiniLM-L6-v2** is used. it is a small, efficient, and fast model that can be used for text summarization, question answering, and other NLP tasks. L6 means 6 Transformer layers, v2 means version 2.0 of the model.

## Key Components:

-- **PDF Processor:**

Extracts text using PyPDF2

Falls back to OCR (pytesseract) for scanned PDFs

Splits text into overlapping chunks

-- **Semantic Search Engine:**

Uses Sentence Transformers (all-MiniLM-L6-v2) for embeddings

FAISS index for fast similarity search

Returns top 3 most relevant chunks

-- **Answer Generator:**

Gemini 1.5 Flash model for answer synthesis

Automatic language detection (Telugu, Tamil, Hindi, English)

Bilingual responses when non-English detected

-- **Web Interface:**

Simple file upload form

Question input field

Formatted answer display

## 🌐 Language Support

📘 English
📕 Telugu + English
📗 Tamil + English
📙 Hindi + English


### Prerequisites
- Python 3.8+
- Google API key ([Get one here](https://ai.google.dev/))
- Poppler utilities (`sudo apt-get install poppler-utils` on Ubuntu)
- Tesseract OCR (`sudo apt-get install tesseract-ocr`)


![alt text](Architecture_PDF_Tutor-1.png)