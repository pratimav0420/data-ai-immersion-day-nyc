# Agents

This folder contains examples demonstrating how to create and use agents with Azure AI using the Microsoft Agent Framework.

## 🧠 What is the Agent Framework?

The **Microsoft Agent Framework** is an open-source SDK for building AI agents and multi-agent workflows. It combines ideas from Semantic Kernel and AutoGen into a unified foundation.

## 📓 Available Notebooks

All notebooks are in the `azure-ai-agents/` folder:

| # | Notebook | Description |
|---|----------|-------------|
| 1 | [`1-agent-and-run-level-middleware.ipynb`](azure-ai-agents/1-agent-and-run-level-middleware.ipynb) | Agent-level vs run-level middleware patterns |
| 2 | [`2-magentic-compliance-review-with-human-input.ipynb`](azure-ai-agents/2-magentic-compliance-review-with-human-input.ipynb) | Magentic multi-agent with human approval for compliance review |
| 3 | [`3-magentic-investment-research.ipynb`](azure-ai-agents/3-magentic-investment-research.ipynb) | Magentic multi-agent orchestration for investment research |

## Prerequisites

1. **Azure CLI Authentication**:
   ```bash
   az login
   ```

2. **Environment Variables** (in root `.env` file):
   ```
   AI_FOUNDRY_PROJECT_ENDPOINT=your-project-endpoint
   AZURE_AI_MODEL_DEPLOYMENT_NAME=gpt-4o
   ```

3. **For Bing Grounding** (optional):
   ```
   BING_CONNECTION_ID=/subscriptions/.../connections/bing-connection
   ```

## Learning Path

| Level | Notebooks |
|-------|-----------|
| **Beginner** | 1 (Middleware Patterns) |
| **Intermediate** | 2 (Magentic + Human-in-the-loop) |
| **Advanced** | 3 (Multi-Agent Research) |

## Related Resources

- [Agent Framework Documentation](https://learn.microsoft.com/en-us/agent-framework/overview/agent-framework-overview)
- [Agent Framework GitHub](https://github.com/microsoft/agent-framework)

