# App Feature A/B Test Analysis
## Nigerian Mobile-First Landing Page Experiment — Controlled Simulation

> **Portfolio project:** A/B testing, statistical inference, product analytics, and Nigerian-context experimentation.

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## Project Question

**Under Nigerian mobile-network conditions, does a lightweight, low-data landing page outperform a standard landing page on conversion and user experience?**

### Experimental variants
- **A — Standard:** conventional, heavier landing page.
- **B — Lightweight:** mobile-first page designed to reduce payload and data usage.

### KPIs
**Primary:** conversion rate

**Secondary:** page size, page-load time, data usage, bounce rate, CTA click-through rate.

## Important Methodology Disclosure

This is a **controlled experimental simulation**, not a live A/B test on real Nigerian customers.

The simulation is calibrated using published aggregate Nigerian telecom performance benchmarks. The individual user-level observations and outcomes in `nigerian_mobile_ab_simulation.csv` are simulated.

**Correct:** “I conducted a controlled experimental simulation calibrated to Nigerian telecom performance benchmarks.”

**Do not claim:** “I conducted an A/B test on 20,000 Nigerian users.”

A live randomized experiment would be required to validate the result with real customer behavior.

## Key Results

The supplied simulation contains **20,000 user-level observations**.

| Metric | A — Standard | B — Lightweight |
|---|---:|---:|
| Users | 9,931 | 10,069 |
| Conversion rate | 9.23% | 10.71% |
| Average page size | 2397 KB | 750 KB |
| Average page-load time | 2037 ms | 1355 ms |
| Average data usage | 2.62 MB | 0.82 MB |
| Bounce rate | 34.42% | 25.80% |
| CTA click rate | 20.89% | 24.22% |

### Primary experiment result

- **Absolute conversion uplift:** 1.47%
- **Relative conversion uplift:** 15.95%
- **One-sided two-proportion Z-test:** z = 3.474
- **p-value:** 0.000256
- **95% CI for B − A:** [0.64%, 2.30%]

Under the simulation assumptions, the lightweight variant shows statistically significant positive evidence on the primary KPI.

This is **simulation evidence supporting a live validation experiment**, not evidence from real Nigerian customers.

## Nigerian Context

A mobile-first product may need to account for variable network quality, network technology, latency, page weight, data affordability and loading performance. The experiment therefore treats performance as part of the product experience.

The notebook uses published Nigerian operator-level benchmark inputs for network context.

## Methodology

1. Approximately 20,000 simulated users are assigned 50/50 to A and B.
2. Operator assignment and network conditions are calibrated to published Nigerian benchmarks.
3. Page performance is modeled from page size and network conditions.
4. Engagement and conversion outcomes are simulated from explicit assumptions.
5. Conversion is evaluated with a one-sided two-proportion Z-test.
6. A 95% confidence interval is calculated for **B − A**.
7. Bootstrap inference, secondary KPI analysis, operator exploration and sensitivity analysis provide robustness and context.

## Repository Structure

```text
app-feature-ab-test-nigerian-mobile/
├── App_Feature_AB_Test_Nigerian_Mobile_Experiment.ipynb
├── nigerian_mobile_ab_simulation.csv
├── nigerian_mobile_ab_simulation_summary.csv
├── README.md
├── DEMO_VIDEO_SCRIPT.md
├── PUBLISH_TO_GITHUB.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook
```

Open `App_Feature_AB_Test_Nigerian_Mobile_Experiment.ipynb` and run all cells from top to bottom.

The notebook expects `nigerian_mobile_ab_simulation.csv` in the same directory.

## Skills Demonstrated

- Pandas and NumPy
- Data cleaning and validation
- Exploratory analysis
- KPI design
- A/B-test design
- Two-proportion hypothesis testing
- Confidence intervals
- Bootstrap inference
- Product analytics
- Visualization
- Business recommendation

## Limitations

1. User behavior is simulated.
2. Telecom benchmarks are aggregate measurements.
3. Results depend on simulation assumptions.
4. No production users were exposed to either variant.
5. The findings cannot be generalized to the Nigerian population.

## Recommended Next Experiment

Run the same experiment on a live mobile-first landing page with randomized visitors and capture:

```text
user_id
variant
timestamp
device
operator
network_type
page_size
page_load_time
data_usage
bounce
CTA_click
conversion
```

Then repeat the same statistical workflow using real observations.

## Source

Nigerian network benchmark context:

MedUX / SpeedChecker — Nigeria, October 2025 network observatory report:

https://observatory.medux.com/africa/nigeria/ng-october-2025/

The benchmark source is used for contextual calibration only. The user-level experiment remains simulated.

## Portfolio Positioning

This project demonstrates an end-to-end analytical workflow:

**business problem → experimental design → data validation → KPI analysis → statistical inference → uncertainty → product-performance analysis → business recommendation.**

## Author

**Onyedikachi Onwuka**

Data Science / Data Analytics Portfolio

GitHub: https://github.com/justdsky4u
