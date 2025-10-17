---
id: linalg eigenvalues and eigenvectors
aliases: []
date: 2025-06-23
---
# linalg eigenvalues and eigenvectors
tags: #linalg

---

## invariant subspaces

- *operator* : linear map from a vector space to itself

- let T be an operator on V
- a subspace U of V is *invariant* under T if Tu in U for all u in U
    - aka T|_U is an operator on U

- {0}, V, null T, range T are all invariant under T

- lambda in F is an *eigenvalue* of T
    - if there exists v in V, v != 0, Tv = lambda v
- V has a *one-dimensional subspace invariant under T* iff
    - *T has an eigenvalue*
    - we have $Tv = \lambda v$, and $\lambda v \in \Span v$

- equivalent conditions to be an eigenvalue:
    - suppose V is finite-dimensional, T in L(V), lambda in F
    - lambda is an eigenvalue of T
    - T - lambda I is not injective
    - T - lambda I is not surjective
    - T - lambda I is not invertible

- v is an *eigenvector* of T corresponding to an eigenvalue lambda of T if
    - v != 0, and Tv = lambda v
    - equivalent to: v is in null(T - lambda I)

- every list of eigenvectors of T corresponding to distinct eigenvalues of T is
linearly independent
- each operator on V can have at most dim V distinct eigenvalues

### polynomials applied to operators

- can take operators to powers
- can apply polynomials to operators:
    - $p(T) = a_0 I + a_1 T + ... + a_m T^m $

- product of polynomials:
    - (pq)(z) = p(z) q(z)
    - p(z) q(z) = q(z) p(z)

- null space and range of p(T) are invariant under T

## minimal polynomial

- every operator on finite-dim, non-zero complex vector space has an eigenvalue

- remark: general idea of proof
    - let $u \neq 0 \in V$, then $u, Tu, ..., T^n u$ is linearly dependent
    - thus we can write $0 = a_0 u + a_1 Tu + ... + a_n T^n u$
    - not all the $a_i$s are 0, since the list is linearly dependent
    - can solve for roots of the polynomial
        - by fundamental thm. of algebra, there must be complex roots of a
        complex polynomial
    - then we can factor into $0 = c (T - \lambda_1 I) ... (T - \lambda_n I)$
    - so we have eigenvalues!

### eigenvalues and the minimal polynomial

- *monic polynomial*
    - polynomial whose highest-degree coefficient is 1

- suppose T in L(V)
- there exists a unique monic polynomial of smallest degree p s.t. p(T) = 0
- deg p <= dim V
- p is the *minimal polynomial*

- solving for the minimal polynomial:
    - find smallest positive integer m s.t.
    - $c_0 I + c_1 T + c_2 T^2 + ... + c_{m-1} T^{m-1} = -T^m$
    - replace T with its matrix and solve as a system of linear equations
    - or can pick some v and replace each T with Tv

- eigenvalues are the zeroes of the minimal polynomial
- q(T) = 0 iff q is a polynomial multiple of the minimal polynomial
- minimal polynomial of T is a poly. multiple of minimal polynomial of T|_U

- T not invertible iff constant term of minimal polynomial is 0
    - T not invertible => 0 is an eigenvalue

- dim null (T^2 + bT + cI) is even iff b^2 < 4c
- operators on odd dimensional vector spaces always have eigenvalues


## upper triangular matrices

- matrix of an operator is always square
- basis is the same for both dimesions
- assume standard basis if not specified

- diagonal of a square matrix is from upper left to bottom right
- a square matrix is *upper triangular* if entries below the diagonal are 0

- suppose T is an operator on V, and v1, ..., vn is a basis of V
- then the following are equal:
    - matrix of T with respect to v1, ..., vn is upper triangular
    - span(v1, ..., vk) is invariant under T for each k = 1, ..., n
    - Tvk in span(v1, ..., vk) for each k = 1, ..., n

- if T is an upper triangular matrix, then
    - (T - lambda_1 I) ... (T - lambda_n I) = 0
    - where lambda_1, ..., lambda_n are along the diagonal
- eigenvalues of T are along the diagonal of an upper triangular matrix

- T has an upper triangular matrix iff
    - minimal polynomial of T = (z - lambda_1) ... (z - lambda_m)

- if F = C, then every operator on V has an upper triangular matrix


## diagonalizable operators

- *diagonal matrix*
    - square matrix that is 0 everywhere except for the diagonal

- entries on the diagonal are eigenvalues of the operator
- an operator is *diagonalizable* if it has a diagonal matrix with respect to
some basis

- suppose T in L(V), lambda in F
- *eigenspace* of T corresponding to lambda is E(lambda, T)
    - = null(T - lambda I) = {v in V : Tv = lambda v}
- eigenspace is a subspace
- eigenspace consists of all eigenvectors of T corresponding to lambda + 0

- lambda is an eigenvalue of T iff E(lambda, T) != {0}

- sum of eigenspaces is a direct sum
- sum of dimensions of eigenspaces is always <= dim V

- conditions equivalent to diagonizability:
    - T is diagonalizable
    - V has a basis consisting of eigenvectors of T
    - V = $E(\lambda_1, T) \oplus ... \oplus E(\lambda_m, T)$
    - dim V = dim E(lambda_1, T) + ... + dim E(lambda_m, T)

- some operators do not have enough eigenvectors to be diagonalizable:
    - ex. T in L(F^3) where T(a, b, c) = (b, c, 0)
- enough eigenvalues implies diagonalizability
    - if T in L(V) has dim V distinct eigenvalues, then T is diagonalizable
- diagonalizing operators makes it easier to compute large powers of T

- T is diagonalizable if minimal polynomial of T can be factored into distinct
linear factors:
    - p(z) = (z - lambda_1) ... (z - lambda_m)
    - where lambda_1, ..., lambda_m are distinct

- if T is diagonalizable and U is invariant under T, then T|_U is a
diagonalizable on U

- *gershgorin disk theorem?* : doesn't look terribly applicable


## commuting operators

- two operators on the same vector space *commute* if ST = TS
- same for matrices: AB = BA

- two operators commute iff their matrices do

- if two operators are invariant, then every eigenspace for one operator is
invariant under the other

- operators have diagonal matrices under the same basis iff they commute
- also simulatenously upper-triangularizable

- every pair of commuting operators on a finite dimensional nonzero complex
vector space has a common eigenvector

- if S and T commute, then
    - every eigenvalue S + T = an eigenvalue of S + an eigenvalue of T
    - every eigenvalue ST = an eigenvalue of S * an eigenvalue of T

---
### references:
[[linalg]]
