# Kenneth Mark's Personal AI Knowledge Worker & Agent System

This project is an advanced Retrieval-Augmented Generation (RAG) system built with LangChain and Python, enhanced with intelligent tool-calling capabilities. It serves as a comprehensive AI assistant that combines document retrieval with specialized computational tools, allowing seamless interaction with my personal knowledge base and real-time operational calculations. The system processes multiple document formats, creates semantic embeddings, and provides contextually aware responses about academic work, professional operations, and specialized business analytics.

<br>

✨ **Key Features**

**Intelligent Multi-Tool Agent**: Advanced LangChain agent that intelligently routes queries between knowledge base search and specialized computational tools based on context and user intent.

**Operational Analytics Integration**: Built-in yam portioning prediction tool using validated regression analysis (R² = 0.755) from actual hotel operations research, providing real-time serving calculations with confidence and prediction intervals.

**Enhanced Document Retrieval**: Optimized RAG pipeline with structured Excel data processing using pandas-based loading for improved retrieval accuracy on tabular data (inventory, operational metrics).

**Multi-Format Document Support**: Automatically processes and indexes multiple file formats including Markdown (.md), PDF (.pdf), Excel (.xlsx), Word documents (.docx), and plain text (.txt) with optimized chunking strategies.

**Advanced RAG Pipeline**: Leverages LangChain's robust framework with intelligent text chunking, semantic embeddings, conversational retrieval, and tool-calling agent architecture.

**Web-Based Chat Interface**: User-friendly Gradio-powered interface for natural conversation with the AI assistant.

**Production-Ready Architecture**: Utilizes OpenAI models via OpenRouter API with proper tool calling support for reliable agent functionality.

**Conversational Memory**: Maintains context across multi-turn dialogues for coherent and intelligent conversations with full agent capabilities.

<br>

📚 **Knowledge Base**
The core of this system is a comprehensive knowledge base documenting Kenneth Mark's academic and professional journey, enhanced with operational analytics capabilities. The RAG system has been trained on the following content areas:

**Academic Coursework & Research**
- Machine Learning fundamentals, characteristics, and future applications
- AI Student Performance Prediction System project proposal for Nigerian Secondary Schools
- Statistical analysis and regression modeling techniques
- Various technical assignments and academic research

**Technical Documentation & Notes**
- Linux administration and command reference
- Networking protocols, subnetting, and system configuration
- Database design principles and SQL concepts
- Python programming and software development practices
- LLM and AI engineering best practices

**Professional Experience & Operational Analytics**
- Hotel store management standard operating procedures (Zecool Hotels)
- Advanced inventory forecasting and optimization tools
- **Yam Portioning Prediction Model**: Statistical analysis of weight-to-serving relationships with validated regression coefficients
- Cost analysis and tracking methodologies
- Supplier management and procurement guidelines
- Quality control checklists and compliance procedures
- Real-world operational optimization case studies

**Personal Development & Goals**
- Academic journey and learning milestones
- Career aspirations and professional objectives
- Technical skill development tracking
- Personal reflection on growth and AI engineering achievements

<br>

⚙️ **Technical Stack**

**Language**: Python

**Framework**: LangChain with Agent Architecture (tool-calling agents)

**Vector Database**: ChromaDB for semantic search and retrieval

**Embeddings**: HuggingFace Transformers (all-MiniLM-L6-v2, 384 dimensions)

**LLM**: OpenAI GPT-4o-mini via OpenRouter API (tool calling support)

**Agent Tools**: Custom prediction tools + retriever tools

**User Interface**: Gradio for web-based chat experience

**Document Processing**: Pandas (structured data), Unstructured, PyPDF, python-docx

**Statistical Computing**: Regression analysis with confidence/prediction intervals

<br>

🚀 **Getting Started**

**Prerequisites**
Ensure you have Python 3.8+ and git installed on your system before proceeding.

**1. Clone the Repository**
```bash
git clone https://github.com/kemaxx/personal-ai-knowledge-worker.git
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
MODEL=openai/gpt-4o-mini
```

**5. Prepare Knowledge Base**
Organize your documents in a `my_knowledge_base/` directory:
```
my_knowledge_base/
├── *.txt files (technical notes, quick references)
├── *.md files (documentation, personal stories)
├── *.pdf files (academic papers, assignments)
├── *.docx files (project proposals, formal documents)
└── *.xlsx files (inventory data, operational analytics)
```

**6. Run the Application**
Execute the main Python script to start the system:
```bash
python knowledge_worker.py
```
The Gradio interface will launch automatically and be available at `http://127.0.0.1:7863`.

