# Injective iff Null Space is 0

## Rightarrow

Proving =>. Suppose T is injective.

We want to prove null T = {0}.

We know $T(0) = 0$...

TODO: finish this.


## Leftarrow

Proving <=. Suppose null T = {0}

To prove T is injective, suppose $u_1, u_2 \in V$ and $T(u_1) = T(u_2)$.

Then $0 = T(u_1) - T(u_2)$
$\implies 0 = T(u_1 - u_2)$     because additivity of linear maps
$\implies 0 = u_1 - u_2$        because null T = {0}
$\implies u_1 = u_2$

Thus T is injective.
