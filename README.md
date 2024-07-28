# Optimization Algorithms

## Overview

This project involves exploring optimization algorithms, particularly hill-climbing and genetic algorithms, to solve optimization problems. The assignment includes implementing and improving these algorithms to find global optima on complex error surfaces.

## Project Structure

1. **Hill Climbing in Python**: Implementation of a hill-climbing algorithm to minimize an error function.
2. **Algorithm Enhancement**: Modifying the hill-climbing algorithm to include random restarts, improving its ability to find global optima.
3. **Genetic Algorithm**: Developing a genetic algorithm as an alternative approach to solve the optimization problem.
4. **Testing and Visualization**: Evaluating the algorithms using different error landscapes and visualizing the results.

## Explanation

### Define the optimization problem that this algorithm is trying to solve: What is the objective function? What are the decision variables? Are there any constraints?
Objective: This algorithm aims to minimize the error function (find the global minimum).
Objective Value: The value calculated by the error(a, b) function. This will be how we will measure the calculation of the error and compare it with the other values received after.

Decision Variables: We have a and b as decision variables. These are the coordinates on the error surface that the algorithm adjusts to find the lowest error value. They are changed each iteration to minimize our objective function.

Constraints: There is no well-defined constraint for the decision variables, as they can be of any value and do not have certain limitations or problems that might arise from them. We only have limitations and necessities to make the algorithm work, such as the maximum number of iterations and the necessity of each step resulting in a lower error to be accepted (if not, the algorithm will terminate abruptly).

### Inputs, outputs, key steps, and the termination condition.
The algorithm is designed to minimize the error function defined by error(a, b). The hill-climbing algorithm iteratively adjusts the decision variables to find the minimum value of the error function.

Inputs: a and b (starting points), step size (stepsize), number of iterations (max_steps).
Outputs: Final a value and b value as a coordinate, corresponding error value at that point.

Key Steps:
- Initial values of a and b, evaluating the error.
- Tentatively moves in each direction by stepsize and assess the error at these new points.
- Updates a and b to the new point, resulting in the lowest error among the options.
- Iterate until no step results in a lower error or reaches the maximum number of steps.

Termination Condition: When a step does not decrease the error or when it reaches the maximum number of iterations set.

Advantage: Simple to implement and quick for finding local minima/maxima in smooth error surfaces.
Limitation: Cannot guarantee to find the global minima due to potential local minima.

### Testing the algorithm
To test the modified hill-climbing algorithm, I conducted multiple runs with random restarts to evaluate its performance across different starting conditions. This approach is effective because it mitigates the risk of the algorithm getting trapped in local optima. By starting from different points in the search space, the algorithm has a better chance of discovering the global optimum. I also changed the error function with a different landscape. This was supposed to challenge the optimization process with different settings, slopes, and multiple peaks, which could potentially trap the algorithm in local optima. The algorithm was still successful, demonstrating that the modification indeed improved the algorithm.

## Developing a different algorithm
I used genetic algorithms (GA) because they solve optimization problems characterized by complex error surfaces. The GA method effectively handles scenarios with many local optima and large search spaces. The process begins by generating a population of potential solutions, each represented by a pair of a and b values. These individuals are evaluated for fitness using an error function, where a lower error signifies a better solution. A subset of the population, selected based on fitness, produces the next generation through crossover, combining parts of each parent's values to create better solutions. Random mutations in some offspring introduce variability, preventing premature convergence to local optima. This iterative process continues for a set number of generations, aiming to evolve the population toward better solutions.
Testing involved running the algorithm with identical parameters to ensure stability and varying key parameters like population size, number of generations, and mutation rate to assess performance under different conditions.

## Files

- `Optimization Algorithms.ipynb`: The Jupyter Notebook containing the hill-climbing and genetic algorithm implementations, along with testing and visualizations.
- `README.md`: This README file.

## Instructions

1. **Run the Jupyter Notebook**: Open `Optimization Algorithms.ipynb` in Jupyter Notebook to explore the implementations.
2. **Test the Algorithms**: Modify the starting points, step sizes, and other parameters to see how the algorithms perform on different error surfaces.
3. **Visualization**: Use the provided plotting functions to visualize the optimization process and the resulting paths.

## Contact

For any questions or further information, please contact pedro@uni.minerva.edu.
