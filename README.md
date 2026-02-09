# Job Transition Analytics Demo

Which projects will deliver on time?

**Stakeholder:** PMO Lead

## Key Insights

- Scope changes above 4 per sprint correlate with late delivery.
- Teams above 85% load miss deadlines 22% more often.
- Velocity above 30 story points improves on-time delivery modestly.

## Dataset

Primary file: `data/project_delivery.csv`  
Target variable: `on_time`

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook notebooks/analysis.ipynb
```


## Next Steps

**Done.** Class-weight tuning and SHAP explainability are implemented — see ### Implemented below.

---
*Analytics portfolio project — 2025-09*

<!-- build 6 -->

### Implemented

```bash
pip install -r requirements.txt
python src/train.py && python src/explain.py
```