# File & Repository-Driven AI Agents

> ⚠️ **ALPHA VERSION - UNDER CONSTRUCTION**  
> This repository is under active development. Structure and content may change frequently.

## Overview
This repository provides **tutorials, templates, and best practices** for building AI agents that are driven by files and repository structures. Learn how to create agents that can be configured, extended, and managed through agent files.

## 🎯 Repository Purpose

This repository serves three main goals:

1. **Tutorials**: Learn how to create "file-driven" and "repo-driven" AI agents
2. **Definitions**: Understand the basic files needed for these agents and how to structure them
3. **Base Template**: Use `agents.md` as a foundation to start your own agent repository

## 🏗️ What are File-Driven Agents?

File-driven agents are AI agents whose behavior, capabilities, and configuration are defined through a structured file system rather than hardcoded logic. This approach offers:

- **Modularity**: Skills, rules, and configs as separate files
- **Transparency**: Agent behavior defined in readable markdown/YAML files
- **Extensibility**: Easy to add new capabilities without code changes
- **Version Control**: Full agent configuration tracked in Git

### Why File-Driven Agents?

As people, we want **visibility and control** over our AI agents. We don't want to teach them from scratch every time or rely on opaque systems. File-driven agents allow us to:

- **See exactly what our agent knows** - all behavior is documented in files
- **Reload agents across different models** - the same agent definition can work with different AI models
- **Compare agent behavior** - test how the same agent behaves in different environments
- **Maintain consistency** - agents (should) behave the same way regardless of where they run
- **Evolve agents over time** - version control tracks every change to agent behavior

## 📁 Repository Structure

The `agents.md` file contains detailed information about how agents are structured and managed. Here's a simple example:

```
/project-root/
├── agents.md         - Defines agent logic (COPY THIS!)
├── /agents/          - Your agent definitions
└── /skills/          - Reusable agent skills
```

See a more complete example in the [agents](agents.md) file. 

## 🚀 Quick Start

Open the GitHub Copilot agent (or any other AI agent) and write:

```
Load agents.md, and give me options
```

## 📚 Key Concepts

### agents.md
The **[agents.md](./agents.md)** file is the foundation of this repository. It defines how agents work, how they're structured, and best practices for creating them.

Read through it to understand the complete framework.

### Agent Lifecycle
1. **Agent Loading** (once): Load agent.md, configurations, and determine scope
2. **Agent Querying** (per conversation): Validate rules, lookup skills, execute

### File Organization Principles
- **Agents**: Have their own directory with multiple files
- **Everything Else**: Single file per item (skills, rules, configs)

## 🤝 Contributing

This repository is under active development. Contributions, suggestions, and feedback are welcome!

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.