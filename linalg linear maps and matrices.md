---
id: linalg linear maps and matrices
aliases: ["linear transformations"]
date: 2025-05-15
---
# linalg linear maps and matrices
tags: #linalg

---

## linear transformations, null spaces, and ranges

- *linear transformation*
    - aka linear map
    - let V and W be vector spaces,
    - T : V -> W is a linear transformation if
        - *additivity* : T(x + y) = T(x) + T(y)
        - *homogeneity* : T(cx) = cT(x)
    - preserves the structure (like a homomorphism)

- has applications in geometry
    - rotation, translation, projection are all linear transformations

- *identity transformation* (I)

- *zero transformation* (T_0)
    - T_0(x) = 0 for all x in V

- *null space*
    - given a linear map T : V -> W, N(T) = { v in V | T(v) = 0 }
    - like the kernel
- *range*
    - aka image
    - R(T) = { T(x) | x in V }

- null space and range of any linear transformation are subspaces

- if beta is a basis for V, then R(T) = span(T(beta))
- this finds a spanning set for R(T)

- given a linear transformation T : V -> W,
    - *nullity* is the dimension of null space of T, nullity(T)
    - *rank* is the dimension of range of T, rank(T)

- *dimension theorem*
    - nullity(T) + rank(T) = dim(V)
    - if V is finite-dimensional

- a linear transformation T is one to one iff N(T) = {0}
    - same law as for homomorphisms and kernels

- let V and W be vector spaces with the same finite dimension...
    - following are equivalent
    - T is one to one
    - T is onto
    - rank(T) = dim(V)
- note that this needs to be finite dimensional

- a linear transformation is completely determined by its *action on a basis*
    - suppose {v1, v2, ..., vn} is a basis for V
    - for w1, w2, ..., wn in W, there exists exactly one linear transformation
    - such that T(vi) = wi for all i

## from linear algebra done right...

- let L(V, W) be the set of linear transformations from V to W
    - define addition as (S + T)(v) + Sv + Tv
    - define scalar multiplication (xT)v + x(Tv)
- L(V, W) is a vector space !!
- can define normal multiplication as function composition

- properties of products of linear maps
    - associative
    - there is an identity element
    - left and right distributive properties hold

- linear maps take 0 to 0

- fundamental theorem of linear maps:
    - dim V = dim null T + dim range T

- linear map to a lower-dimensional space is never injective
- linear map to a higher-dimensional space cannot be surjective

- homogeneous system of equations : the constant term on the right is 0
- homogeneous system of linear equations with more variables than equations has
  nonzero solutions
- system of linear equations with more equations than variables has no solution
  for some choice of the constant terms

- matrix of a linear map, M(T)
- F^m,n represents the set of all m-by-n matrices with entries in F
    - this is also a vector space of dimension mn

- matrix of product of linear maps: M(ST) = M(S) M(T)

## matrix representation of a linear transformation

- *ordered basis*
    - basis for V with a sepcific order
    - {e1, e2, ..., en} is the standardard ordered basis

- *coordinate vector*
    - given x in V, ordered basis beta for V = {u1, u2, ..., un}
    - coordinate vector of x relative to beta
    - is the column vector: (a1, a2, ..., an)
    - such that: a1 u1 + a2 u2 + ... + an un = x

- *matrix representation*
    - given vector spaces V, W
    - with bases beta = {v1, ..., vn}, gamma = {u1, ..., un}
    - for each v in beta, find coordinate vector v relative to gamma

- adding matrix representations is equal to adding linear maps
- same for multiplying matrix representations by a scalar

- *column rank* : dimension of the span of the columns of A
- *row rank* : dimension of the span of the rows of A
- both column rank and row rank are at most $min(m, n)$
- column rank equals the row rank!

- *column-row factorization*
    - let A be a m-by-n matrix
    - then A = CR for some C is a m-by-p matrix and R is p-by-n


## composition of linear transformations and matrix multiplication

- matrix multiplication is the same as function composition of linear maps
- (m x n) (n x p) = (m x p)

- you can do this for bases too?


## invertibility and isomorphism

### invertibility

- linear map is *invertible* if there exists an inverse
    - ST = TS = I
    - denoted by T^-1
