---
id: linalg operators on inner product spaces
aliases: []
date: 2025-10-15
---
# linalg operators on inner product spaces
tags: 

---

## adjoints

- the *adjoint* of a linear map $T \in L(V, W)$, is the map $T^* : W -> V$
- such that $<Tv, w> = <v, T^* w>$ for all $v, w$.

- adjoint of a linear map is always a linear map


### properties of the adjoint

- let $T \in L(V, W)$,
- then we have:

- $(S + T)^* = S^* + T^*$
- $(\lambda T)^* = \bar{\lambda} T^*$
- $(T^*)^* = T$
- $(ST)^* = T^* S^*$
- $I^* = I$
- if $T$ invertible, then $T^*$ is invertible and $(T^*)^{-1} =(T^{-1})^*$


### null space and range of adjoint

- $null T^* = (range T)^\perp$
- $range T^* = (null T)^\perp$
- $null T = (range T^*)^\perp$
- $range T = (null T^*)^\perp$


### conjugate transpose

- the *conjugate transpose* $A^*$ of a matrix is defined as
- $(A^*)_{j, k} = \bar{A_{k, j}}$

- matrix of $T^*$ is the conjugate transpose of matrix of $T$,
- with respect to *orthonormal bases*
- this result does not hold if the bases are not orthonormal !!!


## self-adjoint operators

- an operator is *self-adjoint* if $T = T^*$

- helpful analogy is adjoint plays a similar role as the complex conjugate
- self-adjoint operators are similar to real numbers

- every eigenvalue of a self-adjoint operator is real

- *assuming F = C*, Tv is orthogonal to v for all v iff T = 0
- *assuming F = C*, <Tv, v> is real for all v iff T is self-adjoint

- *for F = C or R*, T = 0 iff T is self-adjoint and <Tv, v> = 0


## normal operators

- an operator is *normal* if it commutes with its adjoint
- aka. $T T^* = T^* T$

- every *self-adjoint* operator is *normal*

- T is normal iff $||Tv|| = ||T^* v||$ for all v


### properties or normal operators

- suppose $T \in L(V)$ is normal, then
- $null T = null T^*$
- $range T = range T^*$
- $V = null T \oplus range T$ 
- $T - \lambda I$ is normal for every $\lambda \in F$
- $Tv = \lambda V$ iff $T^* v = \bar\lambda v$

- eigenvectors of T corresponding to distinct eigenvalues are orthogonal

- T is normal iff real and imaginary parts of T commute
    - T = A + iB, where A and B are commuting self-adjoint operators

---
### references:
[[linalg]]
