---
layout: default
title: Graph Thinness
---
<div style="display:none;">
$
\newcommand{\thin}{\mathsf{thin}}
\newcommand{\thinind}{\mathsf{thin_ind}}
\newcommand{\thincmp}{\mathsf{thin_cmp}}
\newcommand{\pthin}{\mathsf{pthin}}
\newcommand{\pthinind}{\mathsf{pthin_ind}}
\newcommand{\pthincmp}{\mathsf{pthin_cmp}}
\newcommand{\pw}{\mathsf{pw}}
\newcommand{\bw}{\mathsf{bw}}
\newcommand{\diam}{\mathsf{diam}}
$

</div>
# Graph Thinness
## Definitions
- *Consistent solution*: Let $G$ be a graph. A *consistent solution for $G$ using $k$ classes* is a partition $S$ of $V(G)$ and an order $\prec$ on $V(G)$ such that for every $u,v,w \in V(G)$ with $u \prec v \prec w$, if $u$ and $v$ belong to the same class in $S$ and $(u,w) \in E(G)$, then $(v,w) \in E(G)$. {% cite thinness %}
- *Thinness*: A graph $G$ is *$k$-thin* if there exists an order and a partition on the vertices of $G$ into $k$ classes that are consistent. The *thinness* of $G$, denoted $\thin(G)$, is the smallest $k$ such that $G$ is $k$-thin. {% cite thinness %}
- *Strongly consistent solution*: Let $G$ be a graph. A *strongly consistent solution for $G$ using $k$ classes* is a partition $S$ of $V(G)$ and an order $\prec$ on $V(G)$ such that $S$ is consistent both with $\prec$ and with the inverse of $\prec$. {% cite proper-thinness %}
- *Proper thinness*: A graph $G$ is *proper $k$-thin* if there exists a partition $S$ and an order $\prec$ on the vertices of $G$ that are strongly consistent. The *proper thinness* of $G$, denoted $\pthin(G)$, is the smallest $k$ such that $G$ is proper $k$-thin. {% cite proper-thinness %}
- *Independent (proper) thinness*: A graph $G$ is *(proper) $k$-independent-thin* if there exists a partition $S$ of $V(G)$ (strongly) consistent with an order $\prec$ on $V(G)$ such that each part of $S$ is an independent set of $G$. The *independent (proper) thinness* of $G$, denoted $\thinind(G)$ ($\pthinind(G)$), is the smallest $k$ such that $G$ is (proper) $k$-independent-thin. {% cite thinness-of-product-graphs %}
- *Complete (proper) thinness*: A graph $G$ is *(proper) $k$-complete-thin* if there exists a partition $S$ of $V(G)$ (strongly) consistent with an order $\prec$ on $V(G)$ such that each part of $S$ is a clique of $G$. The *complete (proper) thinness* of $G$, denoted $\thincmp(G)$ ($\pthincmp(G)$), is the smallest $k$ such that $G$ is (proper) $k$-independent-thin. {% cite thinness-of-product-graphs %}

## Thinness of graph classes
- For every $t \geq 1$, $\thin(\overline{tK_2}) = \pthin(\overline{tK_2}) = \thinind(\overline{tK_2}) = \pthinind(\overline{tK_2}) = t.$ {% cite thinness thinness-of-product-graphs %}

## Relation to other parameters
- $\thinind(G) \leq \pw(G) + 1$, where $\pw(G)$ is the [pathwidth](https://en.wikipedia.org/wiki/Pathwidth) of $G$. {% cite thinness 2-thin-intersection-models %}
- $\pthinind(G) \leq \bw(G) + 1$ and $\pthin(G) \leq \max\\{1, \bw(G)\\}$, where $\bw(G)$ is the [bandwidth](https://en.wikipedia.org/wiki/Graph_bandwidth) of $G$. Moreover,
a linear layout realizing the bandwidth leads to a (strongly) consistent partition
into at most $\bw(G)$ classes. {% cite 2-thin-intersection-models %}
- For every connected graph $G$, $\pthin(G) \leq \|V(G)\| - \diam(G)$, where $\diam(G)$ is the [diameter](https://en.wikipedia.org/wiki/Distance_(graph_theory)) of $G$. {% cite 2-thin-intersection-models %}
- $\pthinind(G) \leq 2^{\pw(G)}\cdot(\pw(G) + 1)$. Moreover, given a path decomposition of width $q$, a vertex ordering and a strongly consistent partition into at most $2^q\cdot(q + 1)$ independent sets can be found in polynomial time. {% cite mim-width-convex-graphs %}

## References
{% bibliography --cited %}