- inverse of invertible map is *unique*

- linear map is invertible iff it is bijective
- injectivity = surjectivity = invertiblility if dim V = dim W is finite

- ST = I implies TS = I on vector spaces of the same dimension

### isomorphism

- *isomorphism* : invertible linear map
- vector spaces are *isomorphic* if there exists an isomorphism between them

- dimension shows whether vector spaces are isomorphic
- finite-dim. vector spaces are isomorphic iff they have the same dimension
- L(V, W) is isomorphic to F^{m, n}
- dim L(V, W) = (dim V)(dim W)

- linear maps act like matrix multiplication:
    - turn the vector into a column vector (n by 1 matrix)
    - then do matrix multiplication
- each matrix in F^{m, n} induces a linear map
- matrix A depends on choice of bases
    - choose bases that make A simple

- dimension of range T equals column rank of M(T)

### change of basis

- identity matrix I has 1s on the diagonal and 0s everywhere else
- can find the identity matrix with respect to two different bases
    - this matrix is always invertible
    - lets us change between bases

- #todo: write down the rule for matrix multiplication

- change of basis formula
    - suppose u1..., v1... are bases of V
    - let A = M(T, u1...), B = M(T, v1...), C = M(I, u1..., v1...)
    - A = C^-1 B C

## products and quotients of vector spaces

### product of vector spaces

- V1 x V2 x V3 ... = { (v1, v2, v3, ...) : v1 in V1, v2 in V2, ... }
- addition and scalar multiplication are component wise
- product of vector spaces is a vector space
- dimension of product = sum of dimensions of each individual vector space

### quotient spaces

- sum of vector and subset
    - v + U = { v + u : u in U }
    - like cosets

- v + U is a *translate* of U
- V / U is the set of all translates of U
    - { v + U : v in V }

- two translates of a subspace are either equal or disjoint
- quotient space is a vector space

- *quotient map*
    - pi : V -> V/U
    - pi(v) = v + U
    - maps each vector to a translate

- dim V/U = dim V - dim U

- each linear map T induces a linear map T~ on V / (null T)
    - T~ : V / (null T) -> W
    - T~ (v + null T) = Tv

- facts:
    - T~ of pi = T
    - T~ is injective
    - range T~ = range T
    - V / (null T) and range T are isomorphic

## duality

### dual space and dual map

- *linear functional* on V
    - map from V to F

- *dual space* / *V'*
    - vector space of all linear functionals on V
    - V' = L(V, F)
- dim V' = dim V

- *dual basis*
    - let v1, ..., vn be a basis of V
    - the dual basis of v1 ... is phi_1, ..., phi_n
    - where phi_j (v_k) = 1 if k = j, 0 otherwise
- dual basis gives coefficients for linear combination
    - v = phi1(v) v1 + ... + phin(v) vn
- dual basis is a basis of the dual space

- *dual map*
    - suppose T in L(V, W), dual map T' in L(W', V')
    - T'(phi) = phi of T

- algebraic properties of dual maps:
    - (S + T)' = S' + T'
    - (xT)' = xT'
    - (ST)' = T'S'

### null space and range of dual linear map

- *annihilator* / *U^0*
    - for U subset of V, the annihilator of U is defined
    - { phi in V' : phi(u) = 0 for all u in U }

- the annihilator is a subspace
    - U^0 is a subspace of V'

- dim U^0 = dim V - dim U
    - if V is finite dimensional

- U^0 = {0} iff U = V
- U^0 = V' iff U = {0}

- null T' = (range T)^0
- dim null T' = dim null T + dim W - dim V

- dim range T' = dim range T
- range T' = (null T)^0

- T surjective is equivalent to T' injective
- and vice versa

### matrix of dual of linear map

- matrix of T' is transpose of matrix of T
- M(T') = (M(T))^t


## addendum:

- given a 2x2 matrix (a, b; c, d), its inverse is:
- 1/(ad-bc) (d, -b; -c, a)

- when you have the change of base matrix from v to w,
- and multiply with change of base matrix from w to v,
- you get the identity matrix.

- fundamental rule for matrix multiplication:
- #todo: this

---
### references:
[[linalg]]
