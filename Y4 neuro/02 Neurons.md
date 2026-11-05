## Artificial neuron
an artificial neuron computes a weighted sum of inputs xi, and passes it through a nonlinear function f.
![[Screenshot 2026-10-27 at 16.29.07.png]]
- Output of artificial is real number, real neuron outputs train of spikes.
- Time - no time. Real, continuous time dynamics.
- State - none vs a lot
- Inputs - weighted sum vs dendritic tree.
- Connections - Any sign, vs excitatory or inhibitory
- ![[Screenshot 2026-10-27 at 16.38.54.png]]

## Complexity of single neuron
- without dendritic NMDA receptors, one layer is enough, with them, 5-8 layers

# Real neurons
- Three parts, cell body, tree of dendrites, and an axon.
- dendrites carry electrical signals, axon delivers neuron's electrical input.
- Long axons are covered in a myelin sheath, which increases the speed of electrical conduction
- ![[Screenshot 2026-10-27 at 16.43.51.png]]

- Human cerebral cortex contains 20 billion neurons, 6 layers.
- Dendrites tree is very wide.
- single neuron can project to as many as 10,000 neurons.
- Synapses are gaps between axon and dendrites
	- big soup of electrically significal chemicals in the synaptic cleft. neurotransmitters, including serotonin, dopamie and adrenaline.
	- HIGE SIMPLICICATION - simple weighted connections. weighted sums.

# two types of neurons
- Excitatory -increase activity of neurons they are connected to.
- Inhibitory - neurons decrease activity they are connected to. 

they are either or, but cannot be both. Simplified form of Dale's principle.

## Behavior
- receives and transmits electrical pulses, or spikes.
- incoming spikes travel along neuron dendrites, cause charge to build up in body of neuron. when charge reaches a threshold, neuron fires, and sends spike along axon,
- ![[Pasted image 20261102134704.png]]

baseline at 0 or -65
## computer model 
membrane potential (v) exhibits characteristic spiky profile thanks to interplay of three currents.
![[Screenshot 2026-11-02 at 13.56.43.png]]![[Screenshot 2026-11-02 at 13.58.23.png]]
Dont need to know by heart 
m,n,h are all differential equations.

Neurons are binary - exact height doenst count.