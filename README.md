# 🚀 Project Sentinel:
## "An Autonomous Meta-Learning AI Quant System with Volatility-Adjusted Risk Governance for Korea Stock Market (KOSPI/KOSDAQ)"

🔒 **Repository Security & Compliance Note**

*The source code of Project Sentinel is hosted in a private repository to protect proprietary quantitative strategies, trade secrets, and brokerage API credentials. This public repository serves as the technical product specification, architecture blueprint, and validation documentation.*

## 🚀 Executive Summary
**Project Sentinel** is an autonomous, data-driven AI quantitative trading framework optimized for the KOSPI/KOSDAQ markets. Engineered via LangGraph and FastAPI, the system shifts away from rigid, rule-based algorithmic trading by implementing a stateful, multi-agent topology. It features a self-calibrating **Meta-Learning feedback loop** that monitors its own performance metrics (Win Rate, MDD) and dynamically adjusts market regime-switching variables and risk exposure in real-time.

As an AI Product Manager, I established an **AI-Driven Development (AIDD)** workflow, partnering with **Claude** as a technical co-founder to aggressively accelerate the product lifecycle from conceptual specification to quantitative backtesting validation.

## 📊 Product Architecture & Data Flow
Sentinel leverages **LangGraph** to manage a stateful Directed Acyclic Graph (DAG), ensuring seamless context propagation (`AgentState`) across decoupled analytical and execution nodes.

### Agent 1: Macro Agent (macro.py)
### Agent 2: Sector Agent (sector.py)
### Agent 3: Stock Agent (stock.py)
### Agent 4: Execution Agent (execution.py)
### Agent 5: Feedback Agent (feedback.py)
