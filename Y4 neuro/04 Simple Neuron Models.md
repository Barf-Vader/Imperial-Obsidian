![[Screenshot 2026-11-02 at 18.03.48.png]]![[Screenshot 2026-11-02 at 18.03.37.png]]### Integrate and fire neurons

### 1D neuron models
- low-dimensional models - 
![[Screenshot 2026-11-02 at 15.08.46.png]]
t is neuron timescale, and I is dendritic current (input)
- these are often expanded with a fixed voltage threshold phi that triggers a spike and reset.
- For given current I, solution to following equation gives steady state voltage.
- ![[Screenshot 2026-11-02 at 15.14.53.png]]
- Activation function.

### Integrate and fire neurons
- Hodgkin-Huxley is biologically accurate. but computationally expensive.
- Opposite end of spectrum - leaky integrate and fire (LIF), which is computationally inexpensive.
- ![[Screenshot 2026-11-02 at 15.22.31.png]]
- If I = 0, v will drift exponentially to vr.
- In HH model, voltage was relative to rest (0 mv). **from now we use absolute potential -65mV**
- #### sub-threshold
	- dynamics of sodium and potassium currents are approximated by the vr-v term. 
	- the detailed dynamics of the spike itself are ignored. 
	- When we reach the membrane potential, we record a spike and explicitly reset the neuron. v > phi then v <- vr.
	- good value for phi is -50 mV
	- Instant value of Dirac spike can be inserted just for looks.
	- ![[Screenshot 2026-11-02 at 15.46.50.png]]
#### Leakage
- in absence of dendirtic current, drift back down to resting value.![[Screenshot 2026-11-02 at 16.03.45.png]]
- simple integrate and fire model has no refractory period
- to overcome this, we force **absolute refractory period** alpha. absolute bc no matter what current, it will not fire.
- ![[Screenshot 2026-11-02 at 16.06.25.png]]

## Quadratic integrate and fire
- ![[Screenshot 2026-11-02 at 16.10.54.png]]
- ![[Screenshot 2026-11-02 at 16.12.16.png]]
- When I = 0, v decays to resting if below vc, otherwise increases quickly until neuron fires.
- QIF neuron is 1D **dyanimcal system**.
- if we plot dv/dt against v we get:
- these two points are fixed points, where those equations = 0. stable is nearby trajectories move towards it, unstable if it moves away.![[Screenshot 2026-11-02 at 17.20.46.png]]
- Increase input current I shifts curves upwards.
- When the points merge, thats called bifurcation. when I = Ic.
- Above Ic, we reset, because the neuron fires

## Izhikevich neurons
- good compromise between computation efficiency and realism.
- ![[Screenshot 2026-11-02 at 17.34.41.png]]
- v is quad, a to d are constants we can choose.
- State of system with two vars is gicen by a point in a phase plane.
- at every point, the equations give a direction of motion.
- **Nullcline** - curve where one var stops changing.![[Screenshot 2026-11-02 at 17.42.56.png]]
- fixed points are where they cross.
- when I is uncreased we move curve up.
- when nullclines dont touch then it fires.![[Screenshot 2026-11-02 at 17.45.29.png]]
- u makes it harder for neuron to spike, when it has just spiked, soft refractory period.

### Excitatory
![[Screenshot 2026-11-02 at 18.04.01.png]]
![[Screenshot 2026-11-02 at 18.24.08.png]]
## AdEX model
we have exponential instead of quadtratic. If we feed constant current, it spikes a bit faster at the start, but slows down over down. spike-frequency adaptation.![[Screenshot 2026-11-02 at 18.27.36.png]]

![[Screenshot 2026-11-02 at 18.26.30.png]]