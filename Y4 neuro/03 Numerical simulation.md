Given mathematical model of neuron behaviour expressed as set of ordinary differential equations, we can use numerical methods to simulate neuron's temporal dynamics. 

Hodgkin-Huxely is computationally expensive.

## initial value problem
- given ODE ordinary differential equation of form,
![[Screenshot 2026-11-02 at 14.14.02.png]]
and initial value y, compute value of y as it changes over time.

For most ODEs, we cant do this with pen and paper. we do this iteratively.

### Euler method
![[Screenshot 2026-11-02 at 14.15.10.png]]
y(t) - value of y at time t. very sensitive to delta t. 
Smaller step size. closer we get to the exact solution.

### Rugne Kutta
given y(t), we can approximate the value of y(t + dt) using 4th order RK by computing:
![[Screenshot 2026-11-02 at 14.19.26.png]]

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