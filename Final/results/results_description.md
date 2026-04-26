# Results Description

This folder contains the output files generated from the LLM-based HVAC diagnostic framework.  
The files are organized following the workflow of the project.

---

## 1. LLM Diagnostic Outputs

### `ahu_diagnostic_reports_baseline.json`
- Diagnostic reports generated using the **baseline prompt**
- Each entry corresponds to one timestamp
- Includes:
  - physics-based features
  - rule-based evaluation
  - LLM-generated report


### `ahu_diagnostic_reports_improved.json`
- Diagnostic reports generated using the **improved prompt**
- Same structure as baseline
- Differences:
  - More structured reasoning
  - Reduced hallucination
  - More actionable recommendations

---

## 2. Evaluation Results

### `baseline_eval.csv`
- Evaluation results for baseline outputs
- Includes:
  - Rule Consistency
  - Hallucination Score
  - Usefulness Score


### `improved_eval.csv`
- Evaluation results for improved outputs
- Same metrics as baseline


### `eval_comparison.csv`
- Direct comparison between baseline and improved results
- Used for performance comparison


### `eval_summary.csv`
- Aggregated results (average scores)
- Used for final analysis in the report

---

## 3. Workflow Order

The files follow this sequence:

1. LLM outputs  
   → `ahu_diagnostic_reports_baseline.json`  
   → `ahu_diagnostic_reports_improved.json`  

2. Evaluation  
   → `baseline_eval.csv`  
   → `improved_eval.csv`  

3. Comparison  
   → `eval_comparison.csv`  
   → `eval_summary.csv`  

---

## Notes

- Improved prompt is designed to reduce hallucination and improve interpretability
- All evaluation results are derived from the LLM outputs
