# AI 编程推荐 MCP 服务器 (Recommended MCP Servers for AI Programming)

本文档列出了 GitHub 上有用的模型上下文协议 (MCP) 服务器，它们可以增强 AI 的编程能力。

## 🌟 官方与合集 (Official & Collections)

*   **[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)**
    *   **描述**：这是官方仓库，包含了各种 MCP 服务器的参考实现，涵盖了文件系统 (filesystem)、Git、内存 (memory) 等多个方面。
    *   **推荐理由**：提供最可靠、最标准的实现，是学习和使用 MCP 的基础。

*   **[wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers)**
    *   **描述**：一个精心策划的 MCP 服务器列表（Awesome 列表）。
    *   **推荐理由**：非常适合发现新的、由社区贡献的服务器，资源丰富。

## 🛠️ Git 与版本控制 (Git & Version Control)

*   **[cyanheads/git-mcp-server](https://github.com/cyanheads/git-mcp-server)**
    *   **描述**：允许大语言模型 (LLM) 与本地 Git 仓库进行交互。支持 clone（克隆）、commit（提交）、branch（分支）、diff（差异比较）、log（日志）、status（状态）、push（推送）、pull（拉取）、merge（合并）等操作。
    *   **推荐理由**：功能全面的本地 Git 管理工具，让 AI 能直接操作版本控制。

*   **[github/github-mcp-server](https://github.com/github/github-mcp-server)**
    *   **描述**：GitHub 官方推出的 MCP 服务器。
    *   **推荐理由**：与 GitHub API（如 Issues、Pull Requests 等）进行交互的最佳选择，适合处理远程仓库事务。

*   **[cyanheads/github-mcp-server](https://github.com/cyanheads/github-mcp-server)**
    *   **描述**：GitHub API 集成的另一个强力选项，用于管理仓库、issues 和 pull requests。
    *   **推荐理由**：提供了除官方版之外的另一种选择，功能同样强大。

## 📂 文件系统与编辑 (Filesystem & Editing)

*   **[cyanheads/filesystem-mcp-server](https://github.com/cyanheads/filesystem-mcp-server)**
    *   **描述**：跨平台的文件处理工具，具备高级搜索/替换和目录树遍历功能。
    *   **推荐理由**：适用于复杂的文件操作和代码库探索，能帮助 AI 更好地理解项目结构。

*   **[mark3labs/mcp-filesystem-server](https://github.com/mark3labs/mcp-filesystem-server)**
    *   **描述**：文件系统操作的 Go 语言实现版本。
    *   **推荐理由**：以 Go 语言编写，运行快速且高效。

## 💻 代码执行与分析 (Code Execution & Analysis)

*   **[twn39/jupyter-code-executor-mcp-server](https://github.com/twn39/jupyter-code-executor-mcp-server)**
    *   **描述**：通过 Jupyter 内核执行多种编程语言的代码。
    *   **推荐理由**：允许 AI 交互式地运行和测试代码片段，就像在 Jupyter Notebook 中一样，增强了 AI 的验证能力。

*   **[the-ride-never-ends/claudes_toolbox](https://github.com/the-ride-never-ends/claudes_toolbox)**
    *   **描述**：将命令行 (CLI) 程序和函数暴露给 AI 助手。
    *   **推荐理由**：弥合了 AI 与系统 CLI 工具之间的鸿沟，让 AI 能调用更多系统级工具。

## 🧠 知识与帮助 (Knowledge & Help)

*   **[gscalzo/stackoverflow-mcp](https://github.com/gscalzo/stackoverflow-mcp)**
    *   **描述**：查询 Stack Overflow 以帮助查找编程解决方案。
    *   **推荐理由**：让 AI 能直接访问开发者社区的庞大知识库，辅助解决疑难杂症。

## 🚀 部署 (Deployment)

*   **[awslabs/run-model-context-protocol-servers-with-aws-lambda](https://github.com/awslabs/run-model-context-protocol-servers-with-aws-lambda)**
    *   **描述**：在 AWS Lambda 上运行 MCP 服务器。
    *   **推荐理由**：适用于在云端（Serverless 环境）部署你的代理或工具，扩展性强。
