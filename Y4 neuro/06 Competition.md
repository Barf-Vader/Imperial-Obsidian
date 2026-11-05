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