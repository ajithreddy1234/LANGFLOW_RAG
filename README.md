# Multi-Agent Retrieval-Augmented Generation (RAG)

This project demonstrates a Multi-Agent Retrieval-Augmented Generation (RAG) system using LangChain agents. The system features role-based agents that collaboratively solve user queries through specialized tools such as web search, code execution, and mathematical computation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Example Use Cases](#example-use-cases)
- [Project Structure](#project-structure)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Overview

Retrieval-Augmented Generation (RAG) enhances language models by combining them with external data sources. This project extends the standard RAG pipeline by introducing multiple intelligent agents that interact via a shared communication mechanism to solve complex tasks.

Each agent is assigned a specific role and toolset, allowing them to behave differently and collaborate to reach optimal answers.

---

## Features

- Multi-agent system with distinct roles and behaviors
- Tool integration (search, code execution, LLM reasoning, mathematical operations)
- GroupChat and AgentExecutor powered by LangChain
- Environment variable support for OpenAI key management
- Extensible for custom tools and personas

---

## Architecture

### Agents

- **User Proxy Agent**: Simulates user input and initiates the group chat
- **Research Agent**: Performs web search via DuckDuckGo
- **Code Agent**: Executes Python code and returns results
- **Math Agent**: Solves numerical problems using symbolic computation
- **LLM Assistant Agent**: Handles general natural language reasoning

### Core Components

- **LangChain Agent**: Base for each specialized role
- **Toolset**: Configurable tools like `PythonREPLTool`, `DuckDuckGoSearchRun`
- **GroupChat**: Facilitates conversation between multiple agents
- **AgentExecutor**: Coordinates execution of agent interactions

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Multi-Agent-RAG.git
cd Multi-Agent-RAG
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate    # For Linux/macOS
venv\Scripts\activate.bat   # For Windows
```

### 3. Install Required Packages

If `requirements.txt` is available:

```bash
pip install -r requirements.txt
```

Otherwise, install dependencies manually:

```bash
pip install langchain openai duckduckgo-search
```

Optional for Jupyter use:

```bash
pip install notebook ipykernel
```

### 4. Set Environment Variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your-openai-api-key
```

Alternatively, set it in your terminal session:

```bash
export OPENAI_API_KEY=your-openai-api-key    # Linux/macOS
set OPENAI_API_KEY=your-openai-api-key       # Windows
```

---

## Usage

Open the notebook in Jupyter or VSCode and run the cells step-by-step.

```bash
jupyter notebook Multi_Agent_RAG.ipynb
```

You can modify agent behavior, tools, and input prompts directly in the notebook.

---

## Example Use Cases

- General knowledge and coding questions
- Math-related queries with real-time calculation
- Task decomposition between researcher and developer personas
- Retrieval-based Q&A with source citations
- Natural language reasoning and discussion with multiple perspectives

---

## Project Structure

```bash
.
├── Multi_Agent_RAG.ipynb     # Main demonstration notebook
├── requirements.txt          # Optional dependencies file
├── .env                      # Contains API keys (not included in version control)
└── README.md                 # Project documentation
```

---

## Future Work

- Integration with vector databases (Chroma, FAISS)
- PDF and document ingestion using LangChain loaders
- Streamlit or Gradio UI interface
- Advanced memory integration for agent persistence
- Custom evaluation metrics for multi-agent effectiveness

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or add.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Author

**Pochimireddy Ajith Reddy**  
Currently working on multi-agent AI systems, language model integrations, and physics-informed machine learning.  
Feel free to connect for collaboration or discussion.
