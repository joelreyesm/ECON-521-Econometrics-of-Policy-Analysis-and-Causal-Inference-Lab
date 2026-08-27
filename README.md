# ECON 521: Econometrics of Policy Analysis and Causal Inference — Lab

This repository contains the **lab (discussion section) materials** for **ECON 521: Econometrics of Policy Analysis and Causal Inference**. The lab complements the Thursday lecture with hands-on simulation, replication, and estimation exercises in modern causal inference and policy evaluation, using real-world and simulated data.

### Lab logistics (Fall 2026)

- **Meets:** Friday 1:00–1:50 PM, White Hall 102 (the day after Thursday lecture)
- **First lab:** Friday, August 28, 2026
- **Weight:** The lab is **25% of the course grade**. See **Lab Grading** below for the breakdown.

## Course Overview

The course covers advanced econometric techniques used in policy analysis and causal inference. The lab puts each of these methods into practice:

- **Potential Outcomes Framework** — Fundamental concepts of causal inference
- **Randomized Controlled Trials** — Design and analysis of experimental data, variance reduction (Lin 2013, CUPED), and multiple/double randomization
- **Power Analysis** — Monte Carlo and power simulations
- **Instrumental Variables** — Endogeneity, selection bias, and the behavior of IV under weak instruments
- **Regression Discontinuity Design** — Exploiting policy thresholds for identification, and bandwidth selection as a bias–variance trade-off
- **Difference-in-Differences and Event Studies** — Panel data methods for policy evaluation, including modern estimators
- **Synthetic Control Methods** — Constructing counterfactuals for policy analysis
- **Matching and Interrupted Time Series** — Subclassification, matching estimators, and ITS designs
- **Machine Learning for Causal Inference** — Double/debiased ML and heterogeneous treatment effects

## Lab Schedule

Eleven lab sessions are planned. Dates below refer to the **Thursday lecture**; each lab meets the **following Friday**.

| Lecture | Lab topic | Description |
|---|---|---|
| Aug 27 | Selection bias | Treatment effects from observational data with selection bias, benchmarked against experimental data |
| Sep 3 | Regression adjustment and CUPED | Saturated regression (Lin 2013), then CUPED |
| Sep 10 | Multiple randomized designs | Randomizing only viewers, or only content creators, against double randomization |
| Sep 17 | Power analysis | Monte Carlo simulations and power simulations |
| Sep 24 | IV simulations | Properties of the IV estimator |
| Oct 1 | Weak IV simulation | Behavior of the IV estimator when instruments are weak |
| Oct 8 | RDD simulation | Regression discontinuity in practice |
| Oct 22 | RDD bandwidth selection | Discontinuity estimates over progressively narrower bandwidths |
| Oct 29 | DiD and event study simulation | `pyfixest`; `csdid` |
| Nov 12 | Matching and ITS simulation | Subclassification / matching estimators; interrupted time series |

## Lab Grading

The lab is **25% of the course grade**, scored out of **25 points** (1 lab point = 1% of the course grade). The scheme rewards consistent attendance and hands-on practice rather than exam-style performance.

| Component | Points | How it works |
|---|---|---|
| Attendance & in-lab work | 11 | 13 sessions, 1 point each, **capped at 11** |
| Biweekly assignments | 14 | 7 assignments × 2 points each |
| **Total** | **25** | |

### Attendance & in-lab work — 11 points

- There are 13 lab sessions. Each session is worth 1 point, and the total is **capped at 11**, so you may miss up to two sessions with no penalty.
- Attending fewer than 11 sessions costs 1 point for each session below 11. **Attendance at 11 sessions is the minimum expectation for the lab.**
- **Excused absences** (documented illness, family emergency, religious observance, university-sanctioned travel) do not count against the 11. 

### Biweekly assignments — 14 points

- **7 assignments**, released roughly every two weeks, **2 points each**. All 7 count toward the grade.
- Each assignment applies the method from the preceding one or two labs: a short simulation or replication with a few sentences of interpretation. They are meant to be completed in a few hours, not to be term papers.
- Each assignment is graded on a simple rubric — **code reproduces / runs (40%), correct estimates and answers (40%), interpretation (20%)**.
- Collaboration on approach is allowed; every student submits their own code and write-up.
- **No late work is accepted.** A missed assignment receives 0. Because the assignments are low-stakes (2 points each) and frequent, a single missed assignment has a limited effect on the overall grade; the flexibility for illness or travel is built into the attendance cap.

