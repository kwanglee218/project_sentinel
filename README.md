# 🚀 Project Sentinel
## "An Autonomous Meta-Learning AI Quant System with Volatility-Adjusted Risk Governance for Korea Stock Market (KOSPI/KOSDAQ)"

🔒 **Repository Security & Compliance Note**

*The source code of Project Sentinel is hosted in a private repository to protect proprietary quantitative strategies, trade secrets, and brokerage API credentials. This public repository serves as the technical product specification, architecture blueprint, and validation documentation.*

## 🚀 Executive Summary
**Project Sentinel** is an autonomous, data-driven AI quantitative trading framework optimized for the Korean Stock Market (KOSPI/KOSDAQ). Engineered via LangGraph and FastAPI, the system shifts away from rigid, rule-based algorithmic trading by implementing a stateful, multi-agent topology. It features a self-calibrating **Meta-Learning feedback loop** that monitors its own performance metrics (Win Rate, MDD) and dynamically adjusts market regime-switching variables and risk exposure in real-time.

As an AI Product Manager, I established an **AI-Driven Development (AIDD)** workflow, partnering with **Claude** as a technical co-founder to aggressively accelerate the product lifecycle from conceptual specification to quantitative backtesting validation.

## 📊 Product Architecture & Data Flow
Sentinel leverages **LangGraph** to manage a stateful Directed Acyclic Graph (DAG), ensuring seamless context propagation (`AgentState`) across decoupled analytical and execution nodes.

<img width="395" height="450" alt="image" src="https://github.com/user-attachments/assets/508c9fef-ebc2-4224-99e9-164928b1bca9" />

## Agent 1: Macro Agent (macro.py)
Extracts macroeconomic indices from the Federal Reserve Economic Data (FRED) API. Retrieved metrics include the federal funds rate, CPI growth, the yield curve, the VIX, the USD index, high-yield spreads, and the USD/KRW exchange rate.

Based on these market conditions, the Macro Agent dynamically determines the optimal stock weight for the portfolio.

## Task 1. PCA-Based Market Scoring

To resolve multi-collinearity issue and to extract the true underlying market regime, PCA is used.
### a. Standardization
#### Factor normalization using StandardScaler.

### b. Dynamic Component Selection
#### The algorithm automatically selects the number of Principal Components (PCs) required to capture at least 70% of the cumulative explained variance.

### c. Sign Alignment
#### For components that show a positive correlation with the VIX (Volatility Index), the agent inverts their signs. This mathematically aligns the output so that a higher score consistently represents a healthy, favorable market environment (Risk-on).

### d. Empirical Scoring
#### The agent evaluates the empirical percentile of the latest data point within the lookback window and computes a weighted average score (bounded between 0 and 1) based on each component’s explained variance ratio.

## Task 2. Sigmoid-Based Weight Mapping:

## Task 3. Risk Filter:



### Agent 2: Sector Agent (sector.py)
### Agent 3: Stock Agent (stock.py)
### Agent 4: Execution Agent (execution.py)
### Agent 5: Feedback Agent (feedback.py)
