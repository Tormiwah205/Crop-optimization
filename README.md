# Optimization of Crop Land Allocation under Resource Constraints

This project reproduces and extends a crop land allocation model initially implemented in GAMS during Risk Management course at UM6P, Morocco (ABI) using Python. The goal is to maximize expected gross margin from multiple crops under limited land, water, budget, and rotation constraints using statistical modeling and linear programming.

# Objectives
Simulate crop gross margin data using historical rainfall and noise.
Fit regression models to estimate gross margin per hectare (GPha) for each crop.
Use Monte Carlo simulation to account for uncertainty in yield predictions.
Solve an optimization problem to allocate land among crops for maximum profit.
Visualize optimal allocation and contribution of each crop to the total gross margin.


# Datasets (Simulated)
Rainfall Data: Normally distributed synthetic rainfall for 10 years.
Gross Product (GPha): Simulated using a linear model with crop-specific slope and intercept, plus random noise.
Variable Costs & Water Requirements: Based on estimates for each crop (class).


# Statistical Models
Linear Regression (OLS) is used to model the relationship between rainfall and gross product per hectare (GPha).
Standard Error of Prediction is calculated to simulate uncertainty.
Monte Carlo Simulation (1000 iterations) is used to generate a distribution of future GPha values per crop.


# Optimization Model
The objective is to maximize total expected gross margin using:
Linear Programming
Subject to the following constraints:

Land constraint (≤ 22 hectares)
Budget constraint (≤ 52,000 MAD-Morocco dirhams)
Water availability constraint (≤ 110,000 m³)
Rotation constraint (Maize + Cowpea ≤ Rice + Cassava + Spinach)


# Visualizations
Bar plot showing hectares allocated per crop.
Bar plot of each crop's contribution to the total expected margin.
Histograms for each crop showing the uncertainty in predicted GPha.
