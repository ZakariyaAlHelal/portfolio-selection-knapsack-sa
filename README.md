# Strategic Selection of a Technology Project Portfolio as a Multi-Dimensional Knapsack Problem with Structured Balance Penalties

This repository provides a reproducible implementation of the optimization framework presented in the associated research papers, including the full journal version and a preliminary conference version.
---

## Overview

This repository provides a reproducible implementation of a heuristic optimization framework for project portfolio selection under resource constraints and structural balance requirements.

The proposed approach formulates the problem as a **multi-dimensional knapsack model with structured balance penalties**, integrating:

* Project prioritization
* Complementary value
* Future capability contributions
* Balance across time horizons
* Balance across strategic intent categories

---

## Model

The portfolio selection problem is formulated as:

F(x) = V(x) − λ₁ P_time(x) − λ₂ P_intent(x)

subject to:

* Budget constraints
* Staff-hour constraints
* Binary project selection decisions

This formulation extends the classical knapsack problem by explicitly incorporating **portfolio structure control**.

---

## Methods

The following solution approaches are implemented:

* Greedy baseline
* Simulated Annealing (SA)
* Adaptive Simulated Annealing (ASA)

The heuristic search includes:

* Flip moves (add/remove projects)
* Swap moves (exchange projects)
* Feasibility repair mechanisms

---

## Reproducibility

To reproduce results:

```bash
pip install -r requirements.txt
python experiments/run.py
```

Alternatively, the full implementation and experimental workflow can be accessed via the notebook:

[portfolio_knapsack_sa.ipynb](notebooks/portfolio_knapsack_sa.ipynb)

This will:

* Generate synthetic portfolio instances
* Run all algorithms
* Produce results and figures within the notebook

---

## Results (Summary)

The computational experiments show:

* Simulated Annealing consistently achieves the highest objective value
* Adaptive SA performs similarly to the greedy baseline
* The formulation is robust across different parameter settings
---
## Figures

Visualizations generated from the experimental results are available in `docs/figures/`, including:

- Algorithm performance comparison  
- Convergence behavior  
- Resource balance and stability  
- Objective distribution  
- Runtime scaling  
- Trade-off between time and intent deviations  
---
## Tables

Tables used in the paper are available in `docs/tables/`.
---
## Repository Structure

experiments/ → experiment entry point
notebooks/ → full implementation and results

---

## Related Work

This repository is associated with the following research outputs:

- **Journal paper (full version)** — complete formulation, structured balance penalties, and sensitivity analysis  
- **Conference paper** — a preliminary version focusing on the simulated annealing–based solution approach  

Both works are based on the same core implementation provided in this repository.

---
## Citation

If you use this repository, please cite the corresponding work:

Al-Helal, Z. S.,  
"Strategic Selection of a Technology Project Portfolio as a Multi-Dimensional Knapsack Problem with Structured Balance Penalties."