## Repository Structure

```
├── labs/          # Notebooks / scripts for each lab session
├── slides/        # Lab slides and handouts
├── data/          # Datasets used in lab exercises
├── assignments/   # Problem sets tied to the lab methods
└── utils/         # Helper functions and shared utilities
```

This layout grows over the term; not every directory is populated at the start of the semester.

## Getting Started

### Prerequisites

- Basic knowledge of econometrics and statistics
- Comfort with a scripting language for data analysis

### Language

Lab exercises are provided primarily in **Python** (`pandas`, `numpy`, `statsmodels`, `pyfixest`), which matches the lecture notebooks. Several exercises are adapted from Stata originals, and equivalents in **Stata** or **R** are provided where useful. Use whichever environment you are most comfortable with unless an exercise says otherwise.

### Installation (Python)

1. Clone this repository:
```bash
git clone https://github.com/[username]/econ521-causal-inference-lab.git
cd econ521-causal-inference-lab
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Lab:
```bash
jupyter lab
```

## Key Topics Covered

### 1. Foundations of Causal Inference
- Potential outcomes and the fundamental problem of causal inference
- Selection bias and confounding
- Randomized experiments as the benchmark, and variance reduction

### 2. Quasi-Experimental Methods
- **Instrumental Variables**: external variation, endogeneity, and weak-instrument behavior
- **Regression Discontinuity**: cutoffs in treatment assignment and bandwidth selection
- **Difference-in-Differences**: changes over time between treatment and control groups, modern estimators

### 3. Panel Data and Design-Based Methods
- Fixed effects and event study designs
- Synthetic control methods
- Matching, subclassification, and interrupted time series

### 4. Machine Learning for Causal Inference
- Double/debiased machine learning
- Heterogeneous treatment effects

## Acknowledgments

This lab is built on the work of the instructors who developed and taught these materials before me. Much of the structure, the notebooks, and the slides in this repository are inherited from their work, and this README itself is adapted from the previous ECON 521 lab README.

- **Pablo Estrada** — original author of the Advanced Causal Machine Learning materials ([`causalml-advanced`](https://github.com/pabloestradac/causalml-advanced)) from which the lab notebooks derive. [pabloestrada.io](https://www.pabloestrada.io/#about)
- **Justin Eloriaga** — adapted Pablo's materials into the ECON 521 course and lab and taught the previous iteration. The prior lab repository — its notebooks (selection bias, CUPED, power, IV, RDD, DiD and event study) and slides — is the foundation of this one. [justineloriaga.com](https://www.justineloriaga.com)

I am grateful to these previous lab instructors and teaching assistants; any errors introduced in adapting or extending their materials are my own.

**Maintained for Fall 2026 by:** Joel Reyes (lab instructor)

## Resources

### Textbooks
- Angrist, J. D., & Pischke, J. S. (2009). *Mostly Harmless Econometrics*
- Cunningham, S. (2021). *Causal Inference: The Mixtape*
- Huntington-Klein, N. (2021). *The Effect: An Introduction to Research Design and Causality*
- Imbens, G. W., & Rubin, D. B. (2015). *Causal Inference for Statistics, Social, and Biomedical Sciences*

### Software
- **Python**: `pandas`, `numpy`, `scipy`, `statsmodels`, `scikit-learn`, `pyfixest`
- **R**: `AER`, `fixest`, `rdrobust`, `did`, `gsynth`
- **Stata**: community-contributed packages (`ivreg2`, `esttab`, `csdid`, `rdrobust`)

## Contributing

If you find errors or have suggestions for improvements:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## License

These materials are provided for educational use as part of ECON 521. Portions derive from upstream sources (see **Acknowledgments**) and remain subject to their original licensing. Please cite appropriately when reusing these materials in your own work.

## Contact

For questions about the lab materials:
- Open an issue in this repository
- Contact the lab instructor during office hours
- Post on the course discussion forum

---

*This repository is for educational purposes as part of ECON 521.*
