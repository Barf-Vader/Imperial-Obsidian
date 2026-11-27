What could we do with it?
- Predict how they respond to treatment
- use to plan surgery
- find out why people have different cognitive capabilities

## Virtual Brain Twins
- A model fitted to data of one person
- We can perturb the model in ways that would be impossible in the person. 
- To simulate human brain we need more neurons.

# From populations to oscillations
each population has both excitatory and inhibitory neurons.
![[Screenshot 2026-11-27 at 17.17.13.png]]
- We need one rate equation for each.
- Neural mass model, a whole population is treated as a single point with no spatial extent.
- ![[Screenshot 2026-11-27 at 17.23.02.png]]

## Limit cycles
Closed loop in state space that nearby trajectories approach. Whatever the start, the system oscillates with the same amplitude and frequency.

## Kuramoto oscillators
![[Screenshot 2026-11-27 at 17.28.04.png]]
The simplest model for coupled oscillators is kuramoto model
The only thing which changes when a system is on a limit cycle is the phase![[Screenshot 2026-11-27 at 17.31.03.png]]
Used to calculate the rate of change of an oscillator in a network of oscillators, where each one is trying to pull neighbouring oscillators to its phase.

## Chimeras and Metastability
![[Screenshot 2026-11-27 at 17.39.43.png]]
Consider this. each system is eight communities, each with 32 identical phase lagged kuramoto oscillators. All to all connectivity within each community. this a modular small world network. Each oscillator has 32 connections to other communities, chosen at random and slightly weaker.

- In real brains synchronisation waxes and wanes over time.
- The coexistence of order and disorder in a system of identical parts is called a chimera state.

## Metastability
- Chimera states do not stay put - they come and go in irregular patterns. networks lingers in one pattern, then moves to next. This is metastability.![[Screenshot 2026-11-27 at 17.48.16.png]]
The synchrony is the order parameter, where 1 is perfect sync and 0 is completely scattered.