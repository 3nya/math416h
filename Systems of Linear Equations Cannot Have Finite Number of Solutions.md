- One solution
- Or infinitely many

We can prove this using **contradiction**!

Assume that there are finite number of solutions $m$, such that $1 < m < \infty$. 

Because there are at least 2 solutions,

let $x_1$ and $x_2$ be 2 different solutions to the linear system $Ax = b$. st $x_1 \neq x_2$.

We know that 

$Ax_1 = b$ and $Ax_2 = b$

$b = Ax_1 = Ax_2$

Let $\alpha \in \mathbb{R}$

We can write an arbitrary solution $x$ such that  $x = \alpha x_1 + (1 - \alpha ) x_2$.

Putting this in our linear system $Ax = b$, we get that 
$Ax = A(\alpha x_1 + (1 - \alpha ) x_2)$
$=A\alpha x_1 + Ax_2 - A\alpha x_2$
$=\alpha b + b - \alpha b$
$= b$

$x$ is also a solution to this system.

Because $\alpha \in \mathbb{R}$, there are infinite possibilities of what $x$ can be $\implies$ there are infinite solutions. 


