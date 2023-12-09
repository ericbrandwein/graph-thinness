---
layout: default
---
<div style="display:none;">
$
\newcommand{\thin}{\mathsf{thin}}
\newcommand{\pthin}{\mathsf{pthin}}
\newcommand{\pw}{\mathsf{pw}}
\newcommand{\bw}{\mathsf{bw}}
$

</div>
# Graph thinness
## Definitions
- *Consistent solution*: Let $G$ be a graph. A *consistent solution for $G$ using $k$ classes* is a partition $S$ of $V(G)$ and an order $\prec$ on $V(G)$ such that for every $u,v,w \in V(G)$ with $u \prec v \prec w$, if $u$ and $v$ belong to the same class in $S$ and $(u,w) \in E(G)$, then $(v,w) \in E(G)$. {% cite thinness %}
- *Thinness*: A graph $G$ is *$k$-thin* if there exists an order and a partition on the vertices of $G$ into $k$ classes that are consistent. The *thinness* of $G$, denoted $\thin(G)$, is the smallest $k$ such that $G$ is $k$-thin. {% cite thinness %}
- *Strongly consistent solution*: Let $G$ be a graph. A *strongly consistent solution for $G$ using $k$ classes* is a partition $S$ of $V(G)$ and an order $\prec$ on $V(G)$ such that $S$ is consistent both with $\prec$ and with the inverse of $\prec$. {% cite proper-thinness %}
- *Proper thinness*: A graph $G$ is *proper $k$-thin* if there exists a partition $S$ and an order $\prec$ on the vertices of $G$ that are strongly consistent. The *proper thinness* of $G$, denoted $\pthin(G)$, is the smallest $k$ such that $G$ is proper $k$-thin. {% cite proper-thinness %}

## Relation to other parameters
- $\thin(G) \leq \pw(G) + 1$, where $\pw(G)$ is the [pathwidth](https://en.wikipedia.org/wiki/Pathwidth) of $G$. {% cite thinness %}
- For every graph $G$ with $|E(G)|\geq 1$, $\pthin(G) \leq \bw(G)$, where $\bw(G)$ is the [bandwidth](https://en.wikipedia.org/wiki/Graph_bandwidth) of $G$. Moreover,
a linear layout realizing the bandwidth leads to a (strongly) consistent partition
into at most $\bw(G)$ classes. {% cite 2-thin-intersection-models %}

## References
{% bibliography --cited %}