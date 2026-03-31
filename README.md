# [cite_start]Comparative Analysis of Iterative and Direct Methods for Solving Electrical Network Linear Systems [cite: 6, 7]

## 📖 Overview
[cite_start]This project investigates the performance of iterative numerical methods—specifically the Jacobi Method, the Gauss-Seidel Method, and the Successive Over-Relaxation (SOR) Method—in solving linear systems derived from electrical network models[cite: 24]. [cite_start]Electrical networks are mathematically represented as systems of linear equations based on Kirchhoff's Current Law (KCL), with node voltages treated as the unknown variables[cite: 25, 96, 107]. 

[cite_start]Because direct analytical solutions can become computationally expensive and memory-intensive for large-scale networks, this project evaluates iterative methods as efficient, scalable alternatives[cite: 49, 374, 382].

## Authors & Affiliation
[cite_start]**Institution:** Bulacan State University, College of Science, Mathematics Department [cite: 3, 10, 11]  
[cite_start]**Course:** Numerical Analysis (MAT 403) [cite: 14]  
[cite_start]**Authors (BSM CS 4B):** [cite: 16]
* [cite_start]Carlos John D. De Jesus [cite: 18]
* [cite_start]Aldrin M. CustodiΟ [cite: 18]
* Wreigh Francoie DC. [cite_start]Flores [cite: 19]
* Josh Melvin DC. [cite_start]Lazaro [cite: 20]
* [cite_start]Jerry Z. Mariano [cite: 21]

## Methods Analyzed
The repository implements and compares the following mathematical methods:
1. [cite_start]**Direct Solver Method**: Computes the exact node voltages by solving the system $Ax=b$, serving as the baseline reference solution with zero error[cite: 151, 152, 322].
2. [cite_start]**Jacobi Method**: An iterative algorithm where all node voltages are updated simultaneously using values strictly from the previous iteration[cite: 232].
3. [cite_start]**Gauss-Seidel Method**: An improvement over Jacobi that updates node voltages in place, meaning newly computed values are immediately used within the same iteration[cite: 131, 278].
4. [cite_start]**Successive Over-Relaxation (SOR)**: An extension of the Gauss-Seidel method that introduces a relaxation factor ($\omega$) to further accelerate the rate of convergence[cite: 116, 117].

## Key Findings
Based on our experimental results on the 5-node circuit dataset, the iterative methods exhibited distinct differences in efficiency:
* [cite_start]**Jacobi Method**: Proved to be the least efficient, requiring **47 iterations** with an approximation error of $3.24 \times 10^{-6}$[cite: 376, 377].
* [cite_start]**Gauss-Seidel Method**: Significantly improved convergence, requiring only **26 iterations** with a lower error of $1.35 \times 10^{-6}$[cite: 378].
* **SOR Method**: Demonstrated the most superior performance. [cite_start]By tuning the relaxation parameter to $\omega=1.25$, the algorithm converged in just **13 iterations** with an exceptional error margin of $1.11 \times 10^{-7}$[cite: 379, 381].

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
