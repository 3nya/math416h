# Length of Linearly Independent List

In a finite-dimensional vector space, the length of every linearly independent
list of vectors is less than or equal to the length of every spanning list of
vectors.

Let $U = u_1, ..., u_m$ be a linearly independent list of vectors in $V$.

Let $W = w_1, ... , w_n$, the list of vectors that spans $V$.

We are trying to show that $m \leq n$.

## Step 1:

Take $u_1$ and add it to the list $w_1, ... , w_n$.

The list is now $u_1, w_1, ... , w_n$.

Since $W$ spans $V$, we know that any $u \in U$ (since $u \in V$) is also in $W$.

Because $u_1$ is a scalar multiple of the values in $w_1, ... , w_n$, therefore
the list $u_1, w_1, ... , w_n$ is linearly dependent.

We can now apply the [[Linear Dependence Lemma]], which tells us that some vector in
$u_1, w_1, ... w_n$ is a linear combination of the vectors before it. Therefore,
we can remove some vector in $u_1, w_1, ... , w_n$ such that the remain vectors'
span still spans the list.

Because $u_1$ was from a linearly independent list, $u_1 \neq 0$.

However, since it's the first item in the list, it can not be in the span of the
vectors before it (since the span of an empty list is $\{0\}$).

Because we cannot remove $u_1$, we know that we can remove some $w_j$ in the
list instead for $1 \leq j \leq n$.

Remove $w_j$ from the list, leaving us with the list $u_1, w_1, ..., w_{j - 1},
w_{j + 1}, ... , w_{n}$. 

## Step $k$ for $k = 2, 3, ..., m$:

Take $u_k$ and add it to the list $u_1, ..., u_{k - 1}, w_{n - k}, ...,  w_n$.

The list is now $u_1, ..., u_k, w_{n - k}, ...,  w_n$.

Since $W$ spans $V$, we know that any $u \in U$ (since $u \in V$) is also in $W$.

Because $u_k$ is a scalar multiple of the values in $u_1, ..., u_{k - 1}, w_{n -
k}, ...,  w_n$, therefore the list $u_1, ..., u_k, w_{n - k}, ...,  w_n$ remains
linearly dependent.

We can now apply the [[Linear Dependence Lemma]], which tells us that some
vector in $u_1, ..., u_k, w_{n - k}, ...,  w_n$ is a linear combination of the
vectors before it. Therefore, we can remove some vector in $u_1, ..., u_k, w_{n
- k}, ...,  w_n$ such that the remain vectors' span still spans the list.

Because $u_k$ was from a linearly independent list, and the vectors before it
$u_1, ... , u_{k - 1}$ were from the same linearly independent list, we know
that $u_k$ is not in the span of $u_1, ..., u_{k-1}$. Therefore, it cannot be
removed. 


## Conclusion

Because we cannot remove $u_1, ..., u_k$, the linear dependence lemma tells us
that we can remove some $w_j$ in the list instead for $n - k \leq j \leq n$.

After step $m$, we have added all the vectors from $U$ to the list. At each
step, the linear dependence lemma tells us that there is a potential vector in
$W$ that we can still remove. Therefore, implying that the length of $W$ is
always at least the length of $U$.
