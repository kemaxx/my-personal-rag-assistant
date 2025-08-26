# Personal AI Knowledge Worker

**A RAG-powered chatbot trained on my personal knowledge base for intelligent document retrieval and conversation**

## 📋 Overview

This Personal AI Knowledge Worker is a Retrieval-Augmented Generation (RAG) system that creates an intelligent chatbot interface to interact with my personal knowledge base. The system processes various document formats, creates semantic embeddings, and provides contextually aware responses about my academic work, notes, projects, and experiences.

## 🎯 Purpose

As a Computer Science student balancing academic studies with professional work as a hotel store manager, I needed a way to quickly access and query my scattered knowledge across multiple documents, notes, and projects. This knowledge worker serves as my personal AI assistant that understands my:

- Academic assignments and coursework
- Technical notes and study materials  
- Project documentation and code
- Personal experiences and learning journey
- Research papers and ML concepts
- Inventory management practices and store operations

## 🛠️ Technical Architecture

### Core Technologies
- **LangChain**: Document loading, text splitting, and RAG pipeline
- **Chroma DB**: Vector database for semantic search
- **HuggingFace Transformers**: Sentence embeddings (`all-MiniLM-L6-v2`)
- **OpenRouter API**: LLM inference with Mistral models
- **Gradio**: Web-based chat interface

### System Components

```
Documents → Document Loaders → Text Splitter → Embeddings → Vector Store → Retriever → LLM → Chat Interface
```

1. **Multi-format Document Loading**
2. **Intelligent Text Chunking** 
3. **Semantic Vector Embeddings**
4. **Conversational Memory**
5. **Web-based Chat Interface**

## 📁 Supported Document Types

The system automatically processes multiple file formats from the knowledge base:

- **📄 Text Files** (.txt) - Study notes, quick references
- **📝 Markdown** (.md) - Formatted documentation, life story
- **📊 PDF Documents** (.pdf) - Academic papers, assignments
- **📄 Word Documents** (.docx) - Project proposals, formal assignments
- **📈 Excel Files** (.xlsx) - Data analysis, structured information

## ⚙️ Key Configuration

```python
# Model Selection (Cost-optimized)
MODEL = "mistralai/mistral-small-3.2-24b-instruct:free"

# Text Processing
chunk_size = 700
chunk_overlap = 150

# Vector Configuration  
embeddings_model = "sentence-transformers/all-MiniLM-L6-v2"
vector_dimensions = 384

# Retrieval Settings
retrieval_documents = 25  # Top-K similar documents
```

## 🚀 Features

### Intelligent Document Processing
- **Multi-format Support**: Automatically handles PDF, DOCX, TXT, MD, XLSX files
- **Smart Chunking**: 700-character chunks with 150-character overlap for context preservation
- **Semantic Embeddings**: 384-dimensional vectors for accurate similarity matching

### Conversational Memory
- **Context Awareness**: Maintains conversation history for coherent multi-turn dialogues
- **Memory Buffer**: Preserves context across queries within a session

### Cost-Optimized Inference
- **Free Model Access**: Uses Mistral's free tier via OpenRouter
- **Efficient Retrieval**: Optimized vector search with 25-document retrieval limit

### Web Interface
- **Gradio Chat**: Clean, intuitive chat interface
- **Real-time Responses**: Instant query processing and response generation
- **Local Deployment**: Runs locally for privacy and control

## 📊 Current Knowledge Base Stats

- **Total Documents**: 9 processed documents
- **Vector Chunks**: 24 semantic chunks in database
- **Embedding Dimensions**: 384 per vector
- **Knowledge Domains**: Academic work, personal notes, project documentation, ML concepts

## 🔧 Installation & Setup

### Prerequisites
```bash
pip install langchain
pip install langchain-community
pip install langchain-openai
pip install langchain-chroma
pip install chromadb
pip install sentence-transformers
pip install gradio
pip install python-dotenv
pip install pypdf
pip install unstructured
pip install python-docx
```

### Environment Configuration
1. Create `.env` file:
```bash
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

2. Set up knowledge base directory:
```
my_knowledge_base/
├── *.txt files
├── *.md files  
├── *.pdf files
├── *.docx files
└── *.xlsx files
```

### Running the System
```python
# Load and process documents
python knowledge_worker.py

# Launch Gradio interface
# System will be available at http://127.0.0.1:7863
```

## 💡 Use Cases

### Academic Support
- **Assignment Research**: Query specific topics across multiple course materials
- **Concept Review**: Get explanations of ML concepts, networking protocols, database design
- **Project Planning**: Reference similar projects and implementation approaches

### Personal Knowledge Management
- **Quick Reference**: Access Linux commands, networking concepts, study reminders
- **Project Context**: Understand connections between different projects and learning areas
- **Progress Tracking**: Review academic achievements and learning milestones

### Professional Development
- **Skill Assessment**: Identify areas for improvement based on documented learning
- **Project Documentation**: Generate summaries of completed work and experiences
- **Goal Alignment**: Reference personal goals and track progress toward objectives

### Inventory & Store Management
- **Operational Insights**: Access documented inventory management practices and procedures
- **Supply Chain Information**: Query data about suppliers, stock levels, and procurement strategies
- **Quality Control**: Reference quality standards and compliance procedures
- **Process Optimization**: Analyze documented improvements and efficiency measures

## 🎓 Knowledge Domains Covered

Based on my uploaded knowledge base:

### Academic Coursework
- Machine Learning fundamentals and applications
- Operating Systems and Linux administration
- Database design and SQL concepts
- Networking protocols and subnetting
- Software engineering principles

### Personal Projects
- AI Student Performance Prediction System
- Market List inventory management tool
- Various academic assignments and prototypes

### Professional Experience
- Hotel store management insights
- Inventory optimization strategies
- Business process improvement
- Supply chain and procurement documentation
- Quality control and compliance procedures

### Technical Skills
- Python programming and project development
- AI/ML model implementation
- Database design and management
- System administration and networking

## 🔮 Future Enhancements

### Technical Improvements
- [ ] Add support for image documents (OCR integration)
- [ ] Implement semantic search filters by document type
- [ ] Add citation tracking for better source attribution
- [ ] Integrate with external knowledge sources

### User Experience
- [ ] Add conversation export functionality
- [ ] Implement query suggestions based on knowledge base
- [ ] Create document upload interface for real-time updates
- [ ] Add search analytics and usage insights

### Knowledge Base Expansion
- [ ] Automated document ingestion pipeline
- [ ] Integration with academic databases
- [ ] Real-time note synchronization
- [ ] Version control for knowledge evolution

## 🤝 About the Developer

Created by Kenneth Mark, a final-year HND Computer Science student at Kaduna Polytechnic, specializing in AI applications for real-world Nigerian contexts. This project reflects my philosophy that "no detail is insignificant" and demonstrates practical application of RAG systems for personal knowledge management.

## 📄 License

This project is for personal use and educational demonstration. The knowledge base contains personal academic and professional information.

---

*"This knowledge worker represents my commitment to leveraging AI for practical problem-solving and continuous learning."* - Kenneth Mark