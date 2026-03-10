# simulated-worlds

# <span style="color:red"> MULTIVARIATE REGIME-CONDITIONAL SIMULATOR
The goal is to create a pipeline that starts from real-world data, constructs a richly-engineered feature set, 
detects market regimes, and ultimately produces statistically realistic synthetic worlds
As a part of ML-based causal representation learning project in quantitative finance. 

## <span style="color:blue ">Part 1.1 — Data Collection & Feature Engineering:
    
    • builds the data foundation for the entire simulator project,
    • collects financial and macroeconomic data from multiple sources (Yahoo Finance, FRED, SF Fed sentiment),  
    • engineers a comprehensive 59-feature dataset, 
    • outputs a clean, temporally-correct data set ready for regime detection and simulation in Part 1.2. 

## <span style="color:blue ">Part 1.2 — Regime Simulation & Factor Scoring:
    
    • detects market regimes using a Gaussian Hidden Markov Model HMM (0-calm, 1-transition, 2-stress), 
    • vets and scores all candidate features using a multi-dimensional IC-based framework,     
    • selects a final set of 19 high-quality factors for use in the simulation and causal analysis pipeline downstream.   
    • outputs a robust factors set and 3×3 real-world regime transition matrix for use in simulating regime paths in Part 1.3

## <span style="color:blue ">Part 1.3 — Factor & Return Simulation | Simulated Worlds Library:
    
    • regime path simulation (Markov chain),
    • factor sampling per regime (Gaussian Copula),
    • empirical bounds enforcement (regime-conditional clipping), 
    • return generation (a structural β-model with AR(1) memory and GARCH-lite variance dynamics),
    • world library generator that seeds all of the above to create 50 (any number) independent synthetic worlds from the same model. 

## Statistical Validation:
<img width="892" height="346" alt="image" src="https://github.com/user-attachments/assets/63113586-cc7b-476d-8e8a-52a19c9583d4" />

## Simulated Worlds Library Statistics: 
<img width="899" height="321" alt="image" src="https://github.com/user-attachments/assets/0efaf4aa-3433-47c6-99f9-50026e2afd42" />

## Real World. Close Price and HMM Regime: 
![image.png](attachment:df433ad0-1bd0-4843-8950-36f42c75faa4.png)

## Simulated World. Close Price and HMM Regime: : 
![image.png](attachment:cf352d3b-fd90-4198-aa9d-f329ce53838b.png)

