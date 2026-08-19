# ResearchGPT
### Smart AI-Powered Research Agent using IBM Granite & Langflow

<div align="center">

![IBM Granite](https://img.shields.io/badge/IBM%20Granite-1261FE?style=for-the-badge&logo=ibm&logoColor=white)
![Langflow](https://img.shields.io/badge/Langflow-0B0F19?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![AI](https://img.shields.io/badge/Agentic%20AI-6E56CF?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-FF6B35?style=for-the-badge)

**An AI-powered research agent designed to streamline literature discovery, document analysis, summarization and research workflows using IBM Granite and Langflow.**

</div>

---

## 📌 Project Overview

**ResearchGPT** is an Agentic AI research project developed as part of the **IBM SkillsBuild for University Engagements (AICTE 2026)** program.

The project addresses **Problem Statement No. 1 — Research Agent**, with the goal of reducing the manual effort involved in exploring academic literature, understanding technical documents and organizing research information.

ResearchGPT explores the use of:

- **IBM Granite foundation models**
- **IBM watsonx.ai**
- **Langflow orchestration**
- **Retrieval-Augmented Generation (RAG)**
- **Natural Language Processing (NLP)**
- **Agentic AI workflows**

The system is designed around a research-assistant workflow where a natural-language research query can be processed through an orchestration layer, relevant information can be retrieved, and the resulting context can be passed to an AI reasoning model for structured research assistance.

> **Note:** This repository represents an academic/industry-program project and architectural prototype. Some capabilities described in the roadmap are planned extensions rather than currently deployed production features.

---

## 🎯 Objectives

ResearchGPT focuses on improving common research workflows such as:

- Discovering relevant academic literature
- Processing technical documents
- Summarizing research material
- Extracting important findings
- Organizing references and research information
- Generating structured research outputs
- Exploring AI-assisted hypothesis generation

The broader objective is to demonstrate how **Agentic AI + RAG + enterprise LLM infrastructure** can be combined to support research-oriented workflows.

---

## ✨ Core Capabilities

### 🌐 Research Query Processing

Accepts natural-language research questions and processes them through an AI-oriented workflow.

### 📄 Document & Literature Analysis

Designed to process research papers, technical documents and other research material to identify important information.

### 🧠 AI-Powered Summarization

Uses an LLM-based reasoning layer to generate concise, structured summaries from available research context.

### 🔎 Retrieval-Augmented Generation

The architecture supports retrieval of relevant contextual information before generation, helping ground AI responses in retrieved research material.

### 📑 Research Information Structuring

Designed to organize research findings into structured outputs such as summaries, references and research reports.

### 💡 Research Exploration

The system architecture can be extended toward AI-assisted insight discovery and hypothesis exploration.

---

# 🏗️ System Architecture

## Architecture Blueprint

![ResearchGPT Architecture](architecture-blueprint.png)

---

## 🔄 Data Flow

```text
┌─────────────────────────────┐
│       User Research Query   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      Langflow Workflow      │
│  Orchestration & Routing    │
└──────────────┬──────────────┘
               │
       ┌───────┴────────┐
       ▼                ▼
┌───────────────┐  ┌─────────────────┐
│ Literature    │  │ Research        │
│ Retrieval     │  │ Documents / RAG │
│ APIs / Sources│  │ Context         │
└───────┬───────┘  └────────┬────────┘
        │                   │
        └─────────┬─────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │    Context + Prompt  │
       └──────────┬───────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │     IBM watsonx.ai   │
       │                      │
       │   IBM Granite Model  │
       └──────────┬───────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │   Research Output    │
       │                      │
       │ • Summaries          │
       │ • Insights           │
       │ • References         │
       │ • Structured Reports │
       └──────────────────────┘
