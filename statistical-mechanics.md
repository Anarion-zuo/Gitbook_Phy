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
The experiment of observation is the ideal gas expansion experiment. The experiment shows that with no external work done upon the system and no heat exchange allowed, the temperature of the system does not change, no matter how the pressure and volume of the system may change. Therefore, the internal energy of the system is a function with respect to temperature.

By the definition of temperature, $pV\propto T$. If we look at the difference between the process of keeping volume or pressure constant:
$$
C_p-C_V=\frac{pV}{T}\propto N
$$

#### Second Law

As we have known that there is: $dW=\sum_iJ_idx_i$, there must be some formula of similar form for $Q$.

No process is possible whose so result is to complete conversion from heat to work. There is no ideal engine.

Clausius’s Theorem:

- For any cyclic process, the following is always true at any moment:

$$
\oint\frac{dQ(s)}{T(s)}\le0
$$

where $dQ$ is the amount of heat flowing into the system at the moment of temperature $T(s)$ and $s$ represents some state. A cyclic process is a process in which many things may change and in the end comes back to the original state.

### Carnot Engine

A Carnot engine is any engine that is

1. Reversible: Can go forward/backward by reversing input/output.
2. Operating in cycle: Start and end points are the same.
3. All heat input/output at 2 temperatures: Defined at 2 different temperature layer $T_H,T_C$.

![1557921893322](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557921893322.png)

#### Ideal Gas Carnot Cycle

![1557922053282](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557922053282.png)

$BC\&DA$ is a adiabatic path without any exchange of heat and quasi-static. There is $dE=dW=pdV$. We may have:
$$
pV^\gamma=const
$$
There is a theorem saying that Of all engines operating only between temperature $T_H,T_C$, the Carnot engine is the most sufficient. The proof is as following.

![1557922543475](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557922543475.png)

