## Breadth-first search

### Lemma 1
Let \\(G = (V, E)\\) be a directed or undirected graph, and let \\(s \in V\\) be an arbitrary vertex. Then for any edge \\((u, v) \in E\\),\\( \delta (s, v) \leq \delta (s, u) + 1\\).

### Lemma 2
Let \\(G = (V, E)\\) be a directed or undirected graph, and suppose that BFS is run on \\(G\\) from a given source vertex \\(s \in V\\). Then upon termination for each vertex \\(s \in V\\), the value \\(v.d\\) computed by BFS satisfies \\(v.d \geq \delta (s, v)\\).

### Lemma 3
Suppose that during the execution of BFS on a graph \\(G = (V, E)\\), the queue \\(Q\\) contains the vertices \\(\langle v_{1}, v_{2}, \dots, v_{r} \rangle\\), where \\(v_{1}\\) is the head of \\(Q\\) and \\(v_{r}\\) is the tail. Then \\(v_{r}.d \leq v_{1}.d + 1\\) and \\(v_{i}.d \leq v_{i+1}.d\\) for \\(i = 1, 2, \dots, r-1\\)

### Corollary 4
Suppose that vertices \\(v_{i}\\) and \\(v_{j}\\) are enqueued during the execution of BFS, and that \\(v_{i}\\) is enqueued before \\(v_{j}\\). Then \\(v_{i}.d \leq v_{j}.d\\) at the time \\(v_{j}\\) is enqueued.

### Theorem 5 (Correctness of breadth-first search)
Let \\(G = (V, E)\\) be a directed or undirected graph, and suppose that BFS is run on \\(G\\) from a given vertex \\(s \in V\\). Then, during its execution, BFS discovrs every vertex \\(v \in V\\) that is reachable form the source \\(s\\), and upon termination, \\(v.d = \delta (s, v)\\) for all \\(v \in V\\). Moreover, for any vertex \\(v \ne s\\) that is reachable from \\(s\\), one of the shortest paths from \\(s\\) to \\(v\\) is a shortest path from \\(s\\) to \\(v.\pi\\) followed by the edge \\(v.\pi, v\\).

### Lemma 6
When applied to a directed or undirected graph \\(G = (V, E)\\), procedure BFS constructs \\(\pi\\) so that the predecessor subgraph \\(G_{\pi} = (V_{\pi}, E_{\pi})\\) is a breadth-first tree.

## Depth-first search

### Theorem 7 (Parenthesis theorem)
In any depth-first search of a (directed or undirected) graph \\(G = (V, E)\\), for any two vertices \\(u\\) and \\(v\\), exactly one of the following three conditions holds:
* the intervals \\([u.d, u.f]\\) and \\([v.d, v.f]\\) are entirely disjoint and neither \\(u\\) nor \\(v\\) is a descendant of the other in the depth-first forest.
* the interval \\([u.d, u.f]\\) is contained entirely within the interval \\([v.d, v.f]\\), and \\(u\\) is a descendant of \\(v\\) in a depth-first tree, or
* the interval \\([v.d, v.f]\\) is contained entirely within the interval \\([u.d, u.f]\\), and \\(v\\) is a descendant of \\(u\\) in a depth-first tree.

### Corollary 8 (Nesting of descendants' interval)
Vertex \\(v\\) is a proper descendant of vertex \\(u\\) in the depth-first forest for a (directed or undirected) graph \\(G\\) if and only if \\(u.d < v.d < v.f < u.f\\).

### Theorem  9 (White-path theorem)
In a depth-first forest of a (directed or undirected) graph \\(G = (V, E)\\), vertex \\(v\\) is a descendant of vertex \\(u\\) if and only if at the time \\(u.d\\) that the search discovers \\(u\\), there is a path from \\(u\\)to \\(v\\) consisting entirely of white vertices.

### Theorem 10
In a depth-first search of undirected graph \\(G\\), every edge of \\(G\\) is either a tree edge or a back edge.

## Topological sort

### Lemma 11
A directed graph \\(G\\) is acyclic if and only if a depth-first search of \\(G\\) yields no back edges.

### Theorem 12
TOPOLOGICAL-SORT produces a topological sort of the directed acyclic graph provided as its input.

## Strongly connected components

### Lemma 13
Let \\(C\\) and \\(C^{\prime}\\) be distinct strongly connected components in a directed graph \\(G = (V, E)\\), let \\(u, v \in C\\), let \\(u^{\prime}, v^{\prime} \in C^{\prime}\\), then suppose that \\(G\\) contains a path \\(u \leadsto u^{\prime}\\). Then \\(G\\) also cannot contain a path \\(v^{\prime} \leadsto v\\).

### Lemma 14
Let \\(C\\) and \\(C^{\prime}\\) be distinct strongly connected components in directed graph \\(G = (V, E)\\). Suppose that there is an edge \\((u, v) \in E\\), where \\(u \in C\\) and \\(v \in C^{\prime\}\\). Then \\(f(C) > f(C^{\prime})\\). 

### Corollary 15
Let \\(C\\) and \\(C^{\prime}\\) be distinct strongly connected components in directed graph \\(G = (V, E)\\). Suppose that there is an edge \\((u, v) \in E^{T}\\), where \\(u \in C\\) and \\(v \in C^{\prime}\\). Then \\(f(C) < f(C^{\prime}\\). 

### Theorem 16
The STRONGLY-CONNECTED-COMPONENTS procedure correctly computes the strongly connected components of the directed graph provided as its input.

## References
1. Introduction to Algorithms, MIT Press
