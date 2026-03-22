# AI Coding Agents

> AI coding agents are tools powered by large language models that assist developers by understanding, generating, editing, and autonomously executing code. They range from inline autocomplete assistants to fully autonomous agents that can plan, write, test, and ship software independently.

## Diagram

```mermaid
flowchart TB
  classDef concept fill:#4A90A4,stroke:#2C5F6E,stroke-width:2px,color:#fff
  classDef process fill:#7B68A6,stroke:#4A3D6E,stroke-width:2px,color:#fff
  classDef example fill:#5DAE8B,stroke:#3D7A5E,stroke-width:2px,color:#fff
  classDef analogy fill:#D4A574,stroke:#A67B4A,stroke-width:2px,color:#fff
  coding-agents("AI Coding Agents")
  inline-assistants("Inline Assistants")
  agentic-cli("Agentic CLI / Terminal Agents")
  ide-agents("AI-Native IDEs")
  autonomous-agents("Autonomous Agents")
  github-copilot(["GitHub Copilot"])
  cursor(["Cursor"])
  claude-code(["Claude Code"])
  codex(["OpenAI Codex CLI"])
  aws-kiro(["AWS Kiro"])
  devin(["Devin (Cognition)"])
  autonomy-spectrum("Autonomy Spectrum")
  context-window("Context & Codebase Awareness")
  tool-use["Tool Use"]
  class coding-agents,inline-assistants,agentic-cli,ide-agents,autonomous-agents,autonomy-spectrum,context-window concept
  class tool-use process
  class github-copilot,cursor,claude-code,codex,aws-kiro,devin example
  coding-agents -->|includes| inline-assistants
  coding-agents -->|includes| agentic-cli
  coding-agents -->|includes| ide-agents
  coding-agents -->|includes| autonomous-agents
  inline-assistants -->|e.g.| github-copilot
  ide-agents -->|e.g.| cursor
  agentic-cli -->|e.g.| claude-code
  agentic-cli -->|e.g.| codex
  ide-agents -->|e.g.| aws-kiro
  autonomous-agents -->|e.g.| devin
  inline-assistants ---|low autonomy end| autonomy-spectrum
  autonomous-agents ---|high autonomy end| autonomy-spectrum
  autonomy-spectrum -.->|depends on| context-window
  autonomy-spectrum -.->|enabled by| tool-use
  tool-use ---|exemplified by| claude-code
  tool-use ---|exemplified by| devin

  subgraph Legend
    L1("Concept"):::concept
    L2["Process"]:::process
    L3(["Example"]):::example
    L4{{"Analogy"}}:::analogy
  end
```

## Concepts

- **AI Coding Agents** [Concept]
  _LLM-powered tools that understand and generate code, ranging from autocomplete to fully autonomous software engineers_
  - **Inline Assistants** [Concept]
    _Embedded in the editor, suggest code as you type — low autonomy, high speed_
    - **GitHub Copilot** [Example]
      _Microsoft/OpenAI — the original AI coding assistant. IDE plugin offering inline suggestions, chat, and PR summaries. Powered by GPT-4o and Claude._
  - **Agentic CLI / Terminal Agents** [Concept]
    _Run from the terminal, can read files, run commands, and make multi-step changes autonomously_
    - **Claude Code** [Example]
      _Anthropic's terminal-based agentic coding tool. Reads codebases, edits files, runs tests, uses bash — all from the CLI. Excels at large, complex refactors._
    - **OpenAI Codex CLI** [Example]
      _OpenAI's open-source terminal agent. Runs locally, sandboxed, and autonomously edits code and runs shell commands. Powered by o4-mini / o3._
  - **AI-Native IDEs** [Concept]
    _Full development environments built around AI — context-aware, multi-file editing with chat_
    - **Cursor** [Example]
      _VS Code fork with deep AI integration — multi-file context, inline edits, agent mode, and chat. Uses GPT-4, Claude, and custom models._
    - **AWS Kiro** [Example]
      _Amazon's AI-native IDE. Spec-driven development — write a spec, Kiro generates tasks, implements code, and wires up AWS services. Deep AWS integration._
  - **Autonomous Agents** [Concept]
    _Fully autonomous agents that can take a task, plan, implement, test, and deliver — minimal human input_
    - **Devin (Cognition)** [Example]
      _The first fully autonomous AI software engineer. Given a task, Devin plans, codes, debugs, and deploys — operating its own browser and terminal._
  - **Autonomy Spectrum** [Concept]
    _Agents range from suggestion (human drives) → collaboration (pair programming) → delegation (human reviews) → autonomy (human approves outcome)_
    - **Context & Codebase Awareness** [Concept]
      _How much of the codebase an agent can see and reason about at once — key differentiator between tools_
    - **Tool Use** [Process]
      _Ability to run shell commands, call APIs, browse the web, read/write files — expands what agents can accomplish_

## Relationships

- **AI Coding Agents** → *includes* → **Inline Assistants**
- **AI Coding Agents** → *includes* → **Agentic CLI / Terminal Agents**
- **AI Coding Agents** → *includes* → **AI-Native IDEs**
- **AI Coding Agents** → *includes* → **Autonomous Agents**
- **Inline Assistants** → *e.g.* → **GitHub Copilot**
- **AI-Native IDEs** → *e.g.* → **Cursor**
- **Agentic CLI / Terminal Agents** → *e.g.* → **Claude Code**
- **Agentic CLI / Terminal Agents** → *e.g.* → **OpenAI Codex CLI**
- **AI-Native IDEs** → *e.g.* → **AWS Kiro**
- **Autonomous Agents** → *e.g.* → **Devin (Cognition)**
- **Inline Assistants** → *low autonomy end* → **Autonomy Spectrum**
- **Autonomous Agents** → *high autonomy end* → **Autonomy Spectrum**
- **Autonomy Spectrum** → *depends on* → **Context & Codebase Awareness**
- **Autonomy Spectrum** → *enabled by* → **Tool Use**
- **Tool Use** → *exemplified by* → **Claude Code**
- **Tool Use** → *exemplified by* → **Devin (Cognition)**

## Real-World Analogies

### Autonomy Spectrum ↔ Driving assistance features — from lane-keep assist to full self-driving

GitHub Copilot is like lane-keep assist: it nudges you but you're driving. Cursor is adaptive cruise control — it handles stretches but you supervise. Claude Code / Codex are like Tesla Autopilot — you set the destination and monitor. Devin is the robotaxi — you just say where to go.

### Context & Codebase Awareness ↔ A new hire reading the codebase vs a senior engineer who wrote it

A tool with limited context (Copilot autocomplete) is like a new hire writing one function — they know the immediate file. Cursor with project indexing is like a developer who has read the whole repo. Claude Code with full file access is the senior engineer who has been on the project for years — they know every dependency and consequence.

### Spec-driven Development (AWS Kiro) ↔ An architect handing blueprints to a construction crew

Kiro asks you to write a spec first (the blueprint), then automatically breaks it into tasks and builds the implementation. Like a construction crew that can't start without approved plans — the upfront spec prevents expensive mid-build surprises.

---
*Generated on 2026-03-22*