# Codex CLI - AI Code Editor with Ollama Integration

A powerful command-line interface for AI-powered code editing using local Ollama models, featuring RAG (Retrieval-Augmented Generation) capabilities and SQLite vector storage.

## ✨ Features

- 🤖 **Local Ollama Integration**: Use local AI models for code generation
- ✏️ **Intelligent Editing Agent**: Read, write, and update code files with AI assistance
- 🧠 **RAG System**: Context-aware code suggestions using vector embeddings
- 💾 **SQLite Vector Storage**: Efficient vector storage and retrieval
- 🎯 **Smart Context**: Understands codebase structure and patterns
- 🎨 **Rich CLI Interface**: Beautiful terminal interface with Rich and Typer
- 🔍 **Advanced Search**: Semantic search through your codebase
- 🔧 **Code Refactoring**: AI-powered code refactoring and optimization

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Ollama installed and running (https://ollama.ai/)
- codellama model (already exists as mentioned)

### Installation

1. **Clone and setup**:
```bash
git clone <your-repo>
cd aicodeeditor
python setup.py
```

2. **Initialize Codex**:
```bash
python main.py init
```

3. **Start coding with AI**:
```bash
# Generate new code
python main.py generate "Create a Python function to calculate fibonacci" --file fibonacci.py

# Edit existing code
python main.py edit main.py "Add error handling"

# Search your codebase
python main.py search "database connection"

# Explain code
python main.py explain main.py --detailed
```

## 🎨 GUI Interface

For a modern, Cursor-like experience, use the GUI version:

```bash
# Launch the GUI
python codex_gui.py

# Or use the launcher
python launch.py
```

### GUI Features:
- **🎨 Modern Dark Theme**: Beautiful interface with blue accents
- **📝 Multi-tab Editor**: Work with multiple files simultaneously
- **🤖 AI Integration**: Generate, edit, explain, and refactor code
- **🔍 RAG Search**: Semantic search through your codebase
- **📊 Statistics**: View codebase and database stats
- **⚙️ Model Selection**: Switch between different Ollama models

## 📖 Commands

### 🚀 Initialize
```bash
python main.py init [--path PATH] [--force]
```
Initialize the Codex database and index your codebase.

### ✨ Generate
```bash
python main.py generate PROMPT [--file FILE] [--language LANG] [--no-context]
```
Generate code using AI with optional RAG context.

### ✏️ Edit
```bash
python main.py edit FILE INSTRUCTION [--no-context] [--preview]
```
Edit existing files with AI assistance.

### 📖 Explain
```bash
python main.py explain FILE [--detailed]
```
Explain what code does with AI analysis.

### 🔍 Search
```bash
python main.py search QUERY [--limit N] [--threshold FLOAT] [--language LANG]
```
Search codebase using semantic similarity.

### 🔧 Refactor
```bash
python main.py refactor FILE TYPE [--target TARGET] [--preview]
```
Refactor code with AI assistance.

### 📊 Statistics
```bash
python main.py stats
```
Show codebase and database statistics.

### 🤖 Models
```bash
python main.py models
```
List available Ollama models.

### ⚙️ Configuration
```bash
python main.py config
```
Show current configuration.

## 🔧 Configuration

Edit `config.env` to customize settings:

```env
OLLAMA_BASE_URL=http://localhost:11434
OLLAMA_MODEL=codellama
CODEBASE_PATH=.
DATABASE_PATH=codex.db
EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2
MAX_CONTEXT_LENGTH=4096
```

## 🏗️ Architecture

```
src/
├── ollama_client.py    # Ollama API integration
├── editing_agent.py    # Code editing and manipulation
├── rag_system.py       # RAG implementation with SQLite
├── database.py         # SQLite database management
├── vector_store.py     # Vector embeddings and similarity search
└── cli.py             # Rich CLI interface with Typer
```

## 🎯 Use Cases

- **Code Generation**: Generate boilerplate, functions, classes
- **Code Editing**: Modify existing code with natural language instructions
- **Code Explanation**: Understand complex codebases
- **Code Search**: Find similar patterns across your codebase
- **Code Refactoring**: Improve code quality and structure
- **Documentation**: Generate documentation and comments

## 🔍 Examples

### Generate a REST API endpoint
```bash
python main.py generate "Create a FastAPI endpoint for user authentication" --file auth.py
```

### Add error handling to existing code
```bash
python main.py edit utils.py "Add comprehensive error handling and logging"
```

### Find all database-related code
```bash
python main.py search "database connection" --limit 20
```

### Refactor for better performance
```bash
python main.py refactor main.py optimize --preview
```

### Explain complex algorithm
```bash
python main.py explain algorithms.py --detailed
```

## 🛠️ Development

### Project Structure
```
aicodeeditor/
├── src/                 # Source code
├── main.py             # Entry point
├── setup.py            # Setup script
├── requirements.txt    # Dependencies
├── config.env          # Configuration
└── README.md           # This file
```

### Adding New Features
1. Extend the appropriate module in `src/`
2. Add CLI commands in `src/cli.py`
3. Update documentation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details.

## 🙏 Acknowledgments

- [Ollama](https://ollama.ai/) for local AI model serving
- [Rich](https://rich.readthedocs.io/) for beautiful terminal output
- [Typer](https://typer.tiangolo.com/) for CLI framework
- [Sentence Transformers](https://www.sbert.net/) for embeddings





python simple_cli.py generate "Create a complete Snake game in HTML with CSS and JavaScript. Include game board, snake movement, food generation, score tracking, and game over conditions. Make it responsive and visually appealing." --file snake_game.html --language html"# aicodeeditor" 
