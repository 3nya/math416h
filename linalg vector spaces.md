---
id: linalg vector spaces
aliases: []
date: 2025-05-11
---
# linalg vector spaces
tags: #linalg

---

## field basics

- recall definitions of a *field*:
    - ring where all non-zero elements have a multiplicative inverse,
    - and multiplication is commutative

- a *field* $(F, 0, 1, +, *)$
    - has a set F
    - has additive identity 0, multiplicative identity 1
    - 0 != 1
    - and two operations + and *:
    - + and * are commutative and associative
    - all elements have additive inverse
    - all nonzero elements have multiplicative inverse

- ex. complex numbers form a field:
- (a + bi) + (c + di) = (a + c) + (b + d) i
- (a + bi) (c + di) = (ac - bd) + (ad + bc) i

- recall F^n = { (x1, ..., xn) | xi in F }
- F^n is nor a field for n >= 2 !!! 
    - if we define multiplication component wise
    - it is a ring.

## vector spaces

- vector space V over a field F
- two operations: vector addition and scalar multiplication

- better definition:
    - (V, +, *) over a field F
    - + : V x V -> V
    - * : F x V -> V
    - commutativity: $u + v = v + u$ for all $u, v in V$
    - associativity: $u + (v + w) = (u + v) + w$, $a(bv) = (ab)v$
    - additive identity: exists $0 in V$ s.t. $v + 0 = v$
    - additive inverse: for all v in $V$, exists $w$ s.t. $v + w = 0$
    - multiplicative identity: $1v = v$, where $1 in F, v in V$
    - distributive properties: $a(u + v) = au + av$ and $(a + b)v = av + bv$

- associativity of vector addition
- commutativity of vector addition
- identity element of vector addition
- inverse elements of vector addition
- identity element of scalar multiplication
- a(bv) = (ab)v
- (a + b)v = av + bv
- a(u + v) = au + av

in other words...
- vector addition forms an abelian group
- plus the remaining 4 axioms.

- set of all n-tuples with entries from a field F is denoted by F^n
- ex. R^3 is a vector field over R

## matrices

- can be considered as a bunch of row vectors or column vectors
- *zero matrix* where each entry = 0, denoted by O
- *square* if rows and cols are equal
- *matrix addition* and *scalar multiplication*

## properties of vector spaces

- cancellation law: x + z = y + z => x = y
- zero vector is unique
- pretty much properties of fields also hold in vector spaces

## subspaces

- W is a subspace of V if W is also a vector space over F
- denoted as $W \leq V$
- {0} and V are always subspaces of a vector space V

- many of the axioms of a vector space already hold in W...
- need to check
    - W is closed under vector addition
    - W is closed under scalar multiplication
    - W has the zero vector (non-empty and additive identity)

- zero vector is W is same as the zero vector in V
- actually checking inverses is redundant:
    - -1(v) = -v, and -1(v) in W because W is closed under scalar multiplication

- the *transpose* of a matrix is made by swapping rows with columns
    - (A^t)_ij = A_ji
    - if A is m by n, A^t is n by m

- a matrix is *symmetric* if A = A^t
- set of all symmetric matrices is a subspace of the whole vector space

- *diagonal* matrix : all non-diagonal values are 0
- *trace* : tr(A) = sum of all values along the main diagonal of A

- intersection of two subspaces is again a subspace

- sum of two subspaces is also a subspace
    - V1 + V2 = { v1 + v2 | v1 in V1, v2 in V2 }
    - given subspaces V1, V2, etc. V1 + V2 is the smallest subspace that
    - contains V1 and V2
- direct sum: can only be written one way as a combination of v1, v2, ...
    - U + W is a direct sum <=> U intersect W = {0}
    - the only way to write 0 is 0 + ... + 0

## linear combinations and systems of linear equations

- u = a1v1 + a2v2 + a3v3 ... a finite number
- where v's are vectors and a's are scalars
- a's are called coefficients

- zero vector is a linear combination of any non-empty subset
- how to check if something can be represented as a linear combination?
    - set up and solve a system of equations

- let S be a subset of a vector space V
- the *span* of S, span(S), the set of all linear combinations of vectors in S
- span(empty set) = {0}

- span(S) is always a subspace of V
- S *generates* or spans V if span(S) = V

- thm: span(V) is the smallest subspace containing V

## linear dependence and linear independence

- given a subset S of V, find the smallest subset X in S such that
    - span(X) = span(S)

- if a vector in S is a linear combination of the other vectors
    - it can be removed
    - bashing this takes a lot of time...

- if the zero vector can be represented as a linear combination
    - with coefficients that are not all zero
    - then one of the non-zero coefficient vectors can be removed
    - if this is the case, S is *linearly dependent*
    - *linearly independent* otherwise

- *trivial representation of 0* : 0 = 0 u1 + 0 u2 + 0 u3...

- facts about linear independence:
    - empty set is always linearly independent
    - set containing a single nonzero vector is linearly independent
    - a set is linearly independent iff only representations of 0 are trivial
    - subset of linearly independent set is linearly independent

- theorem: let S be a linearly independent subset of V, and let v in V not in S.
    - then S union {v} is also linearly independent

## bases and dimension

- a *basis* beta of a vector space V is a linearly independent subset of V
    - that generates V
    - vectors of beta form a basis for V

- *standard basis*
    - in F^n
    - e1 = (1, 0, ...,  0), e2 = (0, 1, ...,  0), ..., en = (0, 0, ...,  1), 
    - {e1, e2, ..., en} is a basis for F^n

- basis can be finite as well as infinite
- if V is generated by a finite set S, then some subset of S is a basis for V
    - a finite spanning set for V can be reduced to a basis for V

- *replacement theorem:*
    - let V be a vector space generated by G, |G| = n
    - let L be a linearly independent subset of V, |G| = m
    - then there exists a subset of G, H, s.t. L union H generates V
    - |H| = n - m
- if V has a finite basis, then every basis for V has the same number of vectors

- a vector space is *finite-dimensional* if it has a finite basis
- number of vectors in the basis is the *dimension* of V, dim(V)
- dimension of a vector space depends on its field of scalars

- if W is a subspace of V
    - dim(W) <= dim(V)
    - if dim(W) = dim(V), then W = V

- alterative definition for finite dimensional vector space:
    - if there exists a finite list of vectors s.t. span(v1, ..., vn) = V
    - otherwise infinite dimensional

- every spanning list in a vector space can be reduced to a basis
- every linearly independent list can be expanded to a basis

- any two bases of a finite-dimensional vector space has the same length
- linearly independent list of the right length is a basis

---
### references:
[[linalg]]
