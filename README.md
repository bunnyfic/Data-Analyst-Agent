AI Data Analyst Agent

An LLM-Powered Multi-Agent System for Automated Data Analysis

<p align="center">
  <img src="https://img.shields.io/badge/Python-2E7D32?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/LangGraph-2E7D32?style=for-the-badge&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-2E7D32?style=for-the-badge&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI_API-2E7D32?style=for-the-badge&logo=openai&logoColor=white" />
</p><p align="center">
  <img src="https://img.shields.io/badge/Pandas-388E3C?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-388E3C?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Plotly-388E3C?style=for-the-badge&logo=plotly&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-388E3C?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-388E3C?style=for-the-badge&logo=streamlit&logoColor=white" />
</p>---

1. Overview

The AI Data Analyst Agent is an intelligent, LLM-powered multi-agent system designed to automate the end-to-end data analysis process through natural language interaction.

The system integrates Large Language Models (LLMs), agent orchestration frameworks and conventional data science libraries to perform analytical tasks with minimal manual intervention.

Users can upload structured datasets and interact with the system through natural language queries. The system coordinates specialised agents to perform data preprocessing, exploratory data analysis, statistical analysis, visualisation and analytical report generation.

The project explores the application of Generative AI and Agentic AI in automating traditional data science workflows.

2. Objectives

- Develop an autonomous multi-agent system for data analysis.
- Integrate Large Language Models with conventional data science workflows.
- Automate data preprocessing and exploratory analysis.
- Implement intelligent tool selection and execution.
- Generate data-driven insights and interactive visualisations.
- Develop an extensible architecture for AI-assisted analytics.

3. Core Functionalities

Module| Description
Natural Language Interface| Accepts analytical queries in natural language.
Automated Data Cleaning| Identifies missing values, duplicates and inconsistencies.
Exploratory Data Analysis| Performs descriptive statistics and data exploration.
Statistical Analysis| Performs statistical computations and relationship analysis.
Data Visualisation| Generates interactive charts and graphical representations.
Trend and Anomaly Detection| Identifies patterns, trends and unusual observations.
Report Generation| Produces structured analytical reports and insights.

4. Multi-Agent Architecture

The system follows a modular multi-agent architecture orchestrated through LangGraph. Each agent is assigned a specialised analytical responsibility, while a central supervisor coordinates task execution and information exchange.

Agent Modules

01. Supervisor Agent

- Interprets user instructions.
- Determines the analytical workflow.
- Assigns tasks to specialised agents.
- Coordinates execution and integrates outputs.

02. Data Cleaning Agent

- Detects missing values and duplicate records.
- Identifies inconsistent data.
- Applies appropriate preprocessing techniques.
- Validates data quality.

03. Exploratory Data Analysis Agent

- Examines dataset structure and characteristics.
- Computes descriptive statistics.
- Identifies distributions and correlations.
- Generates exploratory insights.

04. Statistical Analysis Agent

- Performs statistical computations.
- Conducts hypothesis testing where appropriate.
- Identifies significant relationships.
- Interprets analytical findings.

05. Visualisation Agent

- Selects appropriate visualisation techniques.
- Generates interactive charts.
- Represents statistical findings graphically.
- Produces visual summaries.

06. Report Generation Agent

- Consolidates analytical outputs.
- Summarises findings and observations.
- Generates actionable insights.
- Produces comprehensive analytical reports.

5. System Architecture

