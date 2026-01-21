# SignalX: Institutional Grade Crypto Quant Architecture

> **The first open-architecture trading system implementing Forensic Snapshot Replay™ and Adaptive Regime Guard.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Architecture](https://img.shields.io/badge/Architecture-Event--Driven-green)](https://github.com/)

## 📜 Manifesto
Retail trading bots are broken. They rely on lagging indicators (RSI, MACD) and "black box" signals that often repaint history to hide losses. 

**SignalX** changes the paradigm. It is not just a bot; it is a **Forensic Analysis Engine**. Every decision made by the AI is cryptographically hashed and linked to a snapshot of the exact market conditions (Order Book, Volatility Z-Score, Delta) at that millisecond.

**We do not trust. We verify.**

---

## 🧬 Core Technology Stack

### 1. Forensic Snapshot Replay™ (FSR)
Unlike traditional systems that output a simple "Buy", SignalX generates a **SNAP ID** (SHA-256 Hash). 
*   **Input:** Price, Volume Delta, Taker Ratio, Volatility, Macro Data (S&P 500).
*   **Output:** An immutable record proving *why* the trade was taken.
*   **Result:** 100% transparent statistics. Impossible to fake or delete.

### 2. Adaptive Guard (Psychologist Mode)
Markets have regimes: **Trending** (Low Entropy) and **Choppy** (High Entropy).
*   SignalX utilizes an **Adaptive Thresholding Mechanism** based on Shannon Entropy.
*   The system hard-blocks trades during high-entropy noise to prevent "meat grinder" capital erosion.

### 3. Dual-Model Consensus
We treat ML predictions as a voting system, not absolute truth. 
*   **Model A (Lead):** XGBoost (Gradient Boosting) for non-linear pattern recognition.
*   **Model B (Shadow):** Random Forest for structural stability and overfitting protection.

---

## 📚 Technical Documentation & Results
- 📊 **Performance Validation:** [View Live Signal Logs](./PERFORMANCE.md)
- 🛡️ **Transparency Policy:** [Why we are in Private Beta](./TRANSPARENCY.md)
- 🧠 **Risk Architecture:** [Deep Dive into Adaptive Guard Logic](./docs/ADAPTIVE_GUARD.md)
- 📦 **Data Samples:** [Explore Forensic Metrics on Hugging Face](https://huggingface.co/datasets/signalxpert/SignalX-Crypto-Forensic-Metrics)

---

## 🚀 Roadmap (v9.0 NEON)
- [x] **v8.3 Core:** Institutional feature contract & FMP Macro integration.
- [ ] **Entropy Filter:** Scipy-based automated chaos detection.
- [ ] **Stablecoin Velocity:** Tracking USDT inflows as "Market Oxygen".
- [ ] **RLHF Module:** Reinforcement Learning from Human Feedback.

---

## ⚠️ Disclaimer
This repository contains the documentation, feature contracts, and performance logs of SignalX. The core execution engine (`trade_engine.py`) and pre-trained models (`.pkl`) are proprietary to mitigate front-running risks.

**SignalX is an analytical tool, not a financial advisor. Trade at your own risk.**
