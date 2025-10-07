
A list of vectors $v_1, ... , v_n \in V$ is a [[Basis]] $\iff$ every vector $\in V$ can be written uniquely in the form $u = a_1v_1 + ... + a_nv_n$ where $a_1,...,a_n \in \mathbb{F}$.

Suppose $v_1,...,v_n$ is a basis of $V$.

Therefore, $v_1,...,v_n$ spans $V$ and any vector within the span can be written as $u = a_1v_1 + ... + a_nv_n$ for $a_1, ... , a_n \in \mathbb{F}$

To show that this is unique, suppose there was another set of $c_1, ... , c_n \in \mathbb{F}$ such that $u = c_1v_1 + ... + c_nv_n$ is true.

If we subtract these 2 expressions, we get that 

$0 = (a_1 - c_1)v_1 + ... + (a_n - c_n)v_n$

Because this list is a basis, it is also linearly independent. Being linearly independent tells us that the above statement is only true if $(a_1 - c_1) = ... = (a_n - c_n) = 0$.

Therefore $a_k - c_k$ for $1 \leq k \leq n$ is equal to 0. Therefore, $a_k = c_k$, proving that this form is unique.

Suppose that every vector $u \in V$ can be written uniquely in the form $u = a_1v_1 + ... + a_nv_n$ where $a_1,...,a_n \in \mathbb{F}$. Because $u$ can be written in this form, we know that this spans $V$.

Because $0 \in V$, this above statement tells us that the $0$ vector could also be written uniquely.

Therefore, this vector is linearly independent. 

Because it spans $V$ and is linearly independent, therefore its a basis.