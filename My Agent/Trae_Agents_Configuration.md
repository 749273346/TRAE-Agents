# Trae 智能体配置清单 (Trae Agent Configurations)

本文档定义了 Trae 智能软件开发系统的“1+6”核心智能体配置。

---

## 0. 项目负责人 Agent (Project-Lead-Agent)

*   **名称 (Name)**: `Project-Lead-Agent`
*   **可被其他智能体调用**: 否 (False) - 这是顶层Agent
*   **工具 (Tools)**:
    *   **MCP**: `File System` (用于检查各阶段产物), `Agent Invocation` (用于调用其他Agent)
    *   **Built-in**: `Read`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\Project-Lead-Agent.md`

---

## 1. 产品经理 Agent (PM-Agent)

*   **名称 (Name)**: `PM-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`, `GitHub` (可选)
    *   **Built-in**: `Read`, `Write`, `SearchReplace`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\PM-Agent.md`

---

## 2. 架构师 Agent (Arch-Agent)

*   **名称 (Name)**: `Arch-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`
    *   **Built-in**: `Read`, `Write`, `SearchReplace`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\Arch-Agent.md`

---

## 3. 开发工程师 Agent (Dev-Agent)

*   **名称 (Name)**: `Dev-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`, `GitHub`, `Chrome DevTools` (可选)
    *   **Built-in**: `Read`, `Write`, `SearchReplace`, `RunCommand`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\Dev-Agent.md`

---

## 4. 测试工程师 Agent (QA-Agent)

*   **名称 (Name)**: `QA-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`
    *   **Built-in**: `Read`, `Write`, `SearchReplace`, `RunCommand`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\QA-Agent.md`

---

## 5. 运维工程师 Agent (Ops-Agent)

*   **名称 (Name)**: `Ops-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`, `GitHub`
    *   **Built-in**: `Read`, `Write`, `SearchReplace`, `RunCommand`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\Ops-Agent.md`

---

## 6. 编程导师 Agent (Mentor-Agent)

*   **名称 (Name)**: `Mentor-Agent`
*   **可被其他智能体调用**: 开启 (True)
*   **工具 (Tools)**:
    *   **MCP**: `File System`
    *   **Built-in**: `SearchCodebase`, `Read`, `Terminal`
*   **提示词 (Prompt)**:
    *   **路径**: `e:\My Agent\My Agent\Mentor-Agent.md`
