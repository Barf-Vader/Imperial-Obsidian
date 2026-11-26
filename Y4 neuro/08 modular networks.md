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
Small world index is undefined for mostly disconnected networks because path length is undefined.

Space shapes the shape of the networks, take the london underground for example.

## Spatial embedding
- Real networks are spatially embedded - nodes have positions, and their positions influence how they connect.
- Ring lattice of Watts Strogatz procedure is one kind of spacial embedding but only one direction.
- We can place nodes on 2D place, and make probability of connection decrease with distance. Not good model for whole brain connectivity but good for a small patch of cortex.
	- Place n node at random positions. in a square of side 0.5, so all distances are less than 1.
	- Connect each pair of nodes with p = e^-hd
	- h - constant how quickly connections become rare with distance. High h, probability drops very quickly.![[Screenshot 2026-11-26 at 20.27.06.png]]
- both the small world index and modularity increase with h (beyond small values of h)
- But with very high values of h the network fragments, and small world index becomes undefined.
## Gen model
- brain regions stay fixed and edges are added one at a time.
- new edge i and j with p: ![[Screenshot 2026-11-26 at 20.31.58.png]]![[Screenshot 2026-11-26 at 20.32.29.png]]

### Homophily
- closes triangles - more clustering, sharper modules and hubs.
- Human functional connectomes.
- We can use this to build 
- parameters reproduce altered brain connectivity under neuropsychiatric conditions.
- RNNs, we can penalise by it length of connection. makes RNN more modular and small world, and causes **functional segregation** - each sector does a function

## Hub nodes
Both are modular, but right one, the connections between modules only involve a small number of nodes.
![[Screenshot 2026-11-26 at 20.39.15.png]]
![[Screenshot 2026-11-26 at 20.39.59.png]]
Pi = 0 if all of i's edges in one community, and grows if they spread across more communities.
Node i is connector hub if:
- degree ki is above the mean degree (including within community) plus one standard deviation
- participation index Pi is above a threshold (usually 0.3)

### Connective core - connector hubs of a modular network, together with connections between them.
- Human brain is modular, has hubs, and is a rich club - they are more densely connected to each other than their high degrees alone would predict.
- Birds also have connective core. (good theory not just apply to humans)

# Hierarchical modularity:
![[Screenshot 2026-11-26 at 20.48.42.png]]