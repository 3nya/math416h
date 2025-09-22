# Fundamental Theorem of Linear Maps

Suppose V is finite dimensional and T in L(V, W).

Then range(T) is also finite-dimensional and

dim V = dim null T + dim range T


## Proof:

Let $u_1, ..., u_m$ be a basis of $null T$. (Such a basis exists because $null T
\le V$, and V is finite dimensional, thus dim null T <= dim V.)

$u_1, ..., u_m$ is linearly independent because it is a basis.

By the [[Extension Lemma]], we can extend it to a basis of V: $u_1, ..., u_m,
v_1, ..., v_n$.

Then we have $dim null T = m$, and $dim V = m + n$.
We need to show $dim range T = n$.

We will show: $Tv_1, ..., Tv_n$ is a basis of $range T$.

Proving $Tv_1, ..., Tv_n$ spans $range T$:

Let $w \in V$. Then $w = a_1 u_1 + ... + a_m u_m + b_1 v_1 + ... + b_n v_n$
$\implies Tw = T(a_1 u_1 + ... + a_m u_m + b_1 v_1 + ... + b_n v_n)$
$\implies Tw = T(a_1 u_1) + ... + T(a_m u_m) + T(b_1 v_1) + ... + T(b_n v_n)$
$\implies Tw = 0 + T(b_1 v_1) + ... + T(b_n v_n)$
$\implies Tw = b_1 T(v_1) + ... + b_n T(v_n)$

TODO: finish this.

Since $Tv_1, ..., Tv_n$ is a basis of $range T$, $dim range T = n$, and we have
$dim V = m + n = dim null T + dim range T$.
