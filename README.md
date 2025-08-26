# Kenneth Mark's Personal AI Knowledge Worker
This project is a Retrieval-Augmented Generation (RAG) system built with LangChain and Python. It serves as an intelligent chatbot interface that allows seamless interaction with my personal knowledge base containing academic work, professional experiences, technical notes, and project documentation. The system processes multiple document formats to create semantic embeddings and provides contextually aware responses about my academic journey and professional development.

<br>

✨ **Key Features**

**Intelligent Document Retrieval**: Get detailed answers by querying a comprehensive personal knowledge base spanning academic coursework, professional projects, and technical documentation.

**Multi-Format Document Support**: Automatically processes and indexes multiple file formats including Markdown (.md), PDF (.pdf), Excel (.xlsx), Word documents (.docx), and plain text (.txt).

**Advanced RAG Pipeline**: Leverages LangChain's robust framework for document loading, intelligent text chunking, semantic embeddings, and conversational retrieval.

**Web-Based Chat Interface**: User-friendly Gradio-powered interface for natural conversation with the knowledge worker.

**Cost-Optimized Architecture**: Utilizes free-tier models via OpenRouter API with Mistral for efficient and accessible AI inference.

**Conversational Memory**: Maintains context across multi-turn dialogues for coherent and intelligent conversations.

<br>

📚 **Knowledge Base**
The core of this system is a personal knowledge base documenting Kenneth Mark's academic and professional journey. The RAG system has been trained on the following content areas, enabling detailed insights into academic work, technical skills, and career development:

**Academic Coursework & Assignments**
- Machine Learning fundamentals, characteristics, and future applications
- AI Student Performance Prediction System project proposal
- Various technical assignments and academic research

**Technical Documentation & Notes**
- Linux administration and command reference
- Networking protocols, subnetting, and system configuration
- Database design principles and SQL concepts
- Python programming and software development practices

**Professional Experience & Projects**
- Hotel store management standard operating procedures
- Inventory forecasting and optimization tools
- Cost analysis and tracking methodologies
- Supplier management and procurement guidelines
- Quality control checklists and compliance procedures

**Personal Development & Goals**
- Academic journey and learning milestones
- Career aspirations and professional objectives
- Technical skill development tracking
- Personal reflection on growth and achievements

<br>

⚙️ **Technical Stack**

**Language**: Python

**Framework**: LangChain for RAG pipeline implementation

**Vector Database**: ChromaDB for semantic search and retrieval

**Embeddings**: HuggingFace Transformers (all-MiniLM-L6-v2, 384 dimensions)

**LLM**: Mistral Small via OpenRouter API (free tier)

**User Interface**: Gradio for web-based chat experience

**Document Processing**: Unstructured, PyPDF, python-docx, pandas

<br>

🚀 **Getting Started**

**Prerequisites**
Ensure you have Python 3.8+ and git installed on your system before proceeding.

**1. Clone the Repository**
```bash
git clone https://github.com/kemaxx/
my-personal-rag-assistant.git

cd personal-ai-knowledge-worker
```

**2. Set up Virtual Environment**
It's recommended to use a virtual environment to manage dependencies.
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

**3. Install Dependencies**
Install all required libraries using pip:
```bash
pip install langchain langchain-community langchain-openai langchain-chroma

pip install chromadb sentence-transformers gradio python-dotenv

pip install pypdf unstructured python-docx pandas
```

**4. Environment Configuration**
Create a `.env` file in the project root with your OpenRouter API key:
```bash
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

**5. Prepare Knowledge Base**
Organize your documents in a `my_knowledge_base/` directory:
```
my_knowledge_base/
├── *.txt files (technical notes, quick references)
├── *.md files (documentation, personal stories)
├── *.pdf files (academic papers, assignments)
├── *.docx files (project proposals, formal documents)
└── *.xlsx files (data analysis, structured information)
```

**6. Run the Application**
Execute the main Python script to start the system:
```bash
python knowledge_worker.py
```
The Gradio interface will launch automatically and be available at `http://127.0.0.1:7863`.

<br>

🤝 **How to Use**

**Launch the Interface**: Start the application using the steps above. A web browser window will open with the chat interface.

**Ask Questions**: Type natural language questions into the text box, such as:
- "What are Kenneth's main academic achievements?"
- "Summarize the inventory management practices documented"
- "What machine learning concepts has Kenneth studied?"
- "Describe the hotel store operational procedures"

**Get Contextual Responses**: The system processes your query, retrieves relevant information from the knowledge base using semantic search, and provides detailed, referenced answers with conversational context.

**Continue Conversations**: The system maintains conversation memory, allowing for follow-up questions and deeper exploration of topics.

<br>

🔧 **System Configuration**

**Model Settings**
- **LLM Model**: `mistralai/mistral-small-3.2-24b-instruct:free`
- **Embeddings**: `sentence-transformers/all-MiniLM-L6-v2`
- **Vector Dimensions**: 384

**Text Processing**
- **Chunk Size**: 700 characters
- **Chunk Overlap**: 150 characters
- **Retrieval Limit**: Top 25 similar documents

**Current Knowledge Base Statistics**
- **Total Documents**: 9 processed documents
- **Vector Chunks**: 24 semantic chunks in database
- **Knowledge Domains**: Academic work, technical notes, professional experience, personal development

<br>

💡 **Use Cases**

**Academic Support**: Query specific topics across course materials, review ML concepts, and reference implementation approaches for projects.

**Personal Knowledge Management**: Access Linux commands, networking protocols, and study notes for quick reference and learning reinforcement.

**Professional Development**: Generate summaries of documented work experiences, track skill development, and align progress with career goals.

**Inventory & Operations Management**: Access documented store management practices, supplier information, and quality control procedures for operational insights.

<br>

🔮 **Future Enhancements**

**Technical Improvements**: Add OCR support for image documents, implement semantic filters by document type, and integrate citation tracking for better source attribution.

**User Experience**: Add conversation export functionality, implement query suggestions, and create real-time document upload capabilities.

**Knowledge Base Expansion**: Develop automated document ingestion pipeline, integrate with academic databases, and implement version control for knowledge evolution.

<br>

📄 **License**
This project is for personal use and educational demonstration purposes. The knowledge base contains personal academic and professional information belonging to Kenneth Mark.

---

*Created by Kenneth Mark - Final year HND Computer Science student at Kaduna Polytechnic, specializing in AI applications for real-world problem-solving and continuous learning.*