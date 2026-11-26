## Modularity
- Watts Strogatz procedure produces only one type of small world network, not brainlike.
- Network is modular if we can partition it into modules with many connection within each network, but small amounts between partitions.

### Algo:
for n nodes and m edges and C communities. 
- Create C disconnected communities of n/C nodes each
- add m/C random edges within each community
- rewire much like Watts-Strogatz procedure. 
- Each edge is considered in turn and with probability p it keeps one endpoint and the other moves to a random node.
- Most rewired edges end up between communities. p = 1, communities are erased, network is essentially ER.
- The connectivity matrix of network with 6 modules, 20 nodes, p=0.2
- ONLY because we ordered it by module
![[Screenshot 2026-11-26 at 19.40.42.png]]

## Measuring modularty

## Q - Fraction of edges within communities minus expected fraction by chance
- number of nodes,
- k is the degree of node (number of connections)

![[Screenshot 2026-11-26 at 19.50.59.png]]

In maths:
![[Screenshot 2026-11-26 at 19.56.15.png]]

Q is at most 1, and can be negative (when there are fewer edges within the communities than expected by chance)

### NOTE:
Q is defined for given partition - if we know communities in advance, q is easy to compute.
Otherwise, modularity of network is the maximum value of Q over all possible partitions
NP-Hard. Many differnt partitions often have almost the same Q.
In practice, we can use fast heuristics, such as Louvain algorithm

![[Screenshot 2026-11-26 at 20.01.15.png]]