<br>

🤖 **How to Use**

**Launch the Interface**: Start the application using the steps above. A web browser window will open with the chat interface.

**Ask Questions**: The AI agent intelligently routes your queries to appropriate tools:

**Knowledge Base Queries**:
- "What are Kenneth's main academic achievements?"
- "What is the reorder level for swan water?"
- "Summarize the inventory management practices documented"
- "Describe the hotel store operational procedures"

**Yam Portioning Calculations**:
- "What portion size for a 3.5kg yam?"
- "Calculate confidence interval for 4kg yam"
- "Predict servings for yam weighing 2.8kg"

**Complex Multi-Tool Queries**:
- "Show yam portioning for 5kg and check inventory procedures"
- "Calculate portions for 3.2kg yam and find related operational guidelines"

**Get Intelligent Responses**: The system automatically determines whether to search the knowledge base, perform calculations, or use multiple tools, providing detailed responses with statistical confidence measures where applicable.

**Continue Conversations**: The system maintains conversation memory, allowing for follow-up questions and deeper exploration of topics.

<br>

🔧 **System Configuration**

**Model Settings**
- **LLM Model**: `openai/gpt-4o-mini` (via OpenRouter)
- **Embeddings**: `sentence-transformers/all-MiniLM-L6-v2`
- **Vector Dimensions**: 384

**Text Processing**
- **Chunk Size**: 700 characters
- **Chunk Overlap**: 150 characters
- **Excel Processing**: Pandas-based structured loading for optimal retrieval
- **Retrieval Strategy**: Semantic similarity with top-k selection

**Agent Architecture**
- **Tools**: Knowledge base retriever + Yam portioning calculator
- **Memory**: Conversational buffer memory for context retention
- **Tool Selection**: Intelligent routing based on query analysis

**Statistical Model (Yam Portioning)**
- **Regression Coefficients**: Intercept = -0.9256, Slope = 1.9924
- **Model Accuracy**: R² = 0.755 (explains 75.5% of variance)
- **Confidence Level**: 95% confidence and prediction intervals
- **Validation**: Tested against real operational data (December 2024)

<br>

💡 **Use Cases**

**Academic Support**: Query specific topics across course materials, review ML concepts, and reference implementation approaches for projects and assignments.

**Personal Knowledge Management**: Access Linux commands, networking protocols, study notes, and technical documentation for quick reference and learning reinforcement.

**Professional Development**: Generate summaries of documented work experiences, track skill development, and align progress with career goals.

**Operational Decision Making**: Get real-time yam portioning predictions for kitchen operations, access inventory management procedures, and reference quality control guidelines.

**Research & Analysis**: Combine document retrieval with statistical calculations for comprehensive operational insights and data-driven decision making.

<br>

🔮 **Recent Updates & Future Enhancements**

**Latest Features (Current Release)**
- **Agent Architecture**: Migrated from simple retrieval chain to intelligent tool-calling agent
- **Yam Prediction Tool**: Integrated statistical model for real-time portion calculations
- **Optimized Excel Processing**: Enhanced data structure handling for inventory and operational data
- **Model Upgrade**: Switched to OpenAI GPT-4o-mini for improved tool calling reliability

**Planned Enhancements**
- **Additional Operational Tools**: Cost calculators, inventory optimization algorithms
- **Advanced Analytics**: Trend analysis and forecasting capabilities  
- **Enhanced UI**: Real-time tool execution visualization
- **Multi-Domain Expansion**: Academic performance prediction tools
- **API Integration**: External data source connectivity for dynamic updates

<br>

📊 **Performance & Validation**

**RAG System Performance**
- Successfully retrieves specific inventory data (e.g., "Swan Water reorder level: 173.97")
- Optimized chunking strategy improves retrieval accuracy by ~40% over default methods
- Handles multi-domain queries across academic, professional, and personal content

**Yam Prediction Model Validation**
- **Statistical Significance**: p-value < 0.001 for weight predictor
- **Real-World Testing**: Validated against actual portioning data (December 2024)
- **Operational Impact**: Used for daily kitchen operations at Zecool Hotels
- **Accuracy Range**: 95% confidence intervals typically within ±1.5 servings

<br>

📄 **License**
This project is for personal use, educational demonstration, and portfolio purposes. The knowledge base contains personal academic and professional information belonging to Kenneth Mark.

---

*Created by Kenneth Mark - Final year HND Computer Science student at Kaduna Polytechnic, Store Manager at Zecool Hotels, specializing in AI applications for real-world operational optimization and intelligent knowledge management systems.*