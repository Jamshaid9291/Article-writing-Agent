# Article Writing Agent

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.54.0-red.svg)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-0.1+-green.svg)](https://www.langchain.com/)
[![LangGraph](https://img.shields.io/badge/LangGraph-1.0+-orange.svg)](https://www.langchain.ai/langgraph)

An AI-powered blog writing agent that leverages LangGraph for workflow orchestration and LangChain for seamless integration with multiple large language models (LLMs). This project automates the entire blog creation process, from planning and research to content generation and image placement.

## 🚀 Features

- **Multi-LLM Support**: Integrates with Groq, OpenAI GPT, and Google Gemini for flexible AI model selection
- **Automated Research**: Uses Tavily API for real-time web research and citation gathering
- **Image Generation**: Generates and places images using Google Gemini's multimodal capabilities
- **Streamlit Frontend**: User-friendly web interface for input and output
- **Modular Architecture**: Built with LangGraph for scalable, stateful workflows
- **Progressive Examples**: Jupyter notebooks demonstrating incremental improvements from basic to advanced implementations
- **Pydantic Schemas**: Strongly typed data models for reliability and maintainability

## 📋 Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## 🛠 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Jamshaid9291/Article-writing-Agent.git
   cd Article-writing-Agent
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file in the root directory with your API keys:
   ```env
   GROQ_API_KEY=your_groq_api_key
   OPENAI_API_KEY=your_openai_api_key
   GOOGLE_API_KEY=your_google_api_key
   TAVILY_API_KEY=your_tavily_api_key
   ```

## 🎯 Usage

### Running the Streamlit App

```bash
streamlit run blog-writing-agent/bwa_frontend.py
```

This launches a web interface where you can:
- Input blog topic and parameters
- Select AI models and research options
- Generate complete blog posts with images
- Download the final markdown and images as a ZIP file

### Using the Backend Directly

```python
from blog_writing_agent.bwa_backend import app

# Invoke the LangGraph workflow
result = app.invoke({
    "topic": "The Future of AI in 2026",
    "audience": "tech professionals",
    "tone": "informative",
    # ... other parameters
})
```

### Exploring Notebooks

The project includes 5 progressive Jupyter notebooks:
1. `1_bwa_basic.ipynb` - Basic LangGraph workflow
2. `2_bwa_improved_prompting.ipynb` - Enhanced prompting techniques
3. `3_bwa_research.ipynb` - Adding research capabilities
4. `4_bwa_research_fine_tuned.ipynb` - Fine-tuned research and content generation
5. `5_bwa_image.ipynb` - Full pipeline with image generation

## 📁 Project Structure

```
Article-writing-Agent/
├── blog-writing-agent/
│   ├── bwa_backend.py          # Main LangGraph workflow
│   ├── bwa_frontend.py         # Streamlit web interface
│   ├── 1_bwa_basic.ipynb       # Basic implementation
│   ├── 2_bwa_improved_prompting.ipynb
│   ├── 3_bwa_research.ipynb
│   ├── 4_bwa_research_fine_tuned.ipynb
│   ├── 5_bwa_image.ipynb       # Full implementation
│   ├── images/                 # Generated images storage
│   └── __pycache__/
├── images/                     # Static images
├── .env                        # Environment variables (gitignored)
├── .gitignore
├── requirements.txt
├── README.md
└── [Documentation files]
```

## ⚙️ Configuration

The agent supports various configuration options:

- **Blog Types**: Explainer, Tutorial, News Roundup, Comparison, System Design
- **Research Modes**: Closed-book, Hybrid, Open-book
- **Image Generation**: Configurable size, quality, and prompts
- **Word Count Targets**: Customizable per section

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [LangChain](https://www.langchain.com/) for the powerful LLM framework
- [LangGraph](https://www.langchain.ai/langgraph) for workflow orchestration
- [Streamlit](https://streamlit.io/) for the intuitive web interface
- [Tavily](https://tavily.com/) for research capabilities
- [Google Gemini](https://ai.google.dev/) for multimodal AI

---

**Built with ❤️ using cutting-edge AI technologies**