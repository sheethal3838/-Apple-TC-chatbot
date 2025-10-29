# 📄 Apple Terms & Conditions RAG Chatbot

> An intelligent document question-answering system that makes Apple's terms and conditions accessible through natural language queries using Retrieval-Augmented Generation (RAG).

## 🚀 Overview

This project combines semantic search with natural language generation to help users understand complex legal documents. Users can ask questions about Apple's terms and conditions in plain English and receive accurate, contextual answers based on the actual document content.

## ✨ Features

- **📖 PDF Document Processing**: Extracts and processes Apple's terms and conditions PDF
- **🔍 Semantic Search**: Uses sentence transformers for intelligent content retrieval
- **🤖 AI-Powered Answers**: Generates concise summaries using DistilBART model  
- **🎯 High Accuracy**: Prevents hallucinations by grounding responses in source material
- **💻 Interactive Interface**: User-friendly Jupyter widget interface
- **⚡ Fast Retrieval**: Efficient similarity search using FAISS vector database

## 🛠️ Technologies Used

- **PyPDF2** - PDF text extraction
- **LangChain** - Text chunking and preprocessing
- **SentenceTransformers** - Embedding generation (all-MiniLM-L6-v2)
- **FAISS** - Vector similarity search
- **Transformers** - Text summarization (DistilBART)
- **IPyWidgets** - Interactive UI components

## 🏗️ System Architecture

PDF Document → Text Extraction → Chunking → Embeddings → FAISS Index
↓
User Query → Query Embedding → Similarity Search → Context Retrieval
↓
Retrieved Context → DistilBART Summarizer → Generated Answer

## 💡 How It Works

1. **Document Processing**: PDF is split into 1000-character chunks with 200-character overlap
2. **Embedding Generation**: Each chunk is converted to vector embeddings using sentence transformers
3. **Vector Storage**: Embeddings are stored in FAISS index for efficient retrieval
4. **Query Processing**: User questions are embedded and matched against document chunks
5. **Answer Generation**: Top 5 relevant chunks are summarized using DistilBART model

## 🎯 Key Technical Highlights

- **RAG Architecture**: Combines retrieval and generation for accurate responses
- **Semantic Search**: Goes beyond keyword matching to understand context
- **Chunking Strategy**: Optimized chunk size and overlap for better retrieval
- **Input Validation**: Handles model input limits (1024 tokens max)
- **Interactive UI**: Clean interface using Jupyter widgets

## 📊 Performance

- **Retrieval**: Sub-second search across entire document
- **Accuracy**: Responses grounded in actual document content
- **Coverage**: Processes complete terms and conditions document
- **Scalability**: Can handle documents up to 500+ pages

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Hugging Face** for transformer models
- **Facebook** for FAISS vector search
- **LangChain** for document processing utilities
- **Sentence Transformers** for embedding models

---

⭐ **Star this repo if you found it helpful!**
