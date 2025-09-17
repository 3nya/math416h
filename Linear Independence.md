$v_1, ... v_m \in V$ and $v \in$ span$(v_1, ... , v_m)$

By the definition of [[Span|Span]],

$v$ can be represented as 

$v = a_1v_1 + ... + a_mv_m$

A list of vectors is considered as linearly independent if 
$0 = a_1v_1 + ... + a_mv_m$ 

only if $a_1 = ... = a_m = 0$

ie none of the vectors are multiples of each other 

## Linearly dependent
Negate the previous definition of being linearly independent
$0 = a_1v_1 + ... + a_mv_m$ 
can be represented when not all $a_1 ... a_m$ are $0$.

### Linear dependence lemma
Suppose $v_1, ... , v_m$ is a linearly dependent list in $V$. Then there exists $k \in \{1,2,...m\}$ such that 

$v_k \in$ span$(v_1, ... , v_{k-1})$

this also tells us that if $v_k$ is removed, the span of the list remains unchanged. 
[[Linear Dependence Lemma|proof]]


## Properties
[[Length of Linearly Independent List|Length of linearly independent list <= length of spanning list]]


