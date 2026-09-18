# 🎓 Multi-Modal Educational Q&A Chatbot

## 📌 Project Overview

The **Multi-Modal Educational Q&A Chatbot** is a Retrieval-Augmented Generation (RAG) application that allows users to ask questions about information contained in audio/video-based content.

The system first converts audio into text using speech-to-text, splits the resulting text into smaller chunks, generates semantic embeddings, stores them in a FAISS vector database, and retrieves the most relevant context for a user's question.

An OpenAI language model then uses the retrieved context to generate a concise response.

The project also includes a Gradio-based interactive chatbot interface.

## 🚀 Key Features

* 🎙️ Speech-to-text conversion
* 📝 Automatic transcript generation
* ✂️ Text chunking
* 🧠 Semantic text embeddings
* 🔎 FAISS similarity search
* 📚 Retrieval-Augmented Generation (RAG)
* 🤖 LLM-powered question answering
* 💬 Interactive Gradio chatbot interface
* 🎓 Educational content Q&A

## 🔄 System Workflow

```text
Audio / Video Content
        ↓
Speech-to-Text
        ↓
Generated Transcript
        ↓
Text Chunking
        ↓
Hugging Face Embeddings
        ↓
FAISS Vector Database
        ↓
User Question
        ↓
Similarity Search
        ↓
Relevant Context
        ↓
OpenAI LLM
        ↓
Generated Answer
        ↓
Gradio Chatbot
```

## 🛠️ Technologies Used

* Python
* OpenAI
* Whisper API
* LangChain
* Hugging Face
* Sentence Transformers
* FAISS
* Gradio
* RAG
* Vector Embeddings

## 🧠 RAG Pipeline

The application follows a Retrieval-Augmented Generation approach.

### 1. Speech-to-Text

The audio file is processed using OpenAI's speech-to-text functionality to generate a text transcript.

### 2. Text Chunking

The transcript is divided into smaller chunks using LangChain's `RecursiveCharacterTextSplitter`.

The notebook uses:

```python
chunk_size = 1000
chunk_overlap = 50
```

### 3. Embeddings

The project uses:

```text
sentence-transformers/all-MiniLM-L6-v2
```

to convert text chunks into numerical vector representations.

### 4. Vector Storage

The generated embeddings are stored using **FAISS**, enabling similarity-based retrieval.

### 5. Question Answering

When a user asks a question, the system retrieves the most relevant text chunks from the vector database.

The retrieved context is then passed to an OpenAI language model to generate the answer.

## 📂 Project Structure

```text
Multi-Modal-Educational-QA-Chatbot/
│
├── notebooks/
│   └── Audio_QnA_RAG_App.ipynb
│
├── sample/
│   └── README.md
│
├── README.md
├── requirements.txt
├── .gitignore
└── .env.example
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/Multi-Modal-Educational-QA-Chatbot.git
```

Move into the project directory:

```bash
cd Multi-Modal-Educational-QA-Chatbot
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## 🔐 API Configuration

Create a `.env` file in the project root:

```text
OPENAI_API_KEY=your_openai_api_key
HUGGING_FACE_HUB_TOKEN=your_huggingface_token
```

Never upload your `.env` file to GitHub.

## ▶️ Running the Project

Open:

```text
notebooks/Audio_QnA_RAG_App.ipynb
```

Run the notebook cells sequentially.

The notebook processes the audio content, creates the vector database, and launches the Gradio chatbot interface.

## 💬 Example Questions

The notebook demonstrates questions such as:

```text
What is the name of the customer?
```

and:

```text
Age of the customer?
```

Users can also enter their own questions through the Gradio chatbot.

## 🎯 Learning Outcomes

This project provided practical experience with:

* Retrieval-Augmented Generation
* Vector databases
* Semantic embeddings
* Similarity search
* LangChain
* FAISS
* Speech-to-text processing
* Large Language Models
* Prompt construction
* Gradio application development

## ⚠️ Important Notes

* The application requires valid API credentials for the services used.
* API keys must be stored securely as environment variables.
* The generated answers depend on the retrieved context and LLM output.
* LLM responses may vary between executions.
* The original notebook was developed in a Google Colab environment, so some file paths may need to be adjusted when running locally.

## 👨‍💻 Author

**Raj Yadav**

B.Tech Computer Science
AI/ML & Generative AI Enthusiast
