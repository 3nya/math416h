---
id: linalg inner product spaces
aliases: []
date: 2025-07-01
---
# linalg inner product spaces
tags: #linalg

---

## inner products and norms

- *inner product* aims to generalize dot product to all vector spaces
- is a function that takes each ordered pair of vectors (u, v) in V^2
- to a value in F

- satisfies the following 5 properties:
    - *positivity* : <v, v> >= 0 for all v in V
    - *definiteness* : <v, v> = 0 iff v = 0
    - *additivity in first slot* : <u + v, w> = <u, w> + <v, w>
    - *homogeneity in first slot* : <lambda u, v> = lambda <u, v>
    - *conjugate symmetry* : <u, v> = conjugate of <v, u>

- *inner product space*
    - vector space V with an inner product on V

- *euclidean inner product*
    - <(w1, ..., wn), (z1, ..., zn)> = w1 \bar{z1} + ... + wn \bar{zn}
    - assume euclidean inner product is being used unless otherwise stated

- basic properties of inner products:
    - for a fixed v in V, the function that maps from u to <u, v> is linear
    - <v, 0> = 0 for all v in V
    - <0, v> = 0 for all v in V
    - <u, v + w> = <u, v> + <u, w>
    - <u, lambda v> = \bar{lambda} <u, v>

- *norm* of v, denoted by ||v||
    - defined by ||v|| = sqrt(<v, v>)

- basic properties of norms
    - ||v|| = 0 iff v = 0
    - ||lambda v|| = |lambda| ||v||

- two vectors u, v are orthogonal if <u, v> = 0

- 0 is orthogonal to every vector
- 0 is the only vector that is orthogonal to itself

- *pythagorean theorem*
    - if u and v are orthogonal, then
    - ||u + v||^2 = ||u||^2 + ||v||^2

- *orthogonal decomposition*
    - want to write a vector u as a multiple of v + a vector orthogonal to v
    - let c = <u, v> / ||v||^2, w = u - cv
    - then u = cv + w and <w, v> = 0

- *cauchy-schwarz inequality*
    - |<u, v>| <= ||u|| ||v||
    - equal iff one of u, v is a scalar multiple of the other

- *triangle inequality*
    - ||u + v|| <= ||u|| + ||v||
    - equal iff one of u, v is a non-negative real multiple of the other

- *parallelogram equality*
    - ||u+v||^2 + ||u-v||^2 = 2( ||u||^2 + ||v||^2 )


## orthonormal bases

- a list of vectors is *orthonormal* if:
    - each vector in the list has norm 1
    - each vector is orthogonal to all other vectors in the list

- in other words: <e_j, e_k> = 1 if j == k, 0 otherwise for all j, k

- norm of an orthonormal linear combination:
    - ||a1e1 + ... amem||^2 = |a1|^2 + ... + |am|^2
    - follows from pythagorean theorem

- every orthonormal list of vectors is linearly independent

- *bessel's inequality*
    - |<v, e1>|^2 + ... + |<v, em>|^2 <= ||v||^2

- *orthonormal basis*
    - orthonormal list of vectors in V that is also a basis of V
    - orthonormal lists of the right length are bases

- writing a vector as a linear combination of an orthonormal basis
    - v = <v, e1> e1 + ... + <v, em> em
    - ||v||^2 = |<v, e1>|^2 + ... + |<v, em>|^2
    - <u, v> = <u, e1> \bar{<v, e1>} + ... + <u, em> \bar{<v, em>}

- *gram-schmidt* procedure
    - turn an linearly independent list into a orthonormal list with the same span
    - suppose v1, ..., vm is linearly independent
    - let f1 = v1
    - define fk = vk - (<vk, f1> / ||f1||^2) f1 - ... - (<vk, f{k-1}> / ||f{k-1}||) f{k-1}
    - let ek = fk / ||fk||
    - then e1, ..., ek is an orthonormal list

- every finite dimensional inner product space has an orthonormal basis
- every orthonormal list extends to an orthonormal basis

- condition to have an upper triangular matrix with respect to some basis is the
  same as having an upper triangular matrix with an orthonormal basis

- *schur's theorem*
    - every operator on a finite dimensional complex inner product space has an
      upper triangular matrix with respect to some orthonormal basis

### linear functionals on inner product spaces

- if v in V, then the map where u maps to <u, v> is a linear functional on V
- all linear functionals can be represented in this form!

- *riesz representation theorem*
    - let phi be a linear functional on V
    - then there is a unique vector v in V s.t. phi(u) = <u, v> for all u in V


## orthogonal complements and minimization problems

- let U be a subset of V
- then the *orthogonal complement* of U is the set of all vecotrs in V that are
  orthogonal to every vector in U
- $U^\perp = {v \in V : <u, v> = 0 \forall u \in U}$

- properties of orthogonal complements
    - $U^\perp$ is a subspace of V
    - ${0}^\perp = V, V^\perp = {0}$
    - $U \cap U^\perp \subseteq {0}$
    - $G \subseteq H  =>  H^\perp \subseteq G^\perp$

- more results:
    - $U \oplus U^\perp = V$
    - $dim U^\perp = dim V - dim U$
    - $U = (U^\perp)^\perp$
    - $U^\perp = {0}  <=>  U = V$

- suppose U is a finite dimensional subspace of V
- *orthogonal projection* of V onto U
- is the operator $P_U \in L(V)$
- for each v, write v = u + w, where u in U and w in U^\perp
- then let $P_U v = u$
- this is well defined because of result about direct sums

- properties of orthogonal projection
    - $P_U u = u$ for all u in U
    - $P_U w = 0$ for all w in U^\perp
    - range P_U = U
    - null P_U = U^\perp
    - $v - P_U v \in U^\perp$ for all v in V
    - $P_U^2 = P_U$
    - $||P_U v|| <= ||v||$ for all v in V
    - if e1, ..., em is an orthonormal basis of U, then
        - P_U v = <v, e1> e1 + ... + <v, em> em


### minimization problems

- given a subspace U of V and a point v in V,
- find a point u in U s.t. ||v-u|| is as small as possible
- u = P_U v is the unique solution of this problem
- formal result: ||v - P_U v|| <= ||v - u||, with equality iff u = P_U v


### pseudoinverse

- suppose we want to solve Tv = w, but what if T is not invertible?
- aim to find an approximation for the inverse of T

- restriction of a linear map to obtain a bijective map:
    - suppose T in L(V, W)
    - then $T|_{(null T)^\perp}$ is an one-to-one map of null T onto range T
    - its a bijection!

- the *pseudoinverse* $T^\dagger$ is defined by
- $T^\dagger w = (T|_{(null T)^\perp})^-1 P_{range T} w$

- properties of the pseudoinverse:
    - if T is invertible, then $T^\dagger = T^-1$
    - $T T^\dagger = P_{range T} = projection of W onto range T$
    - $T^\dagger T = P_{(null T)^\perp} = projection of V onto (null T)^\perp$

- pseudoinverse provides best approximate solution or best solution:
    - if v in V, then $||T (T^\dagger w) - w|| <= ||Tv - w||$
        - with equality iff v in T^\dagger w + null T
    - if v in T^\daggerw + null T, then $||T^\dagger w|| <= ||v||$
        - with equality if $T^\dagger w = v$

---
### references:
[[linalg]]
