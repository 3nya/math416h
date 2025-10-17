---
id: linalg systems of linear equations
aliases: []
date: 2025-08-25
---
# linalg systems of linear equations
tags: #linalg

---

if we have a system of linear equations...
- *solution* : (c1, ..., cn) is a list of values that satisfies each equation
- *solution space* : set of all possible solutions
- two linear systems are *equivalent* if they have the same solution space

more formally, given equations:
- solution is a set of coefficients that satisfies
- $\sum_{j=1}^n a_{ij} c_i = b_i \forall 1 <= i <= m$

theorem: these operations do not change the solution of the system
- replacement: replace an equation by sum of itself and another
- scaling: multiplying an equation by a non-zero constant
- interchange: change the order of two equations

- *augmented matrix*:
- ex. 2x + 3y = 4 and 3x + 4y = 5
- turns into ((2, 3, 4), (3, 4, 5))
- combine matrix of coefficients with column of constants
- coefficient matrix: matrix of a_i's

- *reduced row-echelon form* (rref)
- leftmost nonzero entry is 1 (if this is not true its just echelon form)
- leftmost nonzero entry of row is only nonzero entry in its column (same as above)
- each leading entry of a row is to the right of the leading entry of row above
- rows with all zeros are at the bottom
- perform row operations on augmented matrix

- any non-zero matrix can be reduced into more than onematrix in echelon form...
- theorem: rref is *unique* for each augmented matrix

- *pivot position* : position that corresponds to a leading 1 in rref
- *pivot column* : column of the matrix that contains a pivot position

- valid *row operations*
    - swap two rows
    - multiply row by non-zero scalar
    - multiply row by non-zero scalar and add to another row

- *row-equivalent* : can turn one matrix into the other using row operations
- row-equivalent matrices represent equivalent systems

- systems are *consistent* if it has at least one solution, otherwise
*inconsistent*
- columns with 1 in rref are *free* variables, otherwise *dependent*
- systems inconsistent iff column n+1 of rref is a pivot column

- suppose a system has n variables and rref has r pivot columns
- *unique solution* if r = n, else *infinitely many solutions* if r < n

aka:
    - last column is pivot? inconsistent
    - last column is not pivot, and no more non pivot columns? unique sol
    - last column is not pivot, and exists more non pivot columns? infinite sols

*theorem*: every system of linear equations as either:
- no solutions
- exactly one solution (unique)
- infinitely many solutions
- prove this in homework 2!

---
### references:
[[linalg]]
