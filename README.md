# awesome-ai-agents
精选 AI Agent 项目合集，涵盖框架、工具与实战案例，持续更新。
# AI Agent Demos
> Collection of AI Agent demo projects, **for demonstration & portfolio only, not for production**.
> All demos focus on Agent core capabilities: task planning, tool calling, self-reflection, iterative loop.
> Tech stack: n8n, LLM, SerpAPI, LangGraph(Python)

## 📂 Project List
### 1. Intelligent Literature Survey Agent (n8n Low-code Version) ✅
> 低代码学术文献调研Agent（n8n可视化工作流）
- 🎯 Goal: Input a research topic → Agent autonomously plan search keywords, retrieve arXiv papers, extract abstract information, self-reflect whether information is sufficient, perform secondary search iteratively, finally output literature review + comparison table.
- ✨ Agent Core Features
  - Task Planner: Generate academic search keywords
  - Tool Calling: SerpAPI search `site:arxiv.org` paper snippets
  - Information Extraction: Structured parsing of paper abstract
  - Self-Reflection & Loop: Judge whether to continue searching (max 2 rounds, avoid infinite loop)
  - Report Writer: Generate markdown literature review + comparison table
- 🛠 Tech Stack
  - n8n (visual workflow orchestration)
  - LLM (OpenAI / Volcano Ark / Tongyi)
  - SerpAPI (Google academic search for arXiv)
- 📁 Folder: `literature-survey-agent-n8n/`
- 📌 Notes: Only read abstract/snippet, **no PDF parsing, no commercial use, demo only**.


## 🚀 Quick Start - Literature Survey Agent
### Prerequisite
1. Deploy n8n locally or use n8n cloud
```bash
# Local n8n start
docker run -it --rm -p 5678:5678 n8nio/n8n

