# Linear-Algebra-Project

Project assignment for "Linear Algebra"

When your notebook is ready, please check it into your Github repository.  To "hand in" your notebook, you can send the URL of your Github repository.

Due: Monday, January 30, end of day

1. As demonstrated in the lecture, approximate fstar(x) = sin(x) on the interval [0, pi/2] via polynomials using a least squares approach. Use 1,000 evaluation points. Create a repository on Github holding your code. This repository needs to have a README explaining (in brief) the algorithm, as well as instructions for using your code to reproduce the results. These instructions should also include figures since a picture is worth a thousand words. Your code should be able to show results for all tasks in this project, and your code should be well-written and understandable. Use comments.

2. Define the approximation error E as the L2 norm of the difference between the approximation function f(x) and fstar(x). This is also called RMS or "root mean square" of the difference: The square root of the average of (f(x) - fstar(x))^2 at all evaluation points. What polynomial order (pmax) is required to satisfy E < 1.0e-10? Plot the
relation between pmax and E for pmax from 0 to at least 20. Discuss the figure. Can you achieve E < 1.0e-20? Say why.

3. The function sin(x) is antisymmetric, i.e. sin(x) = - sin(-x). Modify the method to use only antisymmetric polynomials in your approximation. How does this affect the error? Compare results for the same computational cost, i.e. for the same number of polynomials used (not for the same pmax).

4.a. Calculate (manually, not numerically) the derivative of the approximating function f(c, x) = \sum_p c_p x^p. Define a new function g(d, x) = \sum_p d_p x^p which depends on a different set of coefficients |d>. Set g(d, x) = f'(c, x), and solve for the coefficients |d> as a function of the coefficients |c>. Since the derivative is a linear operation, the relation between |d> and |c> can be expressed via a linear operator, the derivative matrix D: |d> = D|c>. Calculate D.

4.b. Calculate D numerically, and test your code by comparing (1) approximating sin(x) and calculating the derivative via D, and (2) approximating sin'(x) = cos(x). (Note that cos(x) cannot be approximated well by antisymmetric polynomials, i.e. don't use your code from task 3 above.)
