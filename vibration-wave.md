# Vibration & Wave

## Harmonic

### Free

$$
\ddot x(t)=-w^2x,w=\frac{k}{m}
$$

The solution is:
$$
x(t)=a\cos wt+b\sin wt
$$
This is the only solution.

Although Hook’s law does not apply everywhere in the universe, for all systems, there is always a Taylor expansion for its potential energy such that:
$$
V(x)=V(0)+xV'(0)+\frac{1}{2}x^2V''(0)+O(x^3)
$$
As $V'(0)=0,V''(0)$:
$$
F(x)=-\frac{d}{dx}V(x)=-V''(0)x+O(x^2)
$$
As $x$ is small enough, the Hook’s law is going to apply everywhere.

The equation of motion $\ddot x+w^2x=0$ has the following properties:

1. $x_{12}(t)=x_1(t)+x_2(t)$ is also a solution.
2. Time translation invariance: $x(t+a)$ is also a solution.

Energy:
$$
V(x)=\frac{1}{2}Kx^2,T(\dot x)=\frac{1}{2}M\dot x^2,H=V+T=\frac{1}{2}Kx^2+\frac{1}{2}M\dot x^2
$$
Plug in time:
$$
H=\frac{1}{2}MA^22_0^2\sin^2(w_0t+\phi)+\frac{1}{2}KA^2\cos^2(w_0t+\phi)=\frac{1}{2}KA^2
$$


### Damped

$$
\ddot x+\Gamma\dot x+w_0^2x=0,x=Re(z(t)),z(t)=e^{i\alpha t},\alpha=\frac{i\Gamma}{2}\pm\sqrt{w_0^2-\frac{\Gamma^2}{4}}
$$

When $w_0^2>\frac{\Gamma^2}{4}$, the drag force is not hard.

Define:
$$
w^2=w_0^2-\frac{\Gamma^2}{4},z_+(t)=e^{-\Gamma t/2}e^{iwt},z_-(t)=e^{-\Gamma t/2}e^{-iwt},x(t)=e^{\Gamma t/2}[a\cos wt+b\sin wt]
$$
The amplitude of the oscillation would be decreasing exponentially, and the frequency would be damped constantly.

When there is a critical value, $w_0^2=\frac{\Gamma^2}{4}$, the system can actually stop the oscillation.
$$
x_+(t)=e^{-\Gamma t/2},\frac{x_-(t)}{w}=te^{-\Gamma t/2}
$$
The mass would only “pass” 0 for only 1 time, or never pass, as doors closing just in place.

When the drag force is large, $w_0<\frac{\Gamma^2}{4}$, the system is over-damped.
$$
\alpha=i(\frac{\Gamma}{2}\pm\sqrt{\frac{\Gamma^2}{4}-w_0^2}),w_\pm=\frac{\Gamma}{2}\pm\sqrt{\frac{\Gamma^2}{4}-w_0^2}
$$
The system has no more oscillation once reaches the balanced position.

![1560731639794](assets/1560731639794.png)
$$
Q=\frac{w_0}{\Gamma},\beta=\sqrt{\frac{\Gamma^2}{4}-w_0^2}
$$

### Driven

$$
\ddot x+\Gamma\dot x+w_0^2x=f_0\cos w_dt
$$

The amplitude of the oscillation:
$$
A(w_d)=\frac{f_0}{\sqrt{(w_0^2-w_d^2)^2+w_d^2\Gamma^2}}
$$
When $w_d=w_0$, the amplitude would be large, for the damping is usually small.

The phase difference of the oscillation:
$$
\tan\delta(w_d)=\frac{\Gamma w_d}{w_0^2-w_d^2}
$$
Particular solution:
$$
x_p(t)=A(w_d)\cos(w_dt-\delta(w_d))
$$
Combine the homogeneous solution:
$$
x(t)=A(w_d)\cos(w_dt-\delta(w_d))+Be^{-\Gamma t/2}\cos(wt+\alpha)
$$
where $B,\alpha$ are free parameter, determined by the initial conditions.

- $w_0$: natural frequency.
- $w$: damped frequency.
- $w_d$: driven frequency.

One of the term ultimately dies out and we have a static solution, apart from the transient solution.

### Coupled

Normal mode:

> Every part of the system is oscillating at the same frequency and the same phase.

Consider a system like this:

![1560735049372](assets/1560735049372.png)

#### Mode A

Introduce a displacement to the spring and release them at the same time. The system is going to behave as 2 objects with same mass.

![1560735228991](assets/1560735228991.png)

The 2 objects behave in the same way, which is simple undamped harmonic oscillation. The natural frequency is:
$$
w_A=w_B=\sqrt{\frac{2K}{m}}
$$

#### Mode B

Compress one of the little object and stretch the other one with the same displacement.

![1560735477602](assets/1560735477602.png)

The large mass would not move and the little objects oscillate at the same frequency and opposite direction. We can consider it as if the large object is oscillating in the same frequency of the little ones and with 0 amplitude.

#### Mode C

The objects are moving with same velocity.

![1560746835701](assets/1560746835701.png)

The frequency is 0. 

#### Superposition Principle

In general, for mode A:
$$
x_1=A\cos(w_At+\phi_A),x_2=-A\cos(w_At+\phi_A),x_3=-A\cos(w_At+\phi_A),w_A^2=\frac{2K}{m}
$$
For mode B:
$$
x_1=0\cos(w_Bt+\phi_B),x_2=B\cos(w_bt+\phi_B),x_3=-B\cos(w_Bt+\phi_B),w_B^2=\frac{K}{m}
$$
For mode C:
$$
x_1=x_2=x_3=c+vt,w_c^2=0
$$
There are 6 free parameters here: $A,w_A,B,w_B,c,v$, which equals the number of free parameters of 3 differential equations. Therefore, separate the process of a motion into these 3 parts can ultimately solve the motion.

Consider a 2 oscillating objects:

 ![1560849737305](assets/1560849737305.png)

Free body diagram:

![1560850148073](assets/1560850148073.png)

Equations:
$$
\hat x=m\ddot x_1=-T\sin\theta_1+K(x_2-x_1),m\ddot y_1=T\cos\theta_1-mg
$$
Apply approximation:
$$
\cos\theta_1=1,\sin\theta_1=\theta_1,T=mg,m\ddot x_1=-mg\frac{x}{l}+K(x_2-x_1)
$$
For both objects:
$$
m\ddot x_1=-(K+\frac{mg}{l})x_1+Kx_2,m\ddot x_2=Kx_1-(K+\frac{mg}{l})x_2
$$
The latter terms of both equations are