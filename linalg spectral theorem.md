---
id: linalg spectral theorem
aliases: []
date: 2025-10-16
---
# linalg spectral theorem
tags: 

---

## background knowledge

- diagonal matrix is 0 everywhere except the diagonal
- operator T is diagonalizable if it has a diagonal basis w.r.t. some basis of V
- this happen iff there exists a basis of V consisting of eigenvectors of T

- nicest operators have a diagonal matrix w.r.t. an *orthonormal* basis of V
- *spectral theorem*
    - these are the self-adjoint operators when F=R
    - these are the normal operators when F=C


## real spectral theorem

- suppose F=R, T in L(V)
- the following are equivalent:
    - $T$ is self-adjoint
    - $T$ has a diagonal matrix w.r.t. some orthonomal basis of $V$
    - $V$ has an orthonormal basis consisting of eigenvectors of $T$


## complex spectral theorem

- suppose F=C, T in L(V)
- the following are equivalent:
    - $T$ is normal
    - $T$ has a diagonal matrix w.r.t. some orthonomal basis of $V$
    - $V$ has an orthonormal basis consisting of eigenvectors of $T$

---
### references:
[[linalg]]
