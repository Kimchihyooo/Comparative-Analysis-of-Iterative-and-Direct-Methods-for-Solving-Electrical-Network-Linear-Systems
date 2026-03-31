Comparative Analysis of Iterative and Direct Methods for Solving Electrical Network Linear
Systems

## Description
This project performs a comparative numerical analysis of different methods for solving linear systems of equations. Specifically, it calculates node voltages for a 5-node smart grid/circuit system based on a provided dataset of conductances and currents. The project builds a conductance matrix and applies both a direct solver and several iterative numerical methods to compare their convergence, number of iterations, and error margins.

## Methods Analyzed
The notebook implements and compares the following mathematical methods:
1. **Direct Solver**: Using `numpy.linalg.solve` as a baseline for the exact solution.
2. **Jacobi Method**: An iterative algorithm for determining the solutions of a strictly diagonally dominant system of linear equations.
3. **Gauss-Seidel Method**: An improved iterative method that uses the latest updated values for faster convergence.
4. **Successive Over-Relaxation (SOR)**: A variant of the Gauss-Seidel method that uses an extrapolation factor (omega) for even faster convergence.
5. **Conjugate Gradient (CG) Method**: An algorithm for the numerical solution of particular systems of linear equations, namely those whose matrix is symmetric and positive-definite.

## Dataset
The code expects a dataset named `smart_grid_dataset.csv` in the same directory. The CSV should contain the following columns:
- `Voltage`
- `Current`
- `Resistance`
- `From Node` (integer, 1 to 5)
- `To Node` (integer, 1 to 5)
- `Conductance`

*Note: The code assumes a 5-node system where Node 5 is used as the reference (ground) node.*

## Dependencies
To run the Jupyter Notebook, you need Python 3.x and the following libraries installed:
- `pandas` (for dataset manipulation)
- `numpy` (for matrix operations and numerical solvers)
- `matplotlib` (for data visualization)

You can install the dependencies using pip:
```bash
pip install pandas numpy matplotlib
