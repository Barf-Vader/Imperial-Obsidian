Food sources lie at exact same distance away. Robot with simple Braitenberg controller would go straight through.

![[Screenshot 2026-11-03 at 16.48.44.png]]
both are stimulated, it will go straight. 

## Lateral inhibition
![[Screenshot 2026-11-03 at 17.10.38.png]]
Neurons inhibit their neighbours. lateral inhibition. red arrow with circle is inhibition neuron. Each neuron's activity is reduced by neighbour's activity. strongly driven neurons suppress weakly driven ones. 
![[Screenshot 2026-11-03 at 17.21.33.png]]

### Winner-takes-all WTA
- competing populations suppress each other, so that only one of them, the winner, stays active.
- **bistable** - one competitor is active, other is silent. two stable states. both being active is unstable.
- ![[Screenshot 2026-11-03 at 17.25.55.png]]
- for this to work neurons must recover quickly after a spike. a = 0.2 for all neurons instead of 0.02, which is unrealistic. because it has to keep firing to suppress

## Spiking networks (how real neurons communicate, with spikes)
- hard to analyse, so we consider the population as a whole.
- r(t) is fraction of population's neurons that fire in a short time window `τ` around t.
- from one `τ` to the next:
	- neurons that firing now become refractory: -r(t)
	- neurons firing next are driven by input: on avg f(I), the F-I curve f(.).![[Screenshot 2026-11-05 at 14.53.10.png]]
![[Screenshot 2026-11-05 at 15.04.09.png]]
Note here, we are assuming `τ` is equaivalent to recovery period.![[Screenshot 2026-11-05 at 15.05.58.png]]
- smoothness - how noisy, or how heterogeneous the population is.
- for now, any curve with roughly the same shape will do - sigmoid function.
- ![[Pasted image 20261105150929.png]]
- Note that inhibition from competing populations add negative current to the total current given to a population.
- ![[Screenshot 2026-11-05 at 15.12.42.png]]
- Strong inhibition - stable fixed point splits into two.

## Attractors
