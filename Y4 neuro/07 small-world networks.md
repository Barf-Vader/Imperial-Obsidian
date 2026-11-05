![[Screenshot 2026-11-05 at 16.43.58.png]]# Brain networks
- we can study real brain connectivity with network theory.
- A description of a brain as a network is a connectome.

DTI diffusion imaging lets us build atlas of white matter tracts of human brain. these form communications infrastructure in brain. Can be turned into a network which can be studied mathematically.
- cortical surface parcellated into regions, nodes of the network.
- nodes joined by edge if the white matter data shows a fibre tract between them
- weight of edge reflects thickness of tract. 
- result is small-world modular network

### functional connectomes.
- nodes are same, but two nodes joined by edge if regions are co-active, while subject performs a task or is at rest.
- Independent component analysis ICA of resting state fMRI data reveals **resting-state networks.**
	- Default Mode network is active when subject is resting
		- Everything about myself goes on this.
	- Cognitive control network is active when subject is engaged in a task that demands attention.
### Network
A network G = <V,E>, set of nodes V, set of E VxV edges.
![[Screenshot 2026-11-05 at 16.44.05.png]]

`A(i,j)` is connection from i to j
![[Screenshot 2026-11-05 at 16.45.18.png]]
Can be generalised to account for connection strengths.

For now, no weights, and symmetric (undirected) networks, no self connections `A(i, i) = 0`. 
**Degree** - number of edges a node participates in
**avg degree k** - in undirected network is k=2m/n, where n is num of nodes, m is edges. each m has two matrix entries.
**Path length** - num of edges in the shortest path between two nodes.
**Clustering coefficient** - of node: fraction of all possible edges between neighbours of j that are actual edges. of graph G: avg over all nodes. 
- case of leaf nodes, only one neighbour:
	- clustering coefficient of leaf node is zero. convention we will do in this course.
	- or 1.

![[Screenshot 2026-11-05 at 16.58.27.png]]
### ERDOS-RENYI Network
- every pair of nodes i and. is connected independently with probability p. Edges are assigned uniformly at random.

## Small-world networks
- Common feature of natural networks - high clustering. if x connected to y and z, y and z more likely to connect
- short paths - doesn't take many hops to get from any node to any other.
![[Screenshot 2026-11-05 at 17.03.29.png]]
![[Screenshot 2026-11-05 at 17.03.48.png]]
gamma is clustering coefficient, lambda is path length.