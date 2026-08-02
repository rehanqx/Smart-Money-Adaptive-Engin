# 🔄 Smart Money Concepts V4.5 — Adaptive Intelligence Engine

![Pine Script Version](https://img.shields.io/badge/Pine_Script-v6-blue?style=for-the-badge&logo=tradingview)
![TradingView](https://img.shields.io/badge/TradingView-Indicator-00897B?style=for-the-badge&logo=tradingview)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

An institutional-grade **Smart Money Concepts (SMC) Adaptive Market Profile & Dynamic Weighting Engine** written in **Pine Script v6** for TradingView.

V4.5 acts as the self-adjusting brain of the SMC architecture. Instead of using static, one-size-fits-all scoring rules, V4.5 detects real-time regime shifts and automatically switches between specialized trading profiles—dynamically re-weighting sub-modules to match prevailing market conditions (*Trend Following, Range Trading, Breakout / Volatility, Neutral*).

---

## 🔥 Key Features

* **🎛️ Automatic Context Profile Engine:** Dynamically identifies market regimes and switches profiles in real time:
  * **Trend Following:** Prioritizes Market Structure (25%), Order Blocks (20%), and FVGs (15%) when ADX ≥ 25.
  * **Range Trading:** Prioritizes Liquidity Pools (30%), Order Blocks (25%), and FVGs (25%) during low ADX (< 20) ranges.
  * **Breakout / Volatility:** Prioritizes Structure Events / BOS (30%), FVGs (25%), and Order Blocks (25%) on impulse expansions.
  * **Neutral / Transition:** Balances baseline weights evenly across modules.
* **⚖️ Dynamic Weight & Threshold Adaptation:** Dynamically reallocates internal weight percentages (SUM = 100%) and adjusts decision score execution cutoffs based on active volatility profiles.
* **⏱️ Profile Duration & Stability Analytics:** Tracks exact bar durations (`profile_duration`) and stability scores to prevent whipsawing during choppy market transitions.
* **📊 Master Adaptive Dashboard:** On-screen HUD displaying active profile types, adaptive decision scores, dynamic thresholds, real-time weight allocations, and risk profiles.
* **🔌 Open Modular Output API:** Standardized variable exports (`export_CurrentProfile`, `export_AdaptiveDecisionScore`, `export_AdaptiveReadiness`, `export_CurrentModuleWeights`) exposed for **Strategy Execution (V5)** and **MT5 EA Automation (V5.5)**.

---

## 📊 Dashboard Overview

The built-in master adaptive HUD displays key dynamic parameters:

| Metric | Description |
| :--- | :--- |
| **Active Market Context Profile** | Real-time active regime (*Trend Following, Range Trading, Breakout / Volatility, Neutral*) |
| **Adaptive Decision Score** | Dynamic profile-weighted score (0–100) and institutional rating |
| **Dynamic Decision Threshold** | Adaptive execution score threshold calibrated to current volatility |
| **Adaptive Readiness Status** | Execution clearance flag (*Ready for Execution, Building / Neutral*) |
| **Adaptive Risk Environment** | Risk level assessment (*Low Risk, Moderate Risk, High Risk*) |
| **Profile Duration** | Counter measuring bar duration of the active market regime |
| **Dynamic Weight Allocations** | Live percentage weight distributions across sub-indicator engines |

---

## 🛠️ Configuration & Settings

### 1. Adaptive Intelligence Settings
* `Enable Dynamic Profile & Weight Adaptation` *(Default: True)*: Master toggle for adaptive re-weighting.
* `Profile Switching Sensitivity` *(Default: Normal)*: Profile switching responsiveness (*Conservative, Normal, Aggressive*).
* `Minimum Adaptive Decision Threshold` *(Default: 75)*: Base score requirement for execution readiness.

### 2. Visual & Color Standards
* Toggles for On-Chart Profile Label and Dashboard HUD.
* Dynamic color coding for Trend Following (Green), Range Trading (Blue), Breakout/Volatility (Purple), and Neutral (Yellow) profiles.

---

## 💻 Installation & Usage

1. Open **[TradingView](https://www.tradingview.com)**.
2. Open the **Pine Editor** tab at the bottom of your workspace.
3. Create a new script, clear the default template, and paste the code from `SMC_Adaptive_Engine_v4_5.pine`.
4. Click **Save** and then select **Add to Chart**.

---

## ⚡ Real-Time Alerts Included

Includes native TradingView alert conditions for automated execution and webhooks:
* ⚡ **Adaptive Market Profile Changed**
* ✅ **Adaptive Market Ready for Execution**


---

## 📜 License

This project is open-source and released under the [MIT License](LICENSE).
