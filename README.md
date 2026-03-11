# AI Trading Scout 🤖📈

**AI Trading Scout** is a closed-loop quantitative trading research and backtesting system. It integrates LLM-driven stock screening with automated performance tracking and expert-level validation to bridge the gap between raw market data and actionable trading insights.

---

## 🌟 Core Features

- **LLM-Driven Decision Engine**: Utilizes state-of-the-art Large Language Models to analyze multi-dimensional technical indicators and generate structured trading reports.
- **Industrial Data Pipeline**: Automated conversion from `XLSX` to `CSV`, featuring robust cleaning logic including exchange filtering (e.g., Beijing Stock Exchange), delisting checks, and limit-up/down exclusion.
- **Structured Performance Logging**: Automatically parses non-structured AI reports to extract stock codes and reconstruct historical entry prices ($P_0$) for precise tracking.
- **Advanced Backtesting Engine**: A high-performance module that calculates $P_7$ (7-day return), $M_7$ (7-day maximum touch), and Alpha returns against market benchmarks.
- **High-Efficiency Memory Processing**: Optimized "Batch Fetch & Memory Compute" logic to minimize data API calls and maximize execution speed.

---

## 🏗 System Architecture



### 1. Data Engineering
- `convert_xlsx_to_csv.py`: Standardizes raw market data formats.
- `data_loader.py`: The data cleaning hub responsible for code formatting, exchange filtering, and Top/Bottom N percentile screening.

### 2. AI Intelligence Layer
- `config.py`: Centralized configuration for model parameters, API credentials, and strategy thresholds.
- `main_agent.py`: The core entry point for the AI agent, handling prompt engineering and report generation.
- `batch_runner.py`: A historical sample generator for automated batch processing of past trading days.

### 3. Analytics & Backtesting
- `performance_logger.py`: Bridges the gap between AI decisions and structured CSV logs.
- `performance_backtester_expert.py`: The quantitative validation engine for calculating Alpha and profitability metrics.

---

## 📊 Quantitative Metrics (KPIs)

The system evaluates strategy performance through a multi-dimensional metric framework:

| Metric | Definition | Practical Value |
| :--- | :--- | :--- |
| **$P_7$** | 7-Day Closing Return | Measures the absolute profitability of a one-week holding period. |
| **$M_7$** | 7-Day Max Reach | Identifies short-term explosive potential to optimize take-profit targets. |
| **Alpha** | Excess Return | Measures the strategy's ability to outperform the benchmark (e.g., CSI 300). |
| **Win Rate** | Strategy Accuracy | Validates the statistical probability of profitable trades. |
| **P/L Ratio** | Profit/Loss Ratio | Evaluates the risk-reward efficiency and strategy robustness. |



---

## 🚀 Quick Start

### 1. Installation
```bash
git clone [https://github.com/YourUsername/AI_Trading_Scout_v1.git](https://github.com/YourUsername/AI_Trading_Scout_v1.git)
cd AI_Trading_Scout_v1
pip install -r requirements.txt


# AI Trading Scout 🤖📈

**AI Trading Scout** 是一个闭环量化交易研究与回测系统。它将基于大语言模型（LLM）的股票筛选逻辑与自动化的性能追踪、专家级回测验证相结合，旨在打通原始市场数据与实战投资决策之间的鸿沟。

---

## 🌟 核心特性

- **大模型驱动决策引擎**：利用尖端大语言模型（LLM）对多维技术指标进行逻辑推理，生成深度结构化的交易策略报告。
- **工业级数据管线**：支持 `XLSX` 到 `CSV` 的全自动转换，内置健壮的数据清洗逻辑，包括板块过滤（如剔除特定高波动板块）、停牌检测以及涨跌幅限制规避。
- **结构化性能记录**：自动解析非结构化的 AI 决策报告，精准提取标的代码并还原历史入场价格（$P_0$），实现全自动样本记录。
- **专家级回测引擎**：高性能回测模块，支持计算 $P_7$（7日收盘收益）、$M_7$（7日最高触达）以及相对于市场基准的 Alpha 超额收益。
- **内存优化处理**：采用“批量拉取+内存对齐计算”逻辑，极小化外部数据调用频率，确保系统在大规模数据回测时的稳定性与速度。

---

## 🏗 系统架构



### 1. 数据工程层
- `convert_xlsx_to_csv.py`: 标准化原始市场数据格式。
- `data_loader.py`: 数据清洗中心，负责代码规范化、特定板块过滤及 Top/Bottom N 分位数筛选。

### 2. AI 智能决策层
- `config.py`: 系统全局配置中心，管理模型参数、API 凭证及策略阈值。
- `main_agent.py`: AI 智能体核心入口，处理提示词工程（Prompt Engineering）与报告生成。
- `batch_runner.py`: 历史样本生成工具，支持对过去交易日进行全自动批量处理。

### 3. 性能分析与回测层
- `performance_logger.py`: 连接 AI 决策与结构化日志的桥梁，负责数据存证。
- `performance_backtester_expert.py`: 量化验证引擎，负责 Alpha 指标及策略盈亏分布计算。

---

## 📊 核心量化指标 (KPIs)

系统通过多维度指标框架评估策略的真实“战力”：

| 指标 | 定义 | 实战价值 |
| :--- | :--- | :--- |
| **$P_7$** | 7日收盘收益率 | 衡量一周持仓周期的绝对盈利能力。 |
| **$M_7$** | 7日最高触达 | 捕捉标的的短线爆发力，用于优化止盈目标位。 |
| **Alpha** | 超额收益 | 衡量策略跑赢基准指数（如沪深300）的纯选股能力。 |
| **Win Rate** | 策略胜率 | 验证策略在统计学意义上的盈利概率。 |
| **P/L Ratio** | 盈亏比 | 评估策略的风险报酬比及抗风险韧性。 |



---

## 🚀 快速开始

### 1. 环境安装
```bash
git clone [https://github.com/YourUsername/AI_Trading_Scout_v1.git](https://github.com/YourUsername/AI_Trading_Scout_v1.git)
cd AI_Trading_Scout_v1
pip install -r requirements.txt
