
# Multi-Agent Research System

A Python-based **Multi-Agent Research System** built using **LangChain and Groq**. The system uses multiple specialized agents to search the web, extract useful information from webpages, review the collected content, and generate a structured research response.

## 🚀 Overview

Instead of relying on a single LLM call, this project divides the research process into multiple tasks handled by specialized agents.

The system follows this workflow:

```text
User Query
    ↓
Search Agent
    ↓
Tavily Web Search
    ↓
Reader / Scraper Agent
    ↓
BeautifulSoup Web Scraping
    ↓
Collected Research Information
    ↓
Reviewer / Writer
    ↓
Final Research Report
```

## ✨ Features

* Multi-agent research workflow
* Web search using **Tavily**
* Webpage content extraction using **BeautifulSoup**
* LLM-powered research analysis
* Automated review of collected information
* Structured final research response
* Uses **Groq** for fast LLM inference
* Built with **LangChain**
* Modular agent-based architecture

## 🛠️ Technologies Used

* **Python**
* **LangChain**
* **Groq**
* **Tavily**
* **BeautifulSoup**
* **python-dotenv**

## 📁 Project Structure

```text
Multi Agent System/
│
├── agents.py
├── tools.py
├── pipeline.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

### `agents.py`

Contains the different research agents and their prompts.

### `tools.py`

Contains tools used by the agents, such as:

* Tavily web search
* BeautifulSoup webpage scraping

### `pipeline.py`

Controls the overall multi-agent workflow and passes information between the agents.

### `requirements.txt`

Contains the Python dependencies required to run the project.

### `.env`

Stores API keys and configuration values.

## 🔄 How It Works

### 1. User Query

The user provides a research question.

Example:

```text
What are the latest applications of AI agents in software development?
```

### 2. Search Agent

The Search Agent sends the query to **Tavily** and retrieves relevant web search results.

```text
Research Question
       ↓
   Tavily Search
       ↓
Search Results
```

### 3. Reader / Scraper Agent

The Reader Agent processes the relevant webpages and extracts their useful text content using **BeautifulSoup**.

```text
Webpage URL
    ↓
BeautifulSoup
    ↓
Cleaned Web Content
```

### 4. Review

The collected information is passed to the reviewing stage, where the content can be checked for relevance and usefulness.

### 5. Writer

The Writer uses the collected research information to generate the final response in a readable and structured format.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd "Multi Agent System"
```

### 2. Create a virtual environment

Using Python:

```bash
python3 -m venv .venv
```

Activate it:

```bash
source .venv/bin/activate
```

Or, if you use `uv`:

```bash
uv venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If using `uv`:

```bash
uv pip install -r requirements.txt
```

## 🔑 Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key
GROQ_MODEL=your_groq_model
TAVILY_API_KEY=your_tavily_api_key
```

Replace the values with your own API keys.

**Do not commit the `.env` file to GitHub.**

Add it to `.gitignore`:

```gitignore
.env
.venv/
__pycache__/
*.pyc
.DS_Store
```

## ▶️ Running the Project

After activating the virtual environment, run:

```bash
python pipeline.py
```

Or:

```bash
python3 pipeline.py
```

The system will accept a research query and execute the multi-agent workflow.

## 🧠 Agent Architecture

The project separates responsibilities between specialized agents:

| Agent        | Responsibility                    | Tool          |
| ------------ | --------------------------------- | ------------- |
| Search Agent | Finds relevant information        | Tavily        |
| Reader Agent | Extracts webpage content          | BeautifulSoup |
| Reviewer     | Reviews collected information     | Groq LLM      |
| Writer       | Generates final research response | Groq LLM      |

This separation allows each agent to focus on a specific part of the research process.

## 📌 Example

### Input

```text
Research the impact of AI agents on modern software development.
```

### Processing

```text
Search Agent
    ↓
Searches multiple web sources
    ↓
Reader Agent
    ↓
Extracts webpage information
    ↓
Reviewer
    ↓
Checks collected information
    ↓
Writer
    ↓
Generates final research response
```

### Output

The system produces a structured research response based on the information collected from the web.

## 🎯 Project Objective

The main objective of this project is to understand and implement **AI agent-based workflows using LangChain**.

The project demonstrates how multiple specialized agents can collaborate to perform a research task instead of depending on a single LLM prompt.

## 📚 Concepts Learned

Through this project, the following concepts are explored:

* Large Language Models (LLMs)
* LangChain
* AI Agents
* Multi-Agent Systems
* Tool Calling
* Prompt Engineering
* Web Search
* Web Scraping
* Groq LLM
* Environment Variables
* Agent Orchestration
* Information Review and Synthesis

## 🔮 Future Improvements

Possible future improvements include:

* Add more specialized research agents
* Add source citation and verification
* Improve duplicate-source handling
* Add persistent conversation memory
* Generate PDF research reports
* Add a React frontend
* Expose the system through an API
* Add database storage for research history

## 👨‍💻 Author

**Ahamed Meeran Atheeq S**

Computer Science Engineering Student

Sri Krishna College of Technology

---

⭐ If you find this project useful, consider giving it a star.
