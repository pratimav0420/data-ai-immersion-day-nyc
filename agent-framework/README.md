# 🤖 Microsoft Agent Framework Samples

Practical notebooks and reference material for building Microsoft Agent Framework solutions across agents, workflows, memory, middleware, and observability scenarios — all with **real-world business** use cases.

## Table of Contents

1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Environment Setup](#environment-setup)
4. [Running the Notebooks](#running-the-notebooks)
5. [Repository Guide](#repository-guide)
6. [Suggested Learning Path](#suggested-learning-path)
7. [Troubleshooting](#troubleshooting)
8. [Additional Resources](#additional-resources)

## Overview

The Microsoft Agent Framework is the next generation of tooling from the Semantic Kernel and AutoGen teams. It provides a unified programming model for building intelligent agents, multi-agent workflows, and connected tools in both Python and .NET. These samples showcase core scenarios ranging from single-agent chat to advanced orchestration with state management, custom memory, and telemetry.

All notebooks feature **business use cases** including application processing, compliance review, execution monitoring, customer service, and research workflows.

> The framework is currently in public preview. Expect APIs and package names to evolve.

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Python** | 3.10 or later |
| **Azure Subscription** | Access to Microsoft Foundry |
| **Azure CLI** | 2.60+ with active `az login` session |
| **Optional** | Redis (distributed threads), Application Insights (telemetry) |

## Environment Setup

1. **Install packages** — Install the preview roll-up package or specific integrations as needed.

2. **Configure environment variables** — Copy `.env.example` to `.env` and update with your Azure resources:
   - `AI_FOUNDRY_PROJECT_ENDPOINT` — Your Microsoft Foundry project endpoint
   - `AZURE_OPENAI_ENDPOINT` — Your Azure OpenAI endpoint
   - `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` — Model deployment name (e.g., gpt-4o)
   - Additional variables as needed: `BING_CONNECTION_ID`, `AZURE_AI_SEARCH_ENDPOINT`, Redis connection strings

3. **Verify authentication** — Run `az account show` to confirm the CLI is signed in and targeting the correct subscription.

## Running the Notebooks

1. Activate your Python virtual environment.
2. Open the notebook you want to explore and execute the cells in order.
3. Most notebooks include setup cells that validate credentials before the scenarios run.

---

## Repository Guide

### 📁 `agents/`

Agent patterns and multi-agent workflows for Azure AI. See [agents/README.md](agents/README.md) for details.

| # | Notebook | Use Case | Key Concepts |
|---|----------|----------|--------------|
| 1 | `1-agent-and-run-level-middleware.ipynb` | **Middleware Patterns** | Agent-level vs run-level middleware |
| 2 | `2-magentic-compliance-review-with-human-input.ipynb` | **Plan Compliance Review** | Magentic multi-agent with human approval |
| 3 | `3-magentic-investment-research.ipynb` | **Multi-Agent Research** | Magentic multi-agent orchestration |

**Learning Path**: 1 (Middleware) → 2 (Magentic + Human-in-the-loop) → 3 (Multi-Agent)

---

## Suggested Learning Path

| Step | Focus | Notebooks |
|------|-------|-----------|
| 1 | **Middleware Patterns** | `agents/azure-ai-agents/1-agent-and-run-level-middleware.ipynb` |
| 2 | **Human-in-the-Loop** | `agents/azure-ai-agents/2-magentic-compliance-review-with-human-input.ipynb` |
| 3 | **Multi-Agent Orchestration** | `agents/azure-ai-agents/3-magentic-investment-research.ipynb` |

## Troubleshooting

| Issue | Solution |
|-------|----------|
| **Authentication failures** | Re-run `az login` and confirm Azure AI permissions |
| **Missing environment variables** | Verify `.env` mirrors the keys called out in notebook setup cells |
| **Package import errors** | Ensure `agent-framework` packages installed in the same interpreter as Jupyter |
| **Redis connectivity** | Update connection string and confirm service is reachable |
| **Application Insights delay** | Telemetry can take a few minutes; use Live Metrics Stream for real-time debugging |

## Additional Resources

- [Agent Framework Documentation](https://learn.microsoft.com/en-us/agent-framework/overview/agent-framework-overview)
- [Agent Framework GitHub](https://github.com/microsoft/agent-framework)
- [Azure AI Services](https://learn.microsoft.com/azure/ai-services/)
- [Azure Monitor OpenTelemetry](https://learn.microsoft.com/en-us/azure/azure-monitor/app/opentelemetry-overview)

> Keep an eye on release notes in the official documentation for API or package updates while the framework remains in preview.
