# 🧠 LLM Voice & Text Agents

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Framework](https://img.shields.io/badge/Framework-OpenAI_API-orange.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

---

This repository showcases a collection of **six Large Language Model (LLM)–powered voice and text agents** that deliver **real-time AI news and financial insights**.  
Each agent demonstrates a different level of **capability**, **restriction**, and **coordination**, exploring how LLMs can act as **autonomous research coordinators** rather than simple chatbots.

---

## 🤖 Overview of the 6 Agents

| # | Agent Name | Type | Description |
|:-:|-------------|------|-------------|
| **1** | 🗣️ Simple Voice Agent | Voice | Speaks out the **latest AI news** using text-to-speech. |
| **2** | 💬 Text News Agent | Text | Displays **summarized AI news** in text format. |
| **3** | 🔒 Restricted Voice Agent | Voice | Voice-enabled, but **strictly limited** to AI news only. Off-topic questions are rejected. |
| **4** | 💹 Financial Context Agent | Text | Enhances AI news with **real-time financial data** via `yfinance`. |
| **5** | 🧩 Callback-Aware Agent | Text + Voice | Implements **callback systems** for policy enforcement and auditability. |
| **6** | 🎙️ Multi-Agent Podcast System | Voice | A **two-agent system** — one producer and one podcaster — that creates a **dynamic AI news podcast**. |

---

## 💼 Project Goals

- Demonstrate **scalable, transparent LLM design**  
- Showcase **safe delegation** across multiple specialized agents  
- Combine **real-time data (news + finance)** with **interactive voice & text**  
- Integrate **callback & guardrail mechanisms** for safe automation  

---

## ⚙️ Core Features

- 🧭 **5-Step Research Workflow** → Clarify → Search → Analyze → Enrich → Deliver  
- 💬 **Interactive Conversations** — agents engage users dynamically  
- 💹 **Financial Context Integration** — real-time stock data via Yahoo Finance  
- 🧾 **Audit Logs** — each agent maintains a `process_log` for transparency  
- 🚧 **Scope Guardrails** — focused on AI and NASDAQ-listed companies only  
- ⚠️ **Graceful Error Handling** — missing data or off-topic prompts handled safely  

---

## 🧩 Architecture Overview


---

## 🔁 Callback System

The **callback-aware agents** use policy-based hooks to ensure transparency and control.

| Callback Type | Description |
|----------------|--------------|
| `before_agent_callback` | Runs before the agent executes |
| `after_agent_callback` | Runs after the agent finishes |
| `before_tool_callback` | Runs before a tool is called |
| `after_tool_callback` | Logs results after a tool executes |
| `before_model_callback` | Triggers before LLM reasoning |
| `after_model_callback` | Logs or moderates responses |

These guardrails enforce **domain filtering**, **source control**, and **policy transparency**.

---

## 🎙️ Agent #6: Multi-Agent Podcast System

A multi-agent orchestration that generates a **two-host AI news podcast**.

| Role | Description |
|------|--------------|
| 🎧 **Podcaster Agent** | Converts structured news into a natural conversation between *Joe* and *Jane*. |
| 🧑‍💻 **Root Agent** | Acts as **producer**, handling research, finance context, and report compilation. |

### 🪶 Example Workflow
1. Root Agent: “Okay, I’ll start researching the latest AI news for NASDAQ-listed US companies…”  
2. Searches the web for recent AI-related news.  
3. Extracts tickers and fetches financial data using `yfinance`.  
4. Saves findings in `ai_research_report.md`.  
5. Converts data into a **scripted conversation** (Joe = enthusiastic, Jane = analytical).  
6. Passes the script to the **Podcaster Agent** to generate TTS audio.  
7. Finishes with confirmation:  
   > “All done. I’ve compiled the report and generated the podcast audio file.”

---

## 🧠 Built With

- **Python 3.10+**
- **OpenAI API / LLM Frameworks**
- **SpeechRecognition / pyttsx3** — for voice I/O  
- **Streamlit / Gradio** — for UI interfaces  
- **yfinance** — for stock and market data  
- **Custom Callback Engine** — for policy and transparency control  

---



