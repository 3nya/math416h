# Dimension of a Sum of Subspaces

If $V_1, V_2$ are subspaces of a vector space $V$, then

$$dim(V_1 + V_2) = dim(V_1) + dim(V_2) - dim(V_1 \cap V_2)$$


## Proof

Let $v_1, ..., v_m$ be a basis for $V_1 \cap V_2$. Thus $dim(V_1 \cap V_2) = m$.
Use the [[Extension Lemma]] to extend this a basis of $V_1$: $v_1, ..., v_m, w_1,
..., w_j$. Also use the [[Extension Lemma]] to extend this to a basis of $V_2$:
$v_1, ..., v_m, u_1, ..., u_k$. Thus we have $dim(V_1) = m + j$, $dim(V_2) =
m + k$.

To show that $v_1, ..., v_m, w_1, ..., w_j, u_1, ..., u_k$ is a basis for $V_1 +
V_2$, note that it contains both $span(V_1)$ and $span(V_2)$. Thus it spans 
$V_1 + V_2$. To show that it is linearly independent, suppose

$$0 = a_1 v_1 + ... + a_m v_m + b_1 w_1 + ... + b_j w_j + c_1 u_1 + ... + c_k u_k$$

#todo: show that all the scalars here equal 0. general idea is that $c_1 ... \in
V_1 \cap V_2$, and then we can use the fact that $v... w...$ is linearly indep
to show that $a = b = 0$.

## Remarks

This does not generalize to sums of more than 2 subspaces! Looks like the
inclusion-exclusion principle but is not. For example, #todo.
