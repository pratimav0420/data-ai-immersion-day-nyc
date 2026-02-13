# Agentic AI Immersion Workshop

[![Microsoft Foundry](https://img.shields.io/badge/Microsoft-Foundry-blue?style=for-the-badge&logo=microsoft)](https://ai.azure.com)
[![Python](https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-orange?style=for-the-badge&logo=jupyter)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Comprehensive Microsoft Foundry & Agents Development Workshop**

*Master AI agents, workflows, observability, and enterprise patterns through hands-on experimentation with real-world use cases.*

---

## Table of Contents

- [Mission Statement](#mission-statement)
- [Repository Structure](#repository-structure)
- [Industry Use Cases](#industry-use-cases)
- [Getting Started](#getting-started)
  - [Required Azure RBAC Roles](#step-5-required-azure-rbac-roles)
- [Learning Path](#learning-path)
- [Troubleshooting & Support](#troubleshooting--support)
- [Community & Contributions](#community--contributions)

---

## Mission Statement

This comprehensive workshop transforms you from an AI enthusiast into a Microsoft Foundry expert. Through progressive, hands-on modules, you'll master:

| Module | Topics | Technology |
|--------|--------|------------|
| **Foundation** | Setup, Authentication, Quick Start | Azure AI Foundry, Azure AI Agents v2 |
| **Core AI** | Code Execution, Enterprise Search | Azure OpenAI, Azure AI Search |
| **Agents** | Bing Grounding, Multi-Agent Workflows, Memory Patterns | Code Interpreter, Bing Grounding, Multi-Agent Workflows |
| **Foundry IQ** | Revolutionary agentic retrieval with knowledge bases | Foundry IQ, Knowledge Bases |
| **Advanced** | MCP Integration, Red Teaming, Agent Framework | Foundry MCP Server, Microsoft Agent Framework |
| **Operations** | Observability, Evaluation, Fine-Tuning | OpenTelemetry, Azure Monitor, Built-in Evaluators |
| **Deployment** | Hosted Agents with Azure Developer CLI | Azure Developer CLI (azd), Hosted Agents |
| **Enterprise** | Responsible AI | Red Team Testing, Content Safety |

> **Format**: Intensive hands-on experience  
> **Audience**: Developers, AI practitioners, and solution architects  
> **Approach**: Progressive complexity with real-world business use cases

---

## Repository Structure

```
agentic-ai-immersion-day/
│
├── azure-ai-agents/                           # Azure AI Agents SDK (8 notebooks)
│   ├── 1-basics.ipynb                         # Agent fundamentals
│   ├── 2-code-interpreter.ipynb               # Code execution
│   ├── 3-agents-aisearch.ipynb                # Enterprise search
│   ├── 4-bing-grounding.ipynb                 # Web search integration
│   ├── 5-multi-agent-solution-with-workflows.ipynb  # Multi-agent orchestration
│   ├── 6-foundry-IQ-agents.ipynb              # Foundry IQ - Agentic retrieval
│   ├── 7-agent-memory-search.ipynb            # Memory patterns
│   ├── 8-mcp-tools.ipynb                      # MCP integration
│   └── seq-diagrams/                          # Sequence diagram images
│
├── agent-framework/                           # Microsoft Agent Framework (3 notebooks)
│   ├── agents/
│   │   ├── azure-ai-agents/
│   │   │   ├── 1-agent-and-run-level-middleware.ipynb    # Middleware patterns
│   │   │   ├── 2-magentic-compliance-review-with-human-input.ipynb  # Plan review
│   │   │   ├── 3-magentic-investment-research.ipynb      # Multi-agent orchestration
│   │   │   └── resources/                     # Sample data files
│   │   └── README.md
│   └── README.md
│
├── observability-and-evaluations/              # Evaluation (3 notebooks)
│   ├── 1-telemetry.ipynb                      # Azure Monitor telemetry
│   ├── 2-agent-evaluation.ipynb               # Built-in evaluators
│   ├── 3-tool-call-accuracy-evaluation.ipynb  # Tool accuracy
│   └── README.md
│
├── .devcontainer/                              # Dev Container configuration
│   └── devcontainer.json                      # Container settings
│
├── .env.example                               # Environment template
├── requirements.in                            # Unpinned dependencies
├── requirements.txt                           # Pinned dependencies (pip-compile)
├── CONTRIBUTING.md                            # Contribution guidelines
├── LICENSE                                    # MIT License
└── README.md                                  # This file
```

---

## Industry Use Cases

This workshop features **real-world FSI (Financial Services Industry) use cases** across all notebooks, demonstrating practical AI agent applications for enterprise banking, insurance, and investment scenarios.

### Azure AI Agents SDK

| Use Case | Description | Technology | Notebook |
|----------|-------------|------------|----------|
| Financial Services Advisor | General banking, loan, and investment guidance with regulatory disclaimers | Azure AI Agents v2 | [1-basics.ipynb](azure-ai-agents/1-basics.ipynb) |
| Loan & Portfolio Calculator | Calculates loan payments, amortization schedules, analyzes financial data | Azure AI Agents v2, Code Interpreter | [2-code-interpreter.ipynb](azure-ai-agents/2-code-interpreter.ipynb) |
| Banking Products Catalog | Semantic search across banking products (loans, credit cards, accounts) | Azure AI Agents v2, Azure AI Search | [3-agents-aisearch.ipynb](azure-ai-agents/3-agents-aisearch.ipynb) |
| Financial Market Research | Real-time market trends, interest rates, and financial news | Azure AI Agents v2, Bing Grounding | [4-bing-grounding.ipynb](azure-ai-agents/4-bing-grounding.ipynb) |
| Insurance Claims Processing | Automated claims assessment, validation, and payout decisions | Azure AI Agents v2, Multi-Agent Workflows | [5-multi-agent-solution-with-workflows.ipynb](azure-ai-agents/5-multi-agent-solution-with-workflows.ipynb) |
| Multi-Source Fraud Investigation | Investigate fraud using patterns, regulations, and procedures | Azure AI Agents v2, Foundry IQ | [6-foundry-IQ-agents.ipynb](azure-ai-agents/6-foundry-IQ-agents.ipynb) |
| Personalized Banking Assistant | Remembers customer preferences for personalized guidance | Azure AI Agents v2, Memory Search | [7-agent-memory-search.ipynb](azure-ai-agents/7-agent-memory-search.ipynb) |
| Platform Operations Assistant | Model discovery, deployment management, evaluation creation | Azure AI Agents v2, Foundry MCP Server | [8-mcp-tools.ipynb](azure-ai-agents/8-mcp-tools.ipynb) |

### Agent Framework

| Use Case | Description | Technology | Notebook |
|----------|-------------|------------|----------|
| Transaction Compliance Monitoring | Monitor transactions for regulatory violations with audit logs | Agent Framework, Middleware | [1-agent-and-run-level-middleware.ipynb](agent-framework/agents/azure-ai-agents/1-agent-and-run-level-middleware.ipynb) |
| Investment Research with Compliance | Compliance oversight of research plans before execution | Agent Framework, Magentic Orchestration | [2-magentic-compliance-review-with-human-input.ipynb](agent-framework/agents/azure-ai-agents/2-magentic-compliance-review-with-human-input.ipynb) |
| Investment Research Report Generation | Multi-agent market research and quantitative analysis | Agent Framework, Magentic Multi-Agent | [3-magentic-investment-research.ipynb](agent-framework/agents/azure-ai-agents/3-magentic-investment-research.ipynb) |

### Observability & Evaluations

| Use Case | Description | Technology | Notebook |
|----------|-------------|------------|----------|
| Wealth Management Advisory Monitoring | Telemetry and tracing for investment guidance with audit | Azure AI Agents v2, OpenTelemetry | [1-telemetry.ipynb](observability-and-evaluations/1-telemetry.ipynb) |
| Loan Advisory Quality Testing | Evaluate agent responses for quality, safety, compliance | Azure AI Agents v2, Built-in Evaluators | [2-agent-evaluation.ipynb](observability-and-evaluations/2-agent-evaluation.ipynb) |
| Banking Operations Tool Validation | Validate correct tool selection for banking operations | Azure AI Agents v2, Tool Call Accuracy | [3-tool-call-accuracy-evaluation.ipynb](observability-and-evaluations/3-tool-call-accuracy-evaluation.ipynb) |

### Key Patterns Demonstrated

| Pattern | Business Application | Count |
|---------|---------------------|-------|
| **Human-in-the-Loop** | Compliance plan review and approval | 1 |
| **Multi-Agent (Magentic)** | Research analysis, compliance review | 2 |
| **Middleware** | Audit trails, compliance screening | 1 |
| **Evaluation** | Agent quality, tool accuracy | 2 |
| **Foundry IQ** | Agentic retrieval with knowledge bases | 1 |
| **Memory Search** | Personalized customer interactions | 1 |
| **MCP Integration** | Platform operations automation | 1 |

---

## Getting Started

#### Step 1: Repository Setup

```powershell
# Clone the repository
git clone https://github.com/dhangerkapil/agentic-ai-immersion-day.git
cd agentic-ai-immersion-day

# Verify Python version
python --version  # Python 3.10+ required
```

#### Step 2: Environment Setup

```powershell
# Create and activate virtual environment
python -m venv .venv
.\.venv\Scripts\activate

# Install dependencies (versions are pinned for consistency)
pip install -r requirements.txt
```

#### Step 3: Configure Environment Variables
 - Copy `.env.example` to `.env` in the root directory and update values accordingly
   - This repository expects the `.env` file to be in the root directory, if you want to store it elsewhere or name it something else, update the `load_dotenv()` calls in notebooks
   - Many of the Environment Variables needed can be found in the Overview tab of your Microsoft Foundry project or the connected resources in the Management Center tab
   - For example, AZURE_OPENAI variables-
<img src="images/env-example.png" width="75%"/>  

1. Copy `.env.example` to `.env`
2. Update with your Azure resources:

```env
# Required
AI_FOUNDRY_PROJECT_ENDPOINT=https://your-project.services.ai.azure.com
AZURE_OPENAI_API_KEY=your-api-key
AZURE_AI_MODEL_DEPLOYMENT_NAME=gpt-4o
BING_CONNECTION_ID=/subscriptions/.../connections/bing
AZURE_AI_SEARCH_ENDPOINT=https://your-search.search.windows.net
```

### Step 4: Microsoft Foundry Setup

1. **Create Microsoft Foundry Resource** — [Azure Portal](https://portal.azure.com/#create/Microsoft.CognitiveServicesAIFoundry)
2. **Deploy Models** — `gpt-4o`, `gpt-4o-mini`, `text-embedding-3-large`
3. **Connect Services** — Azure AI Search, Bing Search, Application Insights

 a. Configure an Azure Search Service**
   - Create an Azure AI Search resource in Azure
   - Connect this resource to your Microsoft Foundry project
      - Navigate to your Microsoft Foundry project → Management Center → Connected Resources → Add Connection → Select Azure AI Search
      <img src="images/foundry-connection.png" width="75%"/>

 b. Configure Grounding with Bing Search**
   - Create a new Grounding with Bing Search resource in Azure
   - Connect this resource to your Microsoft Foundry project
      - Navigate to your Microsoft Foundry project → Management Center → Connected Resources → Add Connection → Select Grounding with Bing Search


### Step 5: Required Azure RBAC Roles

Assign the following roles based on the notebooks you plan to run. Each role specifies whether it should be assigned to **your user identity** or to the **Project Managed Identity**.

#### Core Roles (Required for All Notebooks)

| Role | Assignee | Resource | Purpose |
|------|----------|----------|---------|
| **Azure AI Developer** | User | AI Foundry Project | Create and manage agents, threads, and runs |
| **Cognitive Services OpenAI User** | User | AI Foundry Project | Access OpenAI model deployments |

####  Azure AI Search Roles

| Role | Assignee | Resource | Purpose | Notebooks |
|------|----------|----------|---------|-----------|
| **Search Index Data Contributor** | User | AI Search Resource | Create indexes, upload documents | `3-agents-aisearch.ipynb`, `6-foundry-IQ-agents.ipynb` |
| **Search Index Data Reader** | User | AI Search Resource | Query search indexes | `3-agents-aisearch.ipynb`, `6-foundry-IQ-agents.ipynb` |
| **Search Service Contributor** | User | AI Search Resource | Manage search service, create knowledge bases | `6-foundry-IQ-agents.ipynb` |
| **Search Index Data Reader** | Managed Identity | AI Search Resource | **CRITICAL**: Agent runtime access to knowledge bases | `6-foundry-IQ-agents.ipynb` |

#### Role Assignment Commands

```powershell
# Get your user principal ID
$USER_PRINCIPAL_ID = (az ad signed-in-user show --query id -o tsv)

# Get resource scopes (replace with your values)
$PROJECT_SCOPE = "/subscriptions/<sub-id>/resourceGroups/<rg>/providers/Microsoft.MachineLearningServices/workspaces/<project>"
$SEARCH_SCOPE = "/subscriptions/<sub-id>/resourceGroups/<rg>/providers/Microsoft.Search/searchServices/<search>"

# ═══════════════════════════════════════════════════════════════
# USER ROLES
# ═══════════════════════════════════════════════════════════════

# Core roles (required for all notebooks)
az role assignment create --role "Azure AI Developer" --assignee $USER_PRINCIPAL_ID --scope $PROJECT_SCOPE
az role assignment create --role "Cognitive Services OpenAI User" --assignee $USER_PRINCIPAL_ID --scope $PROJECT_SCOPE

# Search roles (for AI Search notebooks)
az role assignment create --role "Search Index Data Contributor" --assignee $USER_PRINCIPAL_ID --scope $SEARCH_SCOPE
az role assignment create --role "Search Index Data Reader" --assignee $USER_PRINCIPAL_ID --scope $SEARCH_SCOPE
az role assignment create --role "Search Service Contributor" --assignee $USER_PRINCIPAL_ID --scope $SEARCH_SCOPE

# ═══════════════════════════════════════════════════════════════
# MANAGED IDENTITY ROLES (CRITICAL for Foundry IQ Agents)
# ═══════════════════════════════════════════════════════════════

# Get Project Managed Identity from Azure Portal:
# AI Foundry Project → Settings → Identity → Object (principal) ID
$PROJECT_MI_ID = "<PROJECT_MANAGED_IDENTITY_PRINCIPAL_ID>"

az role assignment create --role "Search Index Data Reader" --assignee $PROJECT_MI_ID --scope $SEARCH_SCOPE
```

> **Critical Notes:**
> - **Managed Identity Role**: The `Search Index Data Reader` on the Project Managed Identity is **required** for `6-foundry-IQ-agents.ipynb` - without it, the MCP tool cannot query the knowledge base at runtime.
> - **Role Propagation**: Role assignments can take **5-10 minutes** to propagate. If you encounter permission errors, wait and retry.  

---

## Learning Path

Follow this structured learning path to master Microsoft Foundry and AI Agents:

### Phase 1: Azure AI Agents SDK
**Location:** `azure-ai-agents/`

| # | Notebook | Description |
|---|----------|-------------|
| 1 | [Agent Basics](azure-ai-agents/1-basics.ipynb) | Fundamental agent concepts and lifecycle |
| 2 | [Code Interpreter](azure-ai-agents/2-code-interpreter.ipynb) | Python code execution capabilities |
| 3 | [Agents + AI Search](azure-ai-agents/3-agents-aisearch.ipynb) | Enterprise search integration |
| 4 | [Bing Grounding](azure-ai-agents/4-bing-grounding.ipynb) | Web search integration |
| 5 | [Multi-Agent Workflows](azure-ai-agents/5-multi-agent-solution-with-workflows.ipynb) | YAML-based multi-agent orchestration for insurance claims |
| 6 | [Foundry IQ Agents](azure-ai-agents/6-foundry-IQ-agents.ipynb) | **Revolutionary agentic retrieval** - Multi-source fraud investigation |
| 7 | [Agent Memory Search](azure-ai-agents/7-agent-memory-search.ipynb) | Persistent memory patterns for personalized banking |
| 8 | [MCP Tools](azure-ai-agents/8-mcp-tools.ipynb) | Foundry MCP Server integration |

### Phase 2: Microsoft Agent Framework
**Location:** `agent-framework/agents/azure-ai-agents/`

The **Microsoft Agent Framework** is an open-source SDK that unifies Semantic Kernel and AutoGen into the next-generation foundation for AI agent development. It offers **AI Agents** for autonomous decision-making with tool integration, and **Workflows** for orchestrating complex multi-agent processes with type safety and checkpointing.

[Official Documentation](https://learn.microsoft.com/en-us/agent-framework/overview/agent-framework-overview) • [GitHub Repository](https://github.com/microsoft/agent-framework) • [Complete Guide](agent-framework/README.md)

| # | Notebook | Description |
|---|----------|-------------|
| 1 | [Agent & Run Level Middleware](agent-framework/agents/azure-ai-agents/1-agent-and-run-level-middleware.ipynb) | Transaction compliance monitoring with middleware scoping |
| 2 | [Magentic Compliance Review](agent-framework/agents/azure-ai-agents/2-magentic-compliance-review-with-human-input.ipynb) | Investment research with human-in-the-loop plan review |
| 3 | [Magentic Investment Research](agent-framework/agents/azure-ai-agents/3-magentic-investment-research.ipynb) | Multi-agent orchestration for investment research reports |

### Phase 3: Observability & Evaluations
**Location:** `observability-and-evaluations/`

Comprehensive evaluation and observability for AI agents.

| # | Notebook | Use Case | Key Concepts |
|---|----------|----------|--------------|
| 1 | [Telemetry](observability-and-evaluations/1-telemetry.ipynb) | Advisory Agent Monitoring | Azure Monitor, custom spans, Application Insights |
| 2 | [Agent Evaluation](observability-and-evaluations/2-agent-evaluation.ipynb) | Advisory Agent Quality | Built-in evaluators (violence, fluency, task_adherence) |
| 3 | [Tool Call Accuracy](observability-and-evaluations/3-tool-call-accuracy-evaluation.ipynb) | Operations Tooling | `builtin.tool_call_accuracy`, JSONL data sources |

[Complete Guide](observability-and-evaluations/README.md)

---

## Troubleshooting & Support

### Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| **Kernel Issues** | `python -m ipykernel install --user --name=ai-foundry-lab` then reload VS Code |
| **Environment Activation** | `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` |
| **Azure Authentication** | `az login --tenant YOUR_TENANT_ID` (Azure CLI preferred over VS Code extension) |
| **Package Import Errors** | Ensure `agent-framework` packages installed in same interpreter as Jupyter |
| **Redis Connectivity** | Update connection string and confirm service is reachable |
| **Application Insights Delay** | Use Live Metrics Stream for real-time debugging |

### Additional Resources

| Resource | Link |
|----------|------|
| **Microsoft Foundry Docs** | [learn.microsoft.com/azure/ai-foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/) |
| **Agent Framework Docs** | [learn.microsoft.com/agent-framework](https://learn.microsoft.com/en-us/agent-framework/overview/agent-framework-overview) |
| **Agent Framework GitHub** | [github.com/microsoft/agent-framework](https://github.com/microsoft/agent-framework) |
| **Azure AI Services** | [learn.microsoft.com/azure/ai-services](https://learn.microsoft.com/azure/ai-services/) |
| **Video Tutorials** | [AI Show](https://learn.microsoft.com/en-us/shows/ai-show/) |
| **GitHub Issues** | [Report bugs or request features](https://github.com/dhangerkapil/agentic-ai-immersion/issues) |

---

## Community & Contributions

| Contribution Type | Description |
|-------------------|-------------|
| **Documentation** | Improve clarity and add examples |
| **Bug Reports** | Help identify and fix issues |
| **Feature Requests** | Suggest new capabilities |
| **Pull Requests** | Contribute code and enhancements |

Please review our [Contributing Guide](CONTRIBUTING.md) for code style, testing requirements, and PR process.

---

## License

**License:** MIT License  
**Repository:** [github.com/dhangerkapil/agentic-ai-immersion](https://github.com/dhangerkapil/agentic-ai-immersion)

---

<div align="center">

**Built with for the AI Developer Community**

*Happy Learning!*

</div>
