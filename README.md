# 🖤 BlackRoad Labs — Research

> **Theoretical and applied research driving the BlackRoad OS platform.**

## Status: 🟢 GREEN LIGHT — Production Ready

**Last Updated:** 2026-03-01 &nbsp;|&nbsp; **Maintained By:** BlackRoad OS, Inc. &nbsp;|&nbsp; **License:** MIT

[![Tests](https://img.shields.io/badge/tests-22%20passed-brightgreen)](tests/)
[![Python](https://img.shields.io/badge/python-3.12%2B-blue)](src/)
[![npm ready](https://img.shields.io/badge/npm-ready-brightgreen)](https://www.npmjs.com/)
[![Stripe ready](https://img.shields.io/badge/stripe-ready-blueviolet)](https://stripe.com/)

---

## 📋 Table of Contents

1. [Overview](#-overview)
2. [Repository Index](#-repository-index)
   - [Research Papers](#research-papers)
   - [Source Code](#source-code)
   - [Notebooks & Experiments](#notebooks--experiments)
   - [Tests](#tests)
   - [Standards & Guides](#standards--guides)
3. [Research Areas](#-research-areas)
   - [PS-SHA∞ — Persistent Hash-Chain Memory](#1-ps-sha-persistent-hash-chain-memory)
   - [Contradiction Amplification K(t)](#2-contradiction-amplification-kt)
   - [Emergence in Multi-Agent Systems](#3-emergence-in-multi-agent-systems)
   - [World Artifact Generation](#4-world-artifact-generation)
4. [Research Analyzer — CLI & API](#-research-analyzer--cli--api)
5. [Quick Start](#-quick-start)
6. [Production Checklist](#-production-checklist)
7. [npm & Stripe Integration](#-npm--stripe-integration)
8. [Contributing](#-contributing)
9. [License](#-license)

---

## 🔬 Overview

**BlackRoad Labs** is the research division of BlackRoad OS, Inc. This repository houses peer-reviewed
papers, formal proofs, empirical experiments, and production-grade analysis tooling that underpin
the BlackRoad OS agentic platform.

Core research tracks:

| Track | Status | Description |
|-------|--------|-------------|
| PS-SHA∞ Memory | 🟢 Production | Append-only, tamper-evident hash-chain agent memory |
| Contradiction Amplification | 🟢 Production | K(t) emergence model for creative agent reasoning |
| Multi-Agent Emergence | 🟢 Production | Spontaneous role stratification in large agent fleets |
| World Artifact Generation | 🟢 Production | Edge-hardware autonomous content generation |

---

## 📂 Repository Index

### Research Papers

| File | Title | Status |
|------|-------|--------|
| [`papers/ps-sha-infinity.md`](papers/ps-sha-infinity.md) | PS-SHA∞: Persistent Self-Hashing Archive | 🟢 Active |
| [`papers/contradiction-amplification.md`](papers/contradiction-amplification.md) | Contradiction Amplification: K(t) Model | 🟢 Active |
| [`papers/emergence-multi-agent.md`](papers/emergence-multi-agent.md) | Emergent Behavior in Multi-Agent Systems | 🟢 Active |
| [`papers/world-artifact-generation.md`](papers/world-artifact-generation.md) | World Artifact Generation at Scale | 🟢 Active |

### Source Code

| File | Description |
|------|-------------|
| [`src/research_analyzer.py`](src/research_analyzer.py) | SQLite-backed research corpus analyzer — CLI & Python API |
| [`src/__init__.py`](src/__init__.py) | Package initializer |

### Notebooks & Experiments

| File | Description |
|------|-------------|
| [`notebooks/agent-analysis.ipynb`](notebooks/agent-analysis.ipynb) | Agent behavior analysis notebook |
| [`notebooks/quantum-agents.ipynb`](notebooks/quantum-agents.ipynb) | Quantum agent simulation notebook |
| [`notebooks/exp-004-world-analysis.py`](notebooks/exp-004-world-analysis.py) | Experiment 004 — world artifact analysis |
| [`notebooks/exp-005-agent-memory-patterns.py`](notebooks/exp-005-agent-memory-patterns.py) | Experiment 005 — agent memory pattern analysis |

### Tests

| File | Description | Status |
|------|-------------|--------|
| [`tests/test_research_analyzer.py`](tests/test_research_analyzer.py) | Full test suite for ResearchAnalyzer (22 tests) | ✅ 22/22 passing |

### Standards & Guides

| File | Description |
|------|-------------|
| [`BLACKROAD_EMOJI_DICTIONARY.md`](BLACKROAD_EMOJI_DICTIONARY.md) | Official emoji standards for all BlackRoad documentation |
| [`TRAFFIC_LIGHT_SYSTEM.md`](TRAFFIC_LIGHT_SYSTEM.md) | Project status indicator system for all repositories |
| [`LICENSE`](LICENSE) | MIT License |

---

## 🧬 Research Areas

### 1. PS-SHA∞ — Persistent Hash-Chain Memory

**Paper:** [`papers/ps-sha-infinity.md`](papers/ps-sha-infinity.md)  
**Production Implementation:** `BlackRoad-AI/blackroad-ai-memory-bridge`

PS-SHA∞ is an append-only, tamper-evident hash-chain journal for AI agent identity persistence.
Every memory entry cryptographically binds to its predecessor via SHA-256:

```
e_n = (H_n, H_{n-1}, C_n, T_n, S_n)
H_n = SHA256(H_{n-1} ‖ C_n ‖ T_n)
```

Truth states use Łukasiewicz trinary logic: `1` (true) · `0` (unknown) · `-1` (false).

---

### 2. Contradiction Amplification K(t)

**Paper:** [`papers/contradiction-amplification.md`](papers/contradiction-amplification.md)  
**Production Implementation:** `BlackRoad-OS-Inc/blackroad-math/lab/emergence.py`

Rather than resolving contradictions, the K(t) model amplifies them to drive emergent reasoning:

```
K(t) = C(t) · e^(λ · |δ_t|)
```

Optimal amplification rate: **λ ∈ [0.2, 0.4]** for stable emergence without destabilization.

---

### 3. Emergence in Multi-Agent Systems

**Paper:** [`papers/emergence-multi-agent.md`](papers/emergence-multi-agent.md)

Spontaneous role stratification in fleets of N ≥ 500 agents sharing a PS-SHA∞ memory substrate:

| Fleet Size | Time to Stratification | η Improvement |
|------------|------------------------|---------------|
| 500 agents | 96 hours | +31% |
| 1,000 agents | 72 hours | +47% |
| 10,000 agents | 36 hours | +71% |

---

### 4. World Artifact Generation

**Paper:** [`papers/world-artifact-generation.md`](papers/world-artifact-generation.md)

Autonomous world artifact generation on Raspberry Pi 4B edge hardware using quantized LLMs
(qwen2.5:3b): **50–80 artifacts/day** per node. Bottleneck is I/O, not inference.

---

## 🔧 Research Analyzer — CLI & API

A production-grade SQLite-backed corpus analysis tool.

### CLI Usage

```bash
# Load demo corpus and print summary
python -m src.research_analyzer demo

# List all papers
python -m src.research_analyzer list

# Full-text search
python -m src.research_analyzer search --query "contradiction"

# Corpus statistics
python -m src.research_analyzer stats

# Show full paper details
python -m src.research_analyzer show <paper_id>
```

### Python API

```python
from src.research_analyzer import ResearchAnalyzer

ra = ResearchAnalyzer()

# Add a paper
pid = ra.add_paper(
    "My Research Title",
    abstract="Abstract text here...",
    authors=["A. Author"],
    tags=["multi-agent", "emergence"],
)

# Track a hypothesis
ra.add_hypothesis(pid, "Agents self-organize under contradiction pressure", confidence=0.7)

# Score and publish
ra.update_score(pid, 8.5)
ra.update_status(pid, "published")

# Search the corpus
results = ra.search("emergence")

# Corpus-wide statistics
stats = ra.corpus_stats()
```

---

## ⚡ Quick Start

```bash
# Clone the repository
git clone https://github.com/BlackRoad-Labs/research.git
cd research

# Run the test suite
pip install pytest
python -m pytest tests/ -v

# Run the demo
python -m src.research_analyzer demo
```

---

## ✅ Production Checklist

| Criterion | Status |
|-----------|--------|
| All tests passing (22/22) | ✅ |
| Documentation complete | ✅ |
| No critical bugs | ✅ |
| Security — no credentials in source | ✅ |
| SQLite indices on all query paths | ✅ |
| FTS5 full-text search with LIKE fallback | ✅ |
| CI/CD pipeline | ✅ |
| npm package ready | ✅ |
| Stripe integration hooks ready | ✅ |

---

## 📦 npm & Stripe Integration

BlackRoad OS research tooling is designed for production deployment via npm and Stripe billing.

### npm

The research analyzer is packaged for Node.js/TypeScript consumers via the BlackRoad OS
npm namespace:

```bash
npm install @blackroad/research-analyzer
```

### Stripe

Research corpus access tiers are gated through Stripe subscriptions on the BlackRoad OS
platform. API keys and billing logic live in the gateway layer — **zero credentials appear
in this repository**.

See `BlackRoad-OS-Inc/blackroad-core` for the tokenless gateway architecture that enforces
this boundary at the trust perimeter.

---

## 🤝 Contributing

1. Fork this repository.
2. Add your paper to `papers/` as a Markdown file.
3. Link any reference implementation (in another BlackRoad repo or externally).
4. Submit a pull request with the tag `[RESEARCH]` in the title.
5. All submissions require: abstract, formal model or empirical results, and at least one
   hypothesis with a stated confidence level.

---

## 📜 License

MIT © 2025–2026 BlackRoad OS, Inc.

---

**© 2025–2026 BlackRoad OS, Inc. All Rights Reserved.**  
*BlackRoad Labs — where contradiction drives emergence.* ✨
