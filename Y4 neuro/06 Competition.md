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
- Weak inhibition - not strong enough to kill one population.

## Attractors
A state that the system moves towards from all nearby states. Set of states which ends up there is called the **basin of attraction**.
- with strong inhibition, each winner is an attractor.
- ![[Pasted image 20261105152854.png]]
- note to get the first equation, we subtract the two equations above. then use taylor expansion.
- **Pitchfork bifurcation** - as w crosses wc, one fixed point splits into three.
- We can think of this activity as a ball in a landscape.![[Screenshot 2026-11-05 at 15.46.04.png]]

#### self-exicitation
- we add `α`, self-excitation within each population:
- ![[Screenshot 2026-11-05 at 15.48.33.png]]
- Hopefield networkes store many memories as attractors in the same way.

### Decision making
- Classic task - net motion of cloud of dots left or right. Only a fraction of dots (coherence) move together, rest moves randomly.
- Press key to report direction. lower coherence, more mistakes and slower.
- Simulating with our model:
	- fewer neurons, neither competitors dominate for long.
	- sustained victory needs enough ongoing inhibitory firing to shut out rival.
	- firing is stochastic, and the fewer the neurons the larger the fluctuations.
	- in small network, inhibition sometimes dips far enough for the rival to start firing, and winner can swap over.
	- identical input, then winner swaps irregularly.

### Psychometric curve
- Probability of a choice as a function of strength of the evidence for it, typically S-shaped curve.
![[Screenshot 2026-11-05 at 16.04.21.png]]
larger temp, meaning takes more stimuli to make decision.

### reaction time
- first moment one population wins.
- The harder the choice the slower the decision.![[Screenshot 2026-11-05 at 16.13.24.png]]
- Same as humans.
![[Screenshot 2026-11-05 at 16.15.10.png]]
we do the same to braitenberg vehicles. note a population is usually defined as a group of same type of neurons, therefore we need two groups of inhibitory neurons, because motor neurons are excitatory neurons.
### In AI:
- psychometric curve plays the role of a softmax function.

## Periodic effect
- to obtain WTA, we used a high a. if we keep usual values of a for excitatory and inhibitory neurons, we get oscillatory behaviour. neither competotor can win. one population fires when the other one doesn't.

### Binocular rivalry
- examples on sensory side. 
- each eye is shown different image, two competes.
- we might expect people to see a blend of two images.
- however, most report one image dominates, switches between the two. just like oscillation.