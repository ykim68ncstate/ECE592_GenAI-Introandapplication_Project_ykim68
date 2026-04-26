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


## What This System Does

This system takes HVAC time-series data as input and performs:

1. Physics-based feature computation  
2. Rule-based system evaluation  
3. LLM-based diagnostic report generation  
4. Performance evaluation of LLM outputs  

The final output is a **structured engineering report** that explains:
- Current system status
- Detected issues
- Physical interpretation
- Actionable recommendations  

---

## LLM Usage

This project uses the **OpenAI API** to generate diagnostic reports.

- Model: GPT-based LLM (via OpenAI API)
- Input: Structured HVAC features + rule evaluation results
- Output: JSON-based diagnostic report

The project compares:
- **Baseline prompt**
- **Improved prompt (constraint-based, physics-guided)**

to evaluate how prompt engineering affects reliability and usefulness.


---

## Repository Structure
├── Dataset/
├── Final/
│ ├── report/
│ ├── results/
│ └── (code files)
├── Milestone/
│ ├── report/
│ ├── code/


## Dataset

### `Dataset.zip`
- Shared dataset for milestone and final stages
- BAS (Building Automation System) data
- Includes HVAC time-series variables (temperature, airflow, etc.)

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

