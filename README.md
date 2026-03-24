# SciCode-Style Benchmark for Process Systems Engineering (PSE)

## Overview

This repository contains a **scientific coding benchmark** designed to evaluate the ability of large language models (LLMs) to solve **multi-step, physics-based problems** in Process Systems Engineering.

The benchmark is inspired by the SciCode framework and focuses on:
- Numerical reasoning
- Physical modeling
- Deterministic scientific computation

---

## Benchmark Structure

The benchmark consists of **one problem with three interconnected subtasks**:

### Subtask 1: Reaction Modelling
- Carbonation conversion using the shrinking-core model
- Interpolation over numerically generated data

### Subtask 2: Reactor Hydrodynamics
- Average pressure estimation using the Ergun equation
- Integration across reactor height

### Subtask 3: CO₂ Sequestration
- End-to-end computation of total CO₂ captured
- Combines outputs and process parameters

---

## Key Features

- End-to-end execution in **Google Colab Pro**
- Uses **Gemini 3 Pro as an agent**
- Fully automated (no manual intervention required)
- Deterministic unit testing
- AST-based output validation
- JSON-based scoring output

---

## Repository Contents

- `Benchmark_for_Gemini.ipynb` → Main benchmark notebook  
- `Golden_Solution.ipynb` → Reference implementation  
- `unit_tests/` → Unit test logic for all subtasks  
- `instructions.txt` → Setup and execution guide  

---

## Requirements

- Google Colab Pro
- Gemini API Key

---

## Setup Instructions

1. Open `Benchmark_for_Gemini.ipynb` in Google Colab

2. Add your Gemini API key:
   - Go to **Secrets (🔑 icon)** in the sidebar
   - Create a new secret
   - Paste your API key
   - Enable *Notebook access*

3. Update the key reference in the notebook:

```python
GEMINI_API_KEY = userdata.get('YOUR_KEY_NAME')