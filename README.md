# Nonlinear_optimisation
Optimisation methods for nonlinear Rosenbrock function

The notebook in this repo contains functions to minimise the Rosenbrock function:

$f(x,y) = (a-x)^2 + b(y-x^2)^$

Where $a = 1$, $b=100$

**Models implemented**

- Grandient descent 
- Gradient descent with momentum
- Nesterov's gradient descent 
- Nonlinear Conjugate Gradients with Newton-Raphson and Fletcher-Reeves

**Parameter analysis**

- For gradient descent, momentum and nesterov's a learning rate larger than approximately 0.00015 causes divergence. 
- Fixing this learning rate for the three above algorithms gradient descent coverges the slowest in 62,288 iterations.
- Momentum and nesterov's are much faster, best convergence found with momentum is 16,878. Both are highly sensitive to values for beta.
- CG coverges after only 19 iterations but in terms of clock time only slightly faster than momentum due to higher time complexity with each step. With a more complex non-linear function, and starting further from the optimum, this method could fail. 

