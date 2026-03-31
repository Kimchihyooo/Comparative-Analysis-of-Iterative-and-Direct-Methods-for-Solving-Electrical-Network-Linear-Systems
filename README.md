Comparative Analysis of Iterative and Direct Methods for Solving Electrical Network Linear Systems 

## Overview
This project investigates the performance of iterative numerical methods. Specifically the Jacobi Method, the Gauss-Seidel Method, and the Successive Over-Relaxation (SOR) Method in solving linear systems derived from electrical network models. Electrical networks are mathematically represented as systems of linear equations based on Kirchhoff's Current Law (KCL), with node voltages treated as the unknown variables. 

Because direct analytical solutions can become computationally expensive and memory-intensive for large-scale networks, this project evaluates iterative methods as efficient, scalable alternatives.

## Authors & Affiliation
**Institution:** Bulacan State University, College of Science, Mathematics Department   
**Course:** Numerical Analysis (MAT 403)  
**Authors (BSM CS 4B):**
* Carlos John D. De Jesus 
* Aldrin M. Custodio
* Wreigh Francoie DC. Flores 
* Josh Melvin DC. Lazaro 
* Jerry Z. Mariano 

## Methods Analyzed
The repository implements and compares the following mathematical methods:
1. **Direct Solver Method**: Computes the exact node voltages by solving the system $Ax=b$, serving as the baseline reference solution with zero error.
2. **Jacobi Method**: An iterative algorithm where all node voltages are updated simultaneously using values strictly from the previous iteration.
3. **Gauss-Seidel Method**: An improvement over Jacobi that updates node voltages in place, meaning newly computed values are immediately used within the same iteration.
4. **Successive Over-Relaxation (SOR)**: An extension of the Gauss-Seidel method that introduces a relaxation factor Ω to further accelerate the rate of convergence.

## Key Findings
Based on our experimental results on the 5-node circuit dataset, the iterative methods exhibited distinct differences in efficiency:
* **Jacobi Method**: Proved to be the least efficient, requiring **47 iterations** with an approximation error of $3.24 x 10^{-6}$.
* **Gauss-Seidel Method**: Significantly improved convergence, requiring only **26 iterations** with a lower error of $1.35 x 10^{-6}$.
* **SOR Method**: Demonstrated the most superior performance. By tuning the relaxation parameter to $Ω=1.25$, the algorithm converged in just **13 iterations** with an exceptional error margin of $1.11 x 10^{-7}$.

## Usage & Dependencies
To run the Jupyter Notebook (`ComparativeAnalysis.ipynb`) and replicate the paper's findings, you need Python 3.x and the following libraries installed:
- `pandas` (for dataset manipulation)
- `numpy` (for matrix operations and numerical solvers)
- `matplotlib` (for generating convergence and error comparison plots)

**Execution:**
1. Ensure your network dataset (containing conductances and currents) is in the root directory.
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook ComparativeAnalysis.ipynb
