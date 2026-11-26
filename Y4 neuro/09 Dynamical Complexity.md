- structure and dynamics
	- how does wiring of a network neurons shape its activity?

Start with 800 excitatory neurons, ring lattice, rewired with probability p.
- if we fire from both sides, they annihilate when they meet each other.
![[Screenshot 2026-11-26 at 21.32.41.png]]
### p = 0.01
- small world, activity is self sustained: long range regions reignite dead regions
![[Screenshot 2026-11-26 at 21.33.05.png]]
Higher p, no regular pattern. chaotic activity.
![[Screenshot 2026-11-26 at 21.33.37.png]]

Higher p, activity sweeps through system in bursts.

Modular neurons setup:
- Eight modules of 100 excitatory neurons each, plus pool of 200 inhibitory neurons.
- Each module has 1000 random one-way excitatory to excitatory connections![[Screenshot 2026-11-26 at 21.36.28.png]]
![[Screenshot 2026-11-26 at 21.38.00.png]]
![[Screenshot 2026-11-26 at 21.40.03.png]]![[Screenshot 2026-11-26 at 21.44.30.png]]

Where between p=0 and p=1 is most interesting?

### Dynamical complexity
 - system is dynamically complex if its parts are both segregated (each does something different) and integrated (act together as whole).
 - Complexity is not a property of any single neuron or module, but of how the parts relate to each other and to the whole.
 - Too integrated: every part does the same thing, so the whole is no richer than one part. 
 - Too segregated: every pat does its own thing, so the whole is just the sum of its parts

## Criticality
- system is critical when it sits at a critical point. value of a control parameter where its behaviour changes qualitatively.
- In large systems, critical point is often phase transition between order and disorder.
- Critical systems are characterised by occasional very large events, often distributed as a power law.
- If systems statistics follow a power law, it may be at criticality.![[Screenshot 2026-11-26 at 22.17.24.png]]

### Model of avalanches
![[Screenshot 2026-11-26 at 22.18.27.png]]
sigma = 1, critical point.
