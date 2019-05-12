# Statistical Mechanics

## Thermal Dynamics

### Definition

Thermal dynamics is a phenomenological description of equilibrium properties of macroscopic systems.

*System*: A place where we can isolate the substances adiabatically, which means it does not allow heat transferring.

*Equilibrium*: It is when properties do not change any more.

*Properties*: Volume, Pressure, …

*Phenomenology*: Observe and construct laws of thermal dynamics.

#### 0th Law

If the 2 systems A, B are separately in equilibrium with C, they are equilibrium with each other.

A and C, B and C are able to exchange heat with each other, which A and B are adiabatically separated from each other. If the equilibrium is achieved between AC and BC, letting AB exchange heat freely would not change the state. The phenomenon implies the existence of some empirical temperature.

There must be some function relating A, B and C.
$$
f_{AC}(A_1,A_2,...;C_1,C_2,...)=0,f_{BC}(B_1,B_2,...;C_1,C_2,...)=0
$$
where the letters with subscribes stand for some coordinate. Rewrite this in another form:
$$
F_{BC}(...)=C_1=F_{AC}(...)
$$
Thus, relates A and B. Choose a particular reference frame C and we would have direct relation between A and B.
$$
\Theta_A(A_1,A_2,...)=\Theta_B(B_1,B_2,...)
$$

#### Ideal Gas Scale

Ideal state of a gas is defined to be:
$$
\lim_{V\rightarrow\infty\\p\rightarrow0}pV=const
$$
The gas satisfying such state is a ideal gas.

#### First Law

The law says the work done upon the adiabatic system can be precisely computed by the former and latter inner energy of the system.

The interesting part of the law is when we violate the condition of adiabatic and allow heat exchange to happen. Thus, we may define *heat* as the energy difference between the adiabatic condition and the not adiabatic condition.
$$
\Delta Q=(E_f-E_i)-\Delta W
$$
In the differential form:
$$
dE(\vec x)=dW+dQ
$$

where $\vec x$ depends on the initial and final state and the right hand side may depend on the path of the process. We can idealize the process so that the change in the system is slow and maintain equilibrium and the state is called *quasi-static*.

The mechanical work can be defined as the sum of the integral of the mechanic forces with respect to displacement.
$$
dW=\sum_iJ_idx_i
$$
Heat is harder to describe. We may describe it as the way of the change of temperature. It is also path-dependent.
$$
C_{path}=\frac{dQ}{dT}
$$
The way of adding heat to the system, keeping volume or pressure constant. Each process is measured under the corresponding condition.
$$
C_V=\frac{dQ_V}{dT}=\frac{dE+pdV}{dT}=(\frac{\partial E}{\partial T})_V,C_p=\frac{dQ_p}{dT}=\frac{dE+pdV_p}{dT}=(\frac{\partial E}{\partial T})_p+(\frac{\partial V}{\partial T})_p
$$
The experiment of observation is the ideal gas expansion experiment. The experiment shows that with no external work done upon the system and no heat exchange allowed, the temperature of the system does not change, no matter how the pressure and volume of the system may change. Therefore, the internal energy of the system is a function to temperature.

By the definition of temperature, $pV\propto T$. If we look at the difference between the process of keeping volume or pressure constant:
$$
C_p-C_V=\frac{pV}{T}\propto N
$$
