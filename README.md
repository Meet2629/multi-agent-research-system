# 🤖 Multi-Agent Research System

An AI-powered research assistant that automates the research process using multiple specialized AI agents. The system can search the web, collect relevant information, generate a structured research report, and review the generated content using an AI critic.

## 🚀 Live Demo

**Streamlit App:**
https://multi-agent-research-system-dhfudueyq5pmkpmjyvzz6m.streamlit.app/

---

## 📌 About the Project

Researching a topic manually can take a lot of time because it requires searching multiple websites, reading information, collecting important points, and preparing a final report.

This project automates these steps using a **multi-agent AI workflow**.

Instead of asking a single AI model to perform the entire task, the project separates the work into different stages:

```text
User
  ↓
Research Topic
  ↓
Search Agent
  ↓
Web Search
  ↓
Reader Agent
  ↓
Content Extraction
  ↓
Writer
  ↓
Research Report
  ↓
Critic
  ↓
Final Review
```

Each component has a specific responsibility, making the research process more organized and modular.

---

## ✨ Features

* 🔍 **Web Search** – Searches the internet for relevant information.
* 📄 **Content Reading** – Extracts useful information from web pages.
* ✍️ **AI Report Generation** – Generates a structured research report using an LLM.
* 🧐 **AI Critic** – Reviews the generated report and provides feedback.
* 🤖 **Multi-Agent Workflow** – Divides the research process into specialized tasks.
* 🖥️ **Streamlit Interface** – Simple web interface for entering research topics and viewing results.
* 📥 **Report Export** – Allows the generated research output to be downloaded.
* 🔐 **Environment Variables** – API keys are stored securely using environment variables.

---

## 🏗️ Project Architecture

The system follows a sequential research pipeline:

### 1. Search Agent

The Search Agent receives the user's research topic and uses the Tavily search API to find relevant web sources.

```text
Research Topic
      ↓
Search Agent
      ↓
Tavily API
      ↓
Search Results
```

### 2. Reader Agent

The Reader Agent processes the selected web pages and extracts useful text and information.

```text
Web URL
   ↓
Web Request
   ↓
HTML Content
   ↓
Content Extraction
   ↓
Useful Text
```

### 3. Writer

The collected research information is provided to an LLM, which generates a structured research report.

```text
Research Data
      ↓
Prompt
      ↓
LLM
      ↓
Research Report
```

### 4. Critic

The generated report is passed to a critic component that reviews the content and provides feedback.

```text
Research Report
      ↓
AI Critic
      ↓
Review & Feedback
```

---

## 🛠️ Tech Stack

### Programming Language

* Python

### AI & LLM

* LangChain
* Large Language Models (LLMs)
* Prompt Engineering
* AI Agents

### Search & Web Data

* Tavily API
* Requests
* BeautifulSoup

### Frontend / UI

* Streamlit

### Deployment

* Streamlit Cloud

---

## 📂 Project Structure

```text
multi-agent-research-system/
│
├── app.py
├── agents.py
├── pipeline.py
├── tools.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

### File Description

| File               | Purpose                                                  |
| ------------------ | -------------------------------------------------------- |
| `app.py`           | Streamlit application and user interface                 |
| `agents.py`        | AI agents and LLM chains                                 |
| `pipeline.py`      | Controls the research workflow                           |
| `tools.py`         | Search and web-related tools                             |
| `requirements.txt` | Python dependencies                                      |
| `.env`             | Stores API keys and environment variables                |
| `.gitignore`       | Prevents sensitive/unnecessary files from being uploaded |
| `README.md`        | Project documentation                                    |

---

## ⚙️ How It Works

When a user enters a research topic, the application follows these steps:

### Step 1 — User Input

The user enters a topic such as:

```text
Impact of Generative AI on Software Development
```

### Step 2 — Web Search

The Search Agent sends the topic to Tavily and receives relevant search results.

### Step 3 — Read Sources

The system accesses selected web pages and extracts useful content.

### Step 4 — Generate Report

The collected information is sent to an LLM with a structured prompt.

The LLM generates a research report containing relevant findings and information.

### Step 5 — Review

The Critic evaluates the generated report and provides feedback about the quality and completeness of the output.

### Step 6 — Display Result

The final research output and review are displayed through the Streamlit interface.

---

## 🔑 Environment Variables

Create a `.env` file in the project root directory.

Example:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
TAVILY_API_KEY=your_tavily_api_key
```

**Never upload your actual API keys to GitHub.**

Make sure `.env` is included in `.gitignore`.

---

## 💻 Installation

### 1. Clone the repository

```bash
git clone https://github.com/Meet2629/multi-agent-research-system.git
```

### 2. Navigate to the project

```bash
cd multi-agent-research-system
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

### 4. Activate the virtual environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure API Keys

Create a `.env` file:

```env
OPENROUTER_API_KEY=your_key_here
TAVILY_API_KEY=your_key_here
```

### 7. Run the application

```bash
streamlit run app.py
```

The application will open in your browser.

---

## 🎯 Example

### Input

```text
What is the future of Generative AI in software development?
```

### Processing

```text
Search
  ↓
Collect Sources
  ↓
Read Content
  ↓
Generate Report
  ↓
Critic Review
```

### Output

The application produces an AI-generated research report based on the collected information along with review/feedback from the critic stage.

---

## 🧠 What I Learned

Through this project, I learned how to:

* Build applications around LLMs.
* Create a multi-stage AI workflow.
* Work with AI agents and LangChain.
* Integrate external APIs into an AI application.
* Perform web search and content extraction.
* Design prompts for different AI tasks.
* Pass information between multiple AI components.
* Build a user interface using Streamlit.
* Manage API keys using environment variables.
* Deploy an AI application using Streamlit Cloud.

---

## 🔮 Future Improvements

Some possible improvements include:

* Adding more specialized research agents.
* Improving source verification and fact checking.
* Adding citation generation.
* Supporting PDF and document research.
* Adding conversation history.
* Improving report formatting.
* Adding more LLM providers.
* Adding parallel agent execution to reduce research time.

---

## 👨‍💻 Author

**Meet Vaghasiya**

Computer Engineering Graduate | Software Engineer | Full Stack Developer | AI/GenAI Enthusiast

### Skills

`Python` `C++` `JavaScript` `React` `Node.js` `Express.js` `MongoDB` `REST APIs` `LLMs` `RAG` `LangChain` `AI Agents`

---

## 📄 License

This project is created for educational and personal project purposes.
