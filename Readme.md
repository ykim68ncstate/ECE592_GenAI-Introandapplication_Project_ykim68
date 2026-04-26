# Physics-Grounded Generative HVAC Diagnosis

This repository contains the implementation and results of an LLM-based HVAC diagnostic framework using BAS data.

The project is organized into **Final** and **Milestone** stages, along with a shared dataset.


This project develops an **LLM-based HVAC diagnostic framework** that automatically interprets building operational data from a Building Automation System (BAS).

---

## Project Objective

The goal of this project is to:
- Automatically interpret complex HVAC operational data
- Evaluate system efficiency using physics-based rules
- Generate structured diagnostic reports using a Large Language Model (LLM)

This helps building operators and researchers understand system performance without requiring deep HVAC expertise.

The final output is a structured diagnostic report including:
- operational summary  
- efficiency assessment  
- key issues  
- engineering interpretation  
- recommendations  

---

## What This System Does

Given HVAC time-series data, the system performs:

1. **Feature Engineering**  
   - Computes physics-based features (temperature differences, airflow, cooling load)

2. **Rule-Based Evaluation**  
   - Classifies system status (efficient / needs review / inefficient)

3. **LLM-Based Diagnosis**  
   Generates structured reports including:
   - Operational summary
   - Efficiency assessment
   - Key issues
   - Engineering interpretation
   - Recommendations

4. **Evaluation**  
   Measures performance using:
   - Rule Consistency
   - Hallucination Score
   - Usefulness Score
     
---

## LLM Usage

This project uses the OpenAI API for LLM-based report generation.

Set your API key before running the code:
```bash
export OPENAI_API_KEY="your_api_key_here"
or inside the notebook:
  ₩import os₩
  ₩os.environ["OPENAI_API_KEY"] = "your_api_key_here"₩

For convenience in this project (e.g., notebook execution), you may also directly input the API key in the code.
  
- Model: GPT-based LLM (via OpenAI API)
- Input: Structured HVAC features + rule evaluation results
- Output: JSON-based diagnostic report

The project compares:
- **Baseline prompt**
- **Improved prompt (constraint-based, physics-guided)**

to evaluate how prompt engineering affects reliability and usefulness.


---

## Dataset

### `Dataset.zip`
- Contains BAS (Building Automation System) data
- Time-series HVAC operational data
- Includes variables such as:
  - temperature (SA_T, MA_T, OA_T, RA_T)
  - airflow (CFM)
  - system operation conditions

---

## Final Project

### Report
- Final report (NeurIPS format)
- Includes methodology, results, and analysis

### `Final/ (code files)`
Includes:
- Data preprocessing
- Compute physics-based features  
- Apply rule-based evaluation 
- Generate LLM diagnostic reports (OpenAI API)
- Evaluation metrics (consistency, hallucination, usefulness)


### `Final/results/`
Contains model outputs and evaluation results:

- `ahu_diagnostic_reports_baseline.json`  
- `ahu_diagnostic_reports_improved.json`  
- `baseline_eval.csv`  
- `improved_eval.csv`  
- `eval_comparison.csv`  
- `eval_summary.csv`  


---

## Milestone

### `Report`
- Milestone report

### `Milestone/code/`
- Initial implementation and baseline experiments

