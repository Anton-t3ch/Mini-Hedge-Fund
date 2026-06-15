<h3>Mini Hedge Fund: Multi-Agent Reinforcement Learning Swarm An institutional-grade algorithmic trading framework that utilizes deep reinforcement learning to trade the SPY ETF. The system features a decoupling of data engineering, mathematical risk management, and agent simulation to create a production-ready, modular quantitative trading pipeline.
📊 System Architecture The project is structured modularly to separate concerns across data processing, risk management, and machine learning training:

🛠️ Tech Stack & AI Orchestration This repository was developed using a hybrid, multi-agent AI co-pilot workflow designed for high-efficiency code generation and deep mathematical validation:

Data & Feature Engineering (Local): Qwen 3.6-35B-A3B via Ollama for local, high-speed data frame manipulation and boilerplate execution testing.

RL Architecture & Risk Management (Cloud): DeepSeek V4 Pro via API to leverage chain-of-thought reasoning for complex financial math and Gymnasium reward function design.

Core Libraries: Python 3.11+, Gymnasium, Stable-Baselines3, pandas_ta, Plotly.

📈 Alpha Factors & Feature Engineering The data_pipeline.py module ingests historical OHLCV data for SPY and engineers structural market features:

Average True Range (ATR_14): Establishes the baseline volatility for position sizing and dynamic stop-loss calculations.

MACD (12, 26, 9): Captures multi-timeframe momentum and trend divergences.

Rolling Volume Profile (VP_POC_20): A custom numpy-optimized indicator calculating the 20-day horizontal volume nodes to identify the daily Point of Control (POC).

🛡️ Risk Management Infrastructure The system employs a strict, zero-trust risk wrapper (risk_manager.py) that acts as a hard boundary before any agent trade execution:

Dynamic Volatility Stops: Stop-loss distances scale automatically based on a multiplier of the current 14-day ATR.

Maximum Drawdown Kill-Switch: Automatically halts the simulation or trading loop if account capital drops below a predefined historical threshold.

Kelly Criterion/Fixed-Fractional Sizing: Positions are strictly sized according to account volatility, preventing catastrophic leverage risk.</h3>
