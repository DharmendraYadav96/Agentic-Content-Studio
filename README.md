# Agentic Content Studio

Agentic Content Studio is a multi-agent AI application that automates the complete blog creation workflow. Instead of relying on a single LLM prompt, the application breaks the task into multiple steps handled by specialized agents that collaborate to research, plan, write, review, and assemble a final blog article.

I built this project to understand how production-style Agentic AI systems are designed using LangGraph. The focus was on building a modular workflow where each agent has a clearly defined responsibility and shares information through a common state.

## Features

* Multi-agent workflow using LangGraph
* Blog planning from a user topic
* Web research using external search tools
* Automatic outline generation
* Blog writing with LLMs
* Content review and refinement
* AI-generated images for articles
* Markdown export
* Modular agent architecture
* Human review support before final output

## Workflow

```
User Input
    │
    ▼
Planner
    │
    ▼
Research
    │
    ▼
Outline
    │
    ▼
Writer
    │
    ▼
Reviewer
    │
    ▼
Image Generator
    │
    ▼
Markdown Output
```

Each agent receives the current workflow state, performs a specific task, updates the shared state, and passes control to the next agent.

## Project Structure

```
.
├── agents/
├── graph/
├── prompts/
├── utils/
├── output/
├── main.py
├── config.py
├── requirements.txt
└── README.md
```

## Tech Stack

* Python
* LangGraph
* LangChain
* OpenAI API
* Pydantic
* Tavily Search
* Markdown

## Getting Started

Clone the repository.

```bash
git clone https://github.com/<your-username>/agentic-content-studio.git
cd agentic-content-studio
```

Create a virtual environment.

```bash
python -m venv .venv
```

Activate it.

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

Install the required packages.

```bash
pip install -r requirements.txt
```

Create a `.env` file and add the required API keys.

```
OPENAI_API_KEY=your_api_key
TAVILY_API_KEY=your_api_key
```

Run the application.

```bash
python main.py
```

## Example

Input

```
Topic: How Agentic AI is Changing Content Creation
```

Output

* Research summary
* Blog outline
* Complete markdown article
* AI-generated images
* Final reviewed blog

## What I Learned

This project helped me understand:

* Building multi-agent workflows with LangGraph
* State management across agents
* Prompt engineering for specialized agents
* Tool calling and external search integration
* Designing modular AI applications
* Managing structured outputs using Pydantic

## Future Improvements

Some features I plan to add are:

* Long-term memory using a vector database
* Multiple LLM providers
* Streaming responses
* REST API
* Docker support
* Web interface
* Human approval checkpoints
* Automated SEO optimization

