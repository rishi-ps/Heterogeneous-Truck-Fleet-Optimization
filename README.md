# Heterogeneous Truck Fleet Optimization using MINLP (CPLEX) and Genetic Algorithm

This project tackles the **Heterogeneous Truck Fleet Optimization (HTFO)** problem, where a logistics manager must assign the right type of truck to deliver products from distribution centers to various **food and medical shops** under **capacity and time window constraints**.

We compare the performance of:
- A **Mixed Integer Non-Linear Programming (MINLP)** model using IBM CPLEX
- A custom **Genetic Algorithm (GA)** heuristic with Taguchi-based parameter tuning

## 🔍 Problem Overview
The aim is to **minimize total delivery cost**, considering:
- Hiring costs for trucks and drivers
- Fixed and variable costs per truck type
- Delivery time windows
- Shop-specific demands and truck load limits

Each truck starts and ends at a distribution center and may serve multiple shops, but each shop is served by only one truck type.


## 🧠 Methodologies Used

### 1. MINLP (CPLEX)
- Linearization of nonlinear constraints
- Implemented with Python using IBM DOcplex
- Solves for the global optimum with full constraint satisfaction

### 2. Genetic Algorithm
- Chromosome = Truck-shop assignment
- Fitness function = Cost + penalty for load/time violations
- Operators: Tournament selection, 1-point crossover, mutation
- Parameters tuned with **Taguchi L16 orthogonal array**

## 📊 Results
- Tested with 10+10 shops due to free CPLEX constraint limits
- **CPLEX** achieved optimal cost: 426219.00
- **GA** (best case): 447143.00 
- Deviation = 4.91%
- Taguchi tuning significantly improved GA performance

## 📚 Citation

This project is based on the research article:

> Dev Mishra and Rony Mitra (2024).  
> _Heterogeneous truck fleet optimization_.  
> **Sādhanā – Academy Proceedings in Engineering Sciences**, Indian Academy of Sciences.  
> DOI: [10.1007/s12046-024-02578-w](https://doi.org/10.1007/s12046-024-02578-w)








