# Injectivity, Surjectivity, and Dimension

Suppose V and W are finite-dimensional vector spaces, and T in L(V, W)
Then:

dim V > dim W       -> then T not injective
dim V < dim W       -> then T not surjective


## Proof for Injective

dim null T + dim range T = dim V, from [[Fundamental Theorem of Linear Maps]]

dim null T = dim V - dim range T

dim V - dim range T >= dim V - dim W, since range T is a subspace of W

however, since dim V > dim W, dim null T > 1, so null T != {0}

thus T is not injective by [[Injective iff Null Space is 0]]


## Proof for Surjective
