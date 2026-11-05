# 📄 AI Learning Coach – RAG Chatbot

An AI-powered chatbot built using Python, Streamlit, LangChain, and Groq. It allows users to upload PDF documents and ask questions based on their content.

The chatbot uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from uploaded PDFs and generate context-based answers.

## 🚀 Features

- **PDF Upload:** Upload one or more PDF documents.
- **Document Processing:** Extract text from PDFs and divide it into smaller chunks.
- **Text Embeddings:** Convert document chunks into numerical representations using Hugging Face embeddings.
- **Vector Database:** Store and retrieve document embeddings using ChromaDB.
- **Context-Based Answers:** Generate answers using retrieved information from uploaded documents.
- **Chat Interface:** Interact with the chatbot through a Streamlit chat interface.
- **Chat History:** Maintain conversation messages during the session.
- **Retrieved Context:** Display relevant information from uploaded documents.
- **Hallucination Control:** If the answer is unavailable in the retrieved context, the chatbot responds that it couldn't find the information.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Streamlit | Web application interface |
| LangChain | LLM integration and prompt management |
| Groq | AI-powered response generation |
| Hugging Face | Text embeddings |
| ChromaDB | Vector storage and similarity search |
| PyPDF | PDF document loading |
| python-dotenv | Environment variable management |

## 📂 Project Structure

```text
AI-Learning-Coach-RAG-Chatbot/
│
├── RAG_CHATBOT.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/AI-Learning-Coach-RAG-Chatbot.git
cd AI-Learning-Coach-RAG-Chatbot
```

### 2. Create a Virtual Environment

```bash
python -m venv env
```

Activate the environment:

**Windows:**

```bash
env\Scripts\activate
```

**Mac/Linux:**

```bash
source env/bin/activate
```

### 3. Install Dependencies

Create a `requirements.txt` file containing:

```text
streamlit
python-dotenv
langchain-community
langchain-text-splitters
langchain-huggingface
langchain-chroma
langchain-core
langchain-groq
sentence-transformers
pypdf
```

Install the required packages:

```bash
pip install -r requirements.txt
```

### 4. Configure Groq API Key

Create a `.env` file in the project folder:

```env
GROQ_API_KEY=your_groq_api_key
```

Replace `your_groq_api_key` with your actual Groq API key.

### 5. Run the Application

```bash
streamlit run RAG_CHATBOT.py
```

The application will open in your browser.

## 🔄 How It Works

1. **Upload PDFs:** The user uploads one or more PDF files.
2. **Document Loading:** PyPDFLoader extracts text from the uploaded documents.
3. **Text Chunking:** RecursiveCharacterTextSplitter divides the text into chunks of 1000 characters with 200 characters of overlap.
4. **Embedding Generation:** Hugging Face converts the text chunks into embeddings using `all-MiniLM-L6-v2`.
5. **Vector Storage:** Chroma stores the document embeddings for retrieval.
6. **Similarity Search:** The retriever finds the 3 most relevant document chunks for the user's question.
7. **Answer Generation:** Groq generates an answer using the retrieved context.
8. **Display Response:** The chatbot displays the answer in the Streamlit interface.

## 📖 How to Use

1. Open the AI Learning Coach application.
2. Upload one or more PDF files.
3. Wait for the documents to be processed.
4. Enter a question related to the uploaded documents.
5. View the AI-generated answer.
6. Continue asking questions through the chat interface.

## 🎯 Use Cases

- Understanding study materials and lecture notes.
- Asking questions about PDF documents.
- Researching information from uploaded reports.
- Preparing for exams using personal study resources.
- Quickly finding relevant information in lengthy documents.

## 🔮 Future Improvements

- Add support for Word documents and text files.
- Display page numbers and source citations in answers.
- Add a button to clear chat history and upload new documents.
- Support persistent vector storage.
- Allow users to download chat conversations.
- Add multilingual question-answering support.

## 👨‍💻 Author

Lakshay

## 📄 License

This project is created for educational and learning purposes.
