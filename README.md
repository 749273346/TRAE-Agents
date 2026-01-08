# My Agent - AI Agent System

Welcome to **My TRAE-Agent**, a comprehensive knowledge base and prompt library for building, managing, and collaborating with AI Agents.

This repository defines a structured ecosystem of AI Agents designed to handle various complex tasks, from software development to teaching and even "manufacturing" other agents.

## 📂 Project Structure

The repository is organized into several functional domains:

### 1. 🏭 Factory Agent (The Agent Builder)
> *"Agents that build other Agents."*

This module contains the "Meta-Agents" responsible for analyzing user needs and generating customized Agent prompts.
*   **Mother-Lead-Agent (Factory Lead)**: The factory manager who coordinates the entire agent creation process.
*   **Agent-Architect-Agent**: Designs the topology and roles of a new agent team.
*   **Prompt-Engineer-Agent**: Writes the actual `.md` prompt files.
*   **Evaluator-Agent**: Quality assurance for generated prompts.

### 2. 💻 Object Agent (The Software Team)
> *"Agents that build software."*

A complete virtual software development company.
*   **Project-Lead-Agent**: The team lead and your main point of contact.
*   **PM-Agent**: Product Manager for PRDs.
*   **Arch-Agent**: System Architect.
*   **Design-Agent**: UI/UX Designer.
*   **Dev-Agent**: Senior Developer.
*   **QA-Agent**: Quality Assurance.
*   **Security-Agent**: Security Specialist.
*   **Ops-Agent**: DevOps Engineer.
*   **Auditor-Agent**: Third-party auditor for final acceptance.

### 3. 🎓 Tutor Agent (The Educators)
*   **Mentor-Agent**: Personalized learning mentor.
*   **TA-Agent**: Teaching Assistant.

### 4. 🐙 Github Agent
*   **GitHub-Ops-Agent**: Automates GitHub operations (repo creation, file pushing, etc.).

### 5. 📚 Documentation
*   **Operation Manuals**: Detailed SOPs for each agent group.
*   **Software Engineering**: Best practices for AI-assisted development.
*   **Traditional Development Process**: Reference material for standard software lifecycles.

## 🚀 How to Use

This project follows a **"Prompt as Code"** philosophy. Each `.md` file represents the "source code" or "persona" of an AI Agent.

### To Start a Software Project:
1.  Open the Chat in your IDE (e.g., Trae).
2.  Load the **Project-Lead-Agent** prompt.
3.  Say: *"I want to build a [Project Name]..."*
4.  Follow the interactive wizard steps guided by the Project Lead.

### To Create a Custom Agent Team:
1.  Load the **Mother-Lead-Agent** prompt.
2.  Say: *"I need a team of agents for [Task Name]..."*
3.  The factory team will design and generate the prompts for you.

## 📖 Documentation
*   [Factory Agent Operation Manual](My%20Agent/Factory%20Agent/Operation_Manual.md)
*   [Object Agent Operation Manual](My%20Agent/Object%20Agent/Operation_Manual.md)

## 📄 License
[MIT License](LICENSE)
