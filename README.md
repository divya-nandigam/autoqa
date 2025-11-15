AutoQA — Autonomous Multi-Agent Software Test Engineer

AutoQA is an end-to-end multi-agent system that automates the complete software testing lifecycle. It reads user stories, extracts requirements, generates test cases, creates automation scripts, executes them (mocked or real), identifies failures, and files bug reports.

This repository was built for the Agents Intensive – Capstone Project (Google × Kaggle) and showcases advanced agent concepts:

Sequential & Parallel Agents

Loop Agents

Custom Tools (MCP Bug Tracker, Code Execution)

Sessions & Memory (Memory Bank)

Context Compaction

Observability (structured logs, stored JSON report)

A2A (Agent-to-Agent pipelines)

Agent Evaluations

📌 Features

Automatic Requirements Extraction

AI-powered Test Case & Scenario Generation

Automated Python Script Generation

Mocked Test Execution

Bug Identification & Reporting

Structured JSON Output for full traceability

Memory-enabled agents

Clean modular pipeline design

📁 Repository Contents
autoqa/
├── agents/
│   ├── requirements_agent.py
│   ├── test_designer_agent.py
│   ├── automation_builder_agent.py
│   ├── test_executor_agent.py
│   └── bug_analyst_agent.py
│
├── tools/
│   ├── bugtracker_mcp.py
│   └── code_execution.py
│
├── memory/
│   └── memory_bank.json
│
├── examples/
│   ├── sample_user_story.txt
│   ├── expected_output_report.json
│   └── automation_scripts/
│
├── mock_bugtracker_server.py
├── main.py
└── README.md
 1.Run the AutoQA pipeline
python main.py

The system will:

Parse the user story

Extract requirements

Generate test cases

Produce automation scripts

Execute tests (mocked)

File bug reports

Save full JSON output

2. View the final report
examples/expected_output_report.json

Contains:

Requirements summary

Test case suite

Test scripts

Execution results

Bug reports

🛠 Installation
Clone the repository:
git clone https://github.com/<your-username>/autoqa.git
cd autoqa

Install dependencies:
pip install -r requirements.txt

Add your Gemini API key:

Mac/Linux:

export GEMINI_API_KEY="your-key"


Windows (PowerShell):

setx GEMINI_API_KEY "your-key"

🧠 Architecture Overview

AutoQA uses a pipeline of five agents:

Requirements Agent – Extracts acceptance criteria

Test Designer Agent – Generates test plans and test cases

Automation Builder Agent – Creates Python test scripts

Test Executor Agent – Executes or simulates test runs

Bug Analyst Agent – Detects failures and generates bug reports

Pipeline Flow:

User Story
   ↓
Requirements Agent
   ↓
Test Designer Agent
   ↓
Automation Builder Agent
   ↓
Test Executor Agent
   ↓
Bug Analyst Agent
   ↓
Final JSON Report

🖼 Architecture Diagram

(Insert your generated architecture diagram PNG here in GitHub)

🔧 Technologies Used

Google Gemini Agents

Python

MCP Tools

A2A Communication

Memory Bank

JSON-based Observability

Mock Execution Framework

🔮 Future Enhancements

If expanded beyond the capstone project:

Real browser automation (Playwright/Selenium)

Integration with JIRA / GitHub Issues

Test coverage dashboards

Parallel agent execution

Visual regression testing

CI/CD integration

Expanded long-term memory

📜 License

Open-source — free to use, fork, and extend.
