**Overview**
This repository contains the full workflow and analysis code for evaluating the synergy effects of green-gray-blue (GGB) drainage systems under multiple scenarios.
The framework integrates Random Forest (RF), PySWMM (Python & Stormwater Management Model), multi-objective optimization, and robustness analysis to explore cost-effective and stormwater management strategies.

**Key Features**
1.Random Forest-based flood hazard classification.
2.Computation of Mean Importance, Standard Deviation, and CV.
3.NSGA-Ⅱ was applied to obtained the Pareto fronts of each scenarios.
4.Bootstrap repeated runs to quantify stability feature importance and Pareto fronts.

**Structures**
1.Random Forest: To assess the spatial distribution of stormwater hazard assessment using the RF model.
2.Stability of RF Model: Evaluates the stability and uncertainty of the RF model via repeated resampling and coefficient of variation (CV) analysis.
3.PySWMM: Simulates hydrological responses of green-gray-blue drainage systems using the PySWMM. Eight scenarios (S1-S8) are designed to represent varying spatial configurations and rainfall return periods.
4.Paretofrontbootstrap: Conducts multi-objective optimization with NSGA-II to minimize life-cycle cost (LCC), minimize inundation, and maximize runoff control under storage constraints. Bootstrap resampling is applied to the Pareto front solutions to evaluate robustness and uncertainty.

**Objectives**
1.Minimize life cycle cost.
2.Minimize flooding.
3.Maximize runoff control.

**Scenarios**
Eight rainfall scenarios (S1–S8) are generated based on spatial distribution of hazards across return periods ranging from 0.5 to 30-year.

**Workflow**
1.Hazard mapping
Using RF to classify stormwater hazard areas based on the importance of explanatory indicators.
2.Stability and uncertainty
Assessing RF performance robustness using multiple resampling and cross-validation tests.
3.Hydrological Simulation
Running PySWMM to simulate system performance for each GGB scenario (S1–S8).
4.Optimization & Robustness
Apply NSGA-II optimization to identify Pareto fronts, followed by Bootstrap analysis to quantify robustness under uncertainty.

**Environment Requirements**
1.Python ≥ 3.9.
2.Required libraries: numpy, pandas, matplotlib, scikit-learn, deap, pyswmm, tqdm, seaborn, scipy, plotly.

**How to Run**
1.Train the Random Forest model
2.Assess model stability
3.Run hydrological simulations
4.Perform NSGA-II optimization and Bootstrap analysis