flowchart TD
    A[User] --> B[Streamlit Interface]
    B --> C[Supervisor Agent]

    C --> D[Data Cleaning Agent]
    C --> E[EDA Agent]
    C --> F[Statistical Analysis Agent]

    D --> G[Shared Analysis State]
    E --> G
    F --> G

    G --> H[Visualisation Agent]
    H --> I[Report Generation Agent]
    I --> J[Final Analytical Output]

    style A fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20
    style B fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20
    style C fill:#c8e6c9,stroke:#2e7d32,color:#1b5e20
    style D fill:#f1f8f2,stroke:#388e3c,color:#1b5e20
    style E fill:#f1f8f2,stroke:#388e3c,color:#1b5e20
    style F fill:#f1f8f2,stroke:#388e3c,color:#1b5e20
    style G fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20
    style H fill:#f1f8f2,stroke:#388e3c,color:#1b5e20
    style I fill:#c8e6c9,stroke:#2e7d32,color:#1b5e20
    style J fill:#2e7d32,stroke:#1b5e20,color:#ffffff

The architecture will use a shared workflow state to facilitate communication between agents. Conditional routing will allow the supervisor to determine which analytical modules need to be executed based on the user's request.

6. Technology Stack

Technology| Application
Python| Core application development
LangGraph| Agent orchestration and workflow management
LangChain| LLM integration and tool development
OpenAI API| Language model integration
Pandas| Data manipulation and analysis
NumPy| Numerical computation
Plotly| Interactive data visualisation
FastAPI| Backend API development
Streamlit| Interactive frontend

7. Expected Workflow

1. Data Input: User uploads a CSV or Excel dataset.
2. Query Processing: The supervisor interprets the analytical request.
3. Task Allocation: Relevant agents are selected.
4. Data Processing: Agents perform cleaning and preprocessing.
5. Analysis: EDA and statistical analysis are conducted.
6. Visualisation: Appropriate graphical representations are generated.
7. Report Generation: Findings are consolidated into a structured report.
8. Output Delivery: Results are presented through the application interface.

8. Project Structure

AI-Data-Analyst-Agent/
│
├── agents/
│   ├── supervisor.py
│   ├── data_cleaning_agent.py
│   ├── eda_agent.py
│   ├── statistical_agent.py
│   ├── visualization_agent.py
│   └── report_agent.py
│
├── workflows/
│   └── graph.py
│
├── backend/
│   └── main.py
│
├── frontend/
│   └── app.py
│
├── utils/
│   ├── data_loader.py
│   └── helpers.py
│
├── data/
├── reports/
├── tests/
│
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md

9. Installation and Configuration

Prerequisites

- Python 3.10+
- Git
- OpenAI API key
- pip package manager

Step 1: Clone the repository

git clone https://github.com/YOUR_USERNAME/AI-Data-Analyst-Agent.git

cd AI-Data-Analyst-Agent

Step 2: Create a virtual environment

python -m venv venv

Activate the environment:

Windows

venv\Scripts\activate

Linux / macOS

source venv/bin/activate

Step 3: Install dependencies

pip install -r requirements.txt

Step 4: Configure environment variables

Create a ".env" file in the project root directory.

OPENAI_API_KEY=your_api_key_here

Ensure that environment files containing credentials are excluded from version control.

Step 5: Run the application

streamlit run frontend/app.py

10. Future Scope

The system is designed to support further extensions, including:

- Integration with SQL and relational databases.
- Retrieval-Augmented Generation (RAG) for analytical knowledge retrieval.
- Advanced multi-agent collaboration.
- Automated machine learning model selection and training.
- Predictive analytics and time-series forecasting.
- Human-in-the-loop validation.
- Model evaluation and agent performance monitoring.
- PDF and Excel report exports.
- Cloud-based deployment and scalability.

11. Project Status

Status: Planning and Development

The project will be implemented incrementally, beginning with individual analytical modules, followed by agent orchestration, integration and application deployment.

12. Author

Maya H. Kamat

MSc Data Science

Interests: Artificial Intelligence | Machine Learning | Generative AI | Data Science | Agentic AI

---

<p align="center">
  <strong>AI Data Analyst Agent</strong>
  <br/>
  Intelligent Automation for Data-Driven Decision Making
  <br/><br/>
  <img src="https://img.shields.io/badge/Built%20with-Python%20%26%20AI-2E7D32?style=flat-square" />
</p>
