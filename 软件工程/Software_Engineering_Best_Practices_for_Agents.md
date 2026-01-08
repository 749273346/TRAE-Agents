# 面向 Agent 的软件工程最佳实践 (Software Engineering Best Practices for Agents)

本文档基于 GitHub 上最受欢迎的软件工程仓库（如 `system-design-primer`, `awesome-software-architecture` 等）的精华内容进行总结，旨在为 AI 编程 Agent 建立一套坚实的理论基础。

作为一名 AI 工程师（Agent），在生成代码或设计系统时，应始终遵循以下原则。

## 1. 系统设计原则 (System Design Principles)
*参考源: [system-design-primer](https://github.com/donnemartin/system-design-primer)*

### 1.1 核心目标
*   **可靠性 (Reliability)**: 系统在困境（硬件故障、软件错误、人为错误）中仍能正常工作。
    *   *Agent 实践*: 编写代码时必须包含错误处理（Try-Catch）、重试机制和日志记录。
*   **可扩展性 (Scalability)**: 系统能够通过增加资源（垂直或水平扩展）来应对负载增长。
    *   *Agent 实践*: 设计无状态 (Stateless) 的服务，使用缓存 (Caching) 减轻数据库压力。
*   **可维护性 (Maintainability)**: 系统易于理解、修改和进化。
    *   *Agent 实践*: 遵循代码规范，编写清晰的注释，避免过度设计。

### 1.2 关键概念
*   **CAP 定理**: 在分布式系统中，一致性 (Consistency)、可用性 (Availability)、分区容错性 (Partition Tolerance) 三者不可兼得。
    *   *决策*: 明确当前系统是 CP（强一致性）还是 AP（高可用性）。
*   **缓存策略**: Read-Through, Write-Through, Write-Back。
    *   *决策*: 优先使用 Redis/Memcached 加速热点数据读取。

## 2. 软件架构模式 (Software Architecture Patterns)
*参考源: [awesome-software-architecture](https://github.com/mehdihadeli/awesome-software-architecture)*

### 2.1 整洁架构 (Clean Architecture) / 洋葱架构
*   **核心思想**: 依赖倒置。核心业务逻辑不应依赖于外部框架、UI 或数据库。
*   **分层**:
    1.  **Entities (领域实体)**: 核心业务规则。
    2.  **Use Cases (用例)**: 应用特定业务规则。
    3.  **Interface Adapters (接口适配器)**: 控制器、网关、Presenters。
    4.  **Frameworks & Drivers (框架与驱动)**: Web 框架、数据库、设备。
*   *Agent 实践*: 生成代码时，严格分离 `Domain`, `Service`, `Infrastructure` 层。

### 2.2 领域驱动设计 (DDD)
*   **核心**: 将复杂的业务逻辑与技术实现分离。
*   **术语**: Aggregate Root (聚合根), Entity (实体), Value Object (值对象), Repository (仓储).
*   *Agent 实践*: 在理解需求时，先识别业务领域的名词，将其建模为实体或值对象。

### 2.3 微服务 (Microservices)
*   **核心**: 将单体应用拆分为一组小型服务，每个服务运行在独立的进程中。
*   *Agent 实践*: 定义清晰的 API 接口 (REST/gRPC)，服务间解耦。

## 3. 设计模式 (Design Patterns)
*参考源: [awesome-design-patterns](https://github.com/DovAmir/awesome-design-patterns)*

Agent 应熟练运用 GoF 23 种设计模式，特别是：

*   **单例模式 (Singleton)**: 用于配置管理、数据库连接池。
*   **工厂模式 (Factory)**: 用于创建复杂对象，解耦创建逻辑。
*   **策略模式 (Strategy)**: 用于算法替换（如多种支付方式）。
*   **观察者模式 (Observer)**: 用于事件驱动架构。
*   **装饰器模式 (Decorator)**: 用于动态扩展功能（如日志、权限校验）。

## 4. 代码质量与整洁代码 (Clean Code)
*参考源: Clean Code (Robert C. Martin)*

### 4.1 命名规范
*   **名副其实**: 变量名应清晰表达其意图。`int d` (Bad) -> `int elapsedTimeInDays` (Good)。
*   **避免误导**: 别用 `hp`, `aix`, `sco` 等专用术语做变量名。

### 4.2 函数设计
*   **短小**: 函数应尽量短小，只做一件事 (Single Responsibility)。
*   **参数少**: 最理想的参数数量是 0，其次是 1，再次是 2。尽量避免 3 个以上参数。

### 4.3 注释
*   **代码即文档**: 最好的注释是写出无需注释的代码。
*   **必要注释**: 解释 "Why" 而不是 "How"。

## 5. Agent 开发检查清单 (Checklist)

在提交代码前，Agent 应自检：
- [ ] **SOLID 原则**:
    - SRP (单一职责)
    - OCP (开闭原则)
    - LSP (里氏替换)
    - ISP (接口隔离)
    - DIP (依赖倒置)
- [ ] **DRY (Don't Repeat Yourself)**: 拒绝重复代码。
- [ ] **KISS (Keep It Simple, Stupid)**: 保持简单。
- [ ] **YAGNI (You Ain't Gonna Need It)**: 不要过度设计。

---
**总结**: 优秀的 AI 编程 Agent 不仅仅是代码生成器，更是**架构师**和**工匠**。请始终将上述原则融入到每一次代码生成中。
