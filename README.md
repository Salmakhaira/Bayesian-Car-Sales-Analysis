# Bayesian-Car-Sales-Analysis

This project involves Bayesian modeling to analyze car sales data using various car features such as price, engine size, horsepower, and fuel efficiency. The analysis was conducted using JAGS and R to perform Bayesian linear regression, along with model comparison and diagnostic techniques.

## Project Overview
The objective of this project is to:
- Build Bayesian linear regression models to predict car sales.
- Implement model diagnostics to assess convergence and model fit.
- Compare models using WAIC and DIC.
- Validate the model through Posterior Predictive Checks (PPD).

## Dataset
The dataset used for this project includes various features of car sales, such as:
- Sales_in_thousands: Number of cars sold in thousands.
- Price_in_thousands: The price of the car model.
- Engine_size: Engine size of the car.
- Horsepower: Power output of the car.
- Fuel_efficiency: Car's fuel efficiency in miles per gallon.

## Bayesian Model Formulation
A Bayesian linear regression model was used with the following formulation:
### Likelihood:
𝑌𝑖∼𝑁(𝛽0 + 𝛽1 ⋅ price𝑖 + 𝛽2 ⋅ engine_size𝑖 + 𝛽3 ⋅ horsepower𝑖 + 𝛽4 ⋅ fuel_efficiency𝑖,𝜎2)

### Priors:
- 𝛽𝑗 ∼ 𝑁(0,0.001) for 𝑗 =0,1,2,3,4
- 𝜎2 ∼ Inverse-Gamma(0.1,0.1)

## Key Steps
1. Data Cleaning and Preparation: The dataset was cleaned by removing missing values and selecting relevant features for analysis.
2. Model Implementation: Bayesian regression was implemented using JAGS to perform MCMC sampling.
3. Model Diagnostics:
- Convergence was checked using trace plots and the Gelman-Rubin diagnostic (R-hat).
- Posterior Predictive Checks (PPD) were used to validate the model's predictive power.
4. Model Comparison: WAIC and DIC were computed to compare model performance.

## Results
- Convergence: The models showed good convergence based on trace plots and R-hat values.
- Model Fit: The posterior predictive checks showed that the model reasonably fits the observed data.
- Comparison: The model's WAIC and DIC values indicated a well-performing model, although future improvements could involve exploring other features or non-linear relationships.

## Conclusion
This project demonstrates the power of Bayesian linear regression in analyzing car sales data. It showcases important techniques such as model diagnostics, posterior predictive checks, and model comparison to ensure robust results.
