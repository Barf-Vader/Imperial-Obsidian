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