Suppose there is another engine better than Carnot’s. Connect is with another Carnot engine working backward between $T_H$ and $T_C$, transferring work of $W$. The input and output are as $Q_H'-Q_H$ and $Q_C'-Q_C$. According to the second law, we have $Q_H'>Q_H$, for the temperature of $T_H$ is higher. Therefore:
$$
\eta_{non-C}\frac{W}{Q_H'}\le\frac{W}{Q_H}=\eta_{C}
$$
The efficiency of any other engine is less that or equal to the efficiency of Carnot engine.

By the same idea, we can also find that All Carnot engines operating between $T_H,T_C$ have the same efficiency. We can let one Carnot engine work on anther and do it backward and have a pair of inequalities which leads to an equality. Therefore, for a pair of given $T_H,T_C$, we can have a certain value of the efficiency.
$$
\eta_{C}=\eta(T_H,T_C)
$$
We hereby give the thermal dynamic’s temperature scale.

#### Some Properties of Thermal Dynamic’s Scale

We put together 2 Carnot’s engine, doing work $W_{12},W_{23}$.

![1557924474825](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557924474825.png)

The whole thing is equivalent to another Carnot engine, doing work $W_{13}$.

![1557924558308](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557924558308.png)

For engine 1:
$$
Q_2=Q_1-W_{12}=Q_1(1-\eta(T_1,T_2))
$$
For engine 2:
$$
Q_3=Q_2-W_{23}=Q_2(1-\eta(T_2,T_3))=Q_1(1-\eta(T_1,T_2))(1-\eta(T_2,T_3))
$$
For the engine combined:
$$
Q_3=Q_1-W_{13}=Q_1(1-\eta(T-1,T_3))
$$
Conclusion:
$$
1-\eta(T_1,T_3)=(1-\eta(T_1,T_2))(1-\eta(T_2,T_3))
$$
By definition:
$$
1-\eta(T_1,T_2)=\frac{1-\eta(T_1,T_3)}{1-\eta(T_2,T_3)}=\frac{Q_2}{Q_1}
$$
The thermal dynamic scale is defined to be:
$$
\frac{Q_2}{Q_1}=\frac{T_2}{T_1}
$$
This defines the ratio, therefore still requires a reference state.

For any engine:
$$
\eta=1-\frac{Q_C}{Q_H}\le\eta_{CE}(T_H,T_C)=1-\frac{T_C}{T_H}\Rightarrow \frac{Q_H}{T_H}+\frac{-Q_C}{T_C}\le0
$$

#### Clausius’ Theorem

For any cyclic process, 

![1557925929084](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557925929084.png)

the heat goes into the system at a certain state $Q_{(s)}$, there is:
$$
\oint\frac{dQ(s)}{T(s)}\le0
$$
which is a general case of the formula above. $Q(s)$ is the heat delivered to the system at temperature $T(s)$.

![1557926658439](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557926658439.png)

Take a Carnot engine extracting heat from some substance with constant temperature $T_0$ and deliver the output heat to the cyclic system. When we are putting heat into the cycle, the temperature of our substance may not be the same as the temperature it holds at the heat source. Therefore, we consider this intermediate process for the convenience of describing the process of transferring heat.

The heat extracted from the source at a cycle is:
$$
\oint dQ_0(s)=\oint T_0dQ(s)/T(s)\le0\Rightarrow\oint\frac{dQ(s)}{T(s)}\le0
$$
for $dQ_0(s)\le0$, or we can get some heat out of some bath and set out a car.

#### Reversible Processes

A reversible process is a process with each state equilibrium. We demand the Carnot engine to deliver the temperature precisely at each of the tiny states of the cyclic reversible process, which for each of them is equilibrium.

![1557927262192](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557927262192.png)

Solid line for equilibrium/reversible.

According to Clausius’ theorem, we must have the less-or-equal-to-0 inequality for both directions of the cycle. Therefore, in the case of reversible process,
$$
\oint\frac{dQ(s)}{T(s)}=0
$$

##### Path Independence

![1557927662483](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557927662483.png)

For any 2 points A and B,
$$
\int_A^B\frac{dQ^{(1)}_{rev}}{T^{(1)}}=\int_A^B\frac{dQ^{(2)}_{rev}}{T^{(2)}}
$$
The different paths of integral ultimately have the same result. An it should be the same for any other path between the 2 points. The result only depends on the initial and final state, which is the definition of entropy.
$$
\int_A^B\frac{dQ^{(i)}_{rev}}{T^{(i)}}=S(B)-S(A)
$$

##### Energy

For a reversible transformation,
$$
dQ=TdS,dE=\sum_iJ_idx_i+TdS
$$
For $n$ ways doing work to the system, $dW=\sum_i^nJ_idx_i$, there is $(n+1)$ independent variables describing the system, $J_1,...,J_n,T$.

Rearrange the expression and have the definition of entropy:
$$
dS=\frac{dE}{T}-\frac{\sum_iJ_i}{T}dx_i\Rightarrow S(E,x),\frac{1}{T}=\frac{\partial S}{\partial E}|_{x},\frac{J_i}{T}=-\frac{\partial S}{\partial x_i}|_{E,x_{j\ne i}}
$$
All other factors are given by the derivatives of $E$ and $x$.

#### Irreversible Transformation

$$
dQ\le TdS
$$

When there is no heat exchanged, the process must be increasing entropy.

#### Enthalpy

Some total energy can be defined for a spring system.
$$
H=\frac{1}{2}kx^2-Jx
$$
When the total energy is not changing, $dH/dx=0$:
$$
H_{eq}=-\frac{J^2}{2k}
$$
When there is some friction, and $J$ is not changing, because of friction,
$$
dW\le J_idx_i=d(J_ix_i)
$$
When there is no heat exchanged,
$$
dE\le d(J_ix_i)
$$
The change in $E-J_ix_i$ is less than or equal to 0.

The enthalpy is defined to be:
$$
dH=dE-d(J_ix_i)=J_idx_i+TdS-J_idx_i-x_idJ_i=TdS-x_idJ_i
$$
By partial derivative,
$$
x_i=-(\frac{\partial H}{\partial J_i})_S
$$

#### Isothermal Condition

At constant temperature,
$$
dQ\ne0,dW=0
$$
According to Clausius’ theorem,
$$
dQ\le TdS=d(TS),dE\le d(TS)
$$
We can define another thermal dynamics variable F Free Energy:
$$
F=E-TS,dF=dE-TdS-SdT=J_idx_i-SdT\le0,S=-\frac{\partial F}{\partial T}
$$

#### Gibbs Free Energy

Isothermal constant $J$:
$$
dQ\le TdS,dW\le J_idx_i,dE\le TdS+J_idx_i=d(TS+J_ix_i)
$$
Definition:
$$
G=E-TS-J_ix_i,dG=-SdT-x_idJ_i
$$

#### Chemical Work

For each particle in the system, it may have chemical reaction with others. The energy generated by the chemical reaction is proportionate to the number of particles. Therefore, we can define the chemical work to be:
$$
dW_{chem}=\mu dN
$$
while the mechanic work is still:
$$
dW_{mech}=Jdx
$$
For the parts taking different amount of mechanic work and different type of chemical reactions:
$$
dW_{chem}=\sum_\alpha\mu_\alpha dN_\alpha,dW_{mech}=\sum_iJ_idx_i
$$

### Grand Equilibrium State Equation

The state of the system is defined by 3 independent variables, $T,J_i,N_\alpha$.
$$
dE=TdS+\sum_iJ_idx_i+\sum_\alpha\mu_\alpha dN_\alpha
$$

Other fashions:
$$
dS(E,x,N)=\frac{dE}{T}-\frac{J_idx_i}{T}-\frac{\mu_\alpha dN_\alpha}{T},d(T-TS)=-SdT+J_idx_i+\mu_\alpha dN_\alpha
$$


#### Grand Potential

$$
g=E-TS-\mu_\alpha N_\alpha,dg=-SdT+\sum_iJ_idx_i-\sum_\alpha N_\alpha d\mu_\alpha
$$

The grand potential function is defined by 3 independent variables $T,\mu_\alpha,x_i$.

#### Extensibility

It is obvious that:
$$
E(\lambda S,\lambda x,\lambda N)=\lambda E(S,x,N)
$$
Take derivative with respect to $\lambda$:
$$
\frac{dE}{d\lambda}|_{\lambda=1}=\frac{\partial E}{\partial S}|_{x,N}S+x_i\frac{\partial E}{\partial x_i}|_{S,N}+N_\alpha\frac{\partial E}{\partial N_\alpha}|_{x,S}=TS+J_ix_i+\mu_\alpha N_\alpha=E(S,x,N)
$$
Take the derivative of both sides:
$$
dE=TdS+SdT+J_idx_i+x_idJ_i+\mu_\alpha dN_\alpha+N_\alpha d\mu_\alpha\Rightarrow SdT+\sum_ix_idJ_i+\sum_\alpha N_\alpha d\mu_\alpha=0
$$
This is the Gibbs-Duhem relation. It is shown that variables $T,J_i,\mu_\alpha$ is dependent with each other by this formula.

#### Isothermal Condition

For general gas,
$$
dT=0,d\mu=\frac{V}{N}dp
$$
For ideal gas:
$$
d\mu=\frac{k_BT}{p}dp,\mu(T,p)=\mu_0+k_BT\ln p
$$

#### Maxwell Relation

A property of a function of state:
$$
\frac{\partial^2f}{\partial x\partial y}=\frac{\partial^2f}{\partial y\partial x}
$$
For systems with fixed number of particles, $dN=0$:
$$
dE=TdS+J_idx_i,T=\frac{\partial E}{\partial S}|_x,J_i=\frac{\partial E}{\partial x_i}|_{S,x_i\ne x_j}
$$
then:
$$
\frac{\partial T}{\partial x_i}|_S=\frac{\partial J_i}{\partial S}|_x,\frac{\partial x_i}{\partial T}|_S=\frac{\partial S}{\partial J_i}|_x
$$
This provides a way of solving problems of such kind as compute $\frac{\partial S}{\partial J_i}|_T$. We construct the function into a form such that $S$ is the first derivative of some function of state. By observation:
$$
d(E-TS-J_ix_i)=TdS+J_idx_i-TdS-SdT-J_idx_i-x_idJ_i=-SdT-x_idJ_i
$$
According to Maxwell relation:
$$
\frac{\partial S}{\partial J_i}|_T=\frac{\partial x_i}{\partial T}|_J
$$

### Stability Conditions

For the case of any system, thermal or mechanical, we defined a function $H$ for it, representing energy:
$$
H=\phi(x)-Jx
$$
The optimization solution is:
$$
J=\frac{\partial \phi}{\partial x}
$$
If the shape of the potential energy is given, which is convex:
$$
\frac{\partial^2\phi}{\partial x^2}>0
$$
If $x$ is a vector, or we have multiple variables here, the Hessian matrix of $H$ is positive definite.
$$
\sum_{i,j}\frac{\partial^2\phi}{\partial x_i\partial x_j}\delta x_i\delta x_j\ge0
$$
When the force is known:
$$
J_i=\frac{\partial \phi}{\partial x_i}
$$
If there is some change in $J$:
$$
\delta J_i=\sum_j\frac{\partial^2\phi}{\partial x_i\partial x_j}\delta x_j
$$
Therefore, for any force, the work:
$$
\sum_i\delta x_i\delta J_i\ge0
$$
Apply the same idea to thermal systems. In order to have the system at equilibrium, there has to be:
$$
\delta T\delta S+\sum_i\delta J_i\delta x_i+\sum_\alpha\delta\mu_\alpha\delta N_\alpha\ge0
$$

#### Entropy Inequality

$$
dE=TdS+\sum_iJ_idx_i
$$

Stability condition:
$$
\delta T\delta S+\sum_i\delta J_i\delta x_i\ge0
$$
Change in emtropy:
$$
\delta S=\frac{\partial S}{\partial T}|_x\delta T+\sum_{i,j}\frac{\partial S}{\partial x_i}|_{T,x_i\ne x_j}\delta x_i
$$
Plug in:
$$
\frac{\partial S}{\partial T}|_x(\delta T)^2+\sum_i(\delta T)(\delta x_i)(\frac{\partial S}{\partial x_i}|_T+\frac{\partial J_i}{\partial T}|_x)+\sum_{i,j}\delta x_i\delta x_j\frac{\partial J_i}{\partial x_j}|_T\ge0
$$
Maxwell relation:
$$
d(E-TS)=-SdT+\sum_iJ_idx_i\Rightarrow\frac{\partial(-S)}{\partial x_i}|_T=\sum_i\frac{\partial J_i}{\partial T}|_x
$$
Plug in:
$$
\frac{\partial S}{\partial T}|_x(\delta T)^2+\sum_{i,j}\delta x_i\delta x_j\frac{\partial J_i}{\partial x_j}|_T\ge0
$$
Fixed $x_i$:
$$
\frac{\partial S}{\partial T}|_{x}\ge0
$$
Entropy should always be an increasing function of temperature at constant displacement. The heat capacity at constant displacement is also be positive.
$$
C_x=\frac{dQ_x}{dT}=T\frac{\partial S}{\partial T}|_x\ge0
$$
Fixed temperature:
$$
\sum_{i,j}\frac{\partial J_i}{\partial x_j}|_T\delta x_i\delta x_j\ge0
$$
Matrix form:
$$
\begin{pmatrix}\delta x_1&\delta x_2&...\end{pmatrix}\begin{pmatrix}
\frac{\partial J_i}{\partial x_j}
\end{pmatrix}\begin{pmatrix}\delta x_1\\\delta x_2\\\vdots\end{pmatrix}
$$
The matrix must be positive definite.

### The Third Law

For 2 different states represented by $x_1, x_2$, if we go along some reversible process, we would have some measurement of emtropy:
$$
\int_{x_1}^{x_2}\frac{dQ_{rev}|_T}{T}=S(x_2,T)-S(x_1,T)
$$
The observation of Nernst is that, as temperature gets lower, the difference in entropy between the 2 states goes to 0.
$$
\lim_{T\rightarrow0}\Delta_{x_1\rightarrow x_2}S(T)=0
$$
This leads to a more ambitious statement of the third law, which is the entropy of all substance at 0 temperature is the same universal constant, set to 0.

#### Mathematical Consequences

$$
\lim_{T\rightarrow0}S(X,T)=0,\lim_{T\rightarrow0}\frac{\partial S}{\partial X}|_T=0
$$

Extensibility:
$$
\alpha=\frac{1}{x}\frac{\partial x}{\partial T}|_J=\frac{1}{x}\frac{\partial S}{\partial J}|_T,\lim_{T\rightarrow0}\alpha=0
$$
Heat capacity:
$$
S(T,X)-S(0,X)=\int_0^T\frac{C_x^{(T)}dT}T
$$
As $T$ approaches 0, the heat capacity has to go to 0, for the integral has to be convergent.

## Probability

### Gaussian

Single variable:
$$
p(x)=\frac{1}{\sqrt{2\pi\sigma^2}}\exp(-\frac{(x-\lambda)^2}{2\sigma^2})
$$
Characteristic function:
$$
\tilde p(k)=\exp(-ik\lambda-\frac{1}{2}k^2\sigma^2)\int\frac{dz}{\sqrt{2\pi\sigma^2}}\exp(-\frac{z^2}{2\sigma^2}),z=x-\lambda+ik\sigma^2
$$
