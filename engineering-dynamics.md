# Engineering Dynamics

## Introduction

The steps of solving dynamic problems:

- Describe motion
- Pick physical model
- Apply math

Example: System of spring.

![1556173558882](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1556173558882.png)

### Describe the Motion

Assign a coordinate system. Specify whether the reference frame is inertial.

![1556173717585](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1556173717585.png)

The x-axis is from the zero spring position.

### Apply Physics Law

Pick Newton’s second law.
$$
M\ddot x+b\dot x+kx=mg
$$
Free body diagram:

1. Draw forces in direction in which they act.
2. Assume positive values for deflections and velocity.
3. Deduce the signs from the deduction of values.

Pick energy conservation model.
$$
E=KE+PE=\frac{1}{2}kx^2+\frac{1}{2}m\dot x^2-Mgx
$$
Take the derivative by time:
$$
E_t=0
$$
The equation shows in the same form of Newton’s second law.

### Reference Frames and Vectors

Pick a coordinate system $xOy$, with the reference frame to be $O$. There are 2 objects in the space, $A,B$, with position described by vectors $R_{A/O},R_{B/O}$. The difference between the 2 positions is $R_{B/A}=R_{B/O}-R_{A/O}$. The reference frame of the vector must be specified, as in this case $/O,/A,/B$.

When finding the velocity of the object, or taking time derivative of the object, the reference frame has to be specified.

In a inertial frame, the direction of an object is always the same when observing it at any different position in the frame.

### Translation and Rotation

If a system is translating, it means that any 2 points in the system are moving in parallel path. Pure rotation means any where on the body goes in the same rate of rotating.

## 

When taking derivative of position, the reference frame must be specified, which is, in this case, the origin $O$.

![1556178730673](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1556178730673.png)
$$
\frac{dR_{B/O}}{dt}=(\frac{dR_{A/O}}{dt})_{/O}+(\frac{dR_{B/B}}{dt})_{/O},(\frac{dR_{A/O}}{dt})_{/O}=v_{A/O}
$$
The latter part gets tricky, for we have to deal with a frame which is not inertial.
$$
(\frac{dR_{B/B}}{dt})_{/O}=(\frac{\partial R_{B/A}}{\partial t})_{Axyz}+Rotation\_term
$$
The former term can be considered as the velocity of $B$ with respect to the frame, or the velocity of $B$ without the frame.

## Change of Frame

Steps of solving a motion:

- State the problem.
- Draw figures.
- Describe motion
  - the degree of freedom
  - the number of coordinates
  - assign coordinates
  - write down $v,a$
- Explain correct physical laws.
- Do the math.

The definition of the center of mass is:
$$
M_TR_{G/O}=\sum m_iR_{i/O}
$$
where the mass and corresponding position vectors are given. When observing a rotating object, the usual choice for reference frame is the center of mass. Therefore, as is done above, we take the center of mass $A$ as the reference frame and write down the relation of velocity.
$$
v_{B/O}=v_{A/O}+(\frac{\partial R_{B/A}}{\partial t})_{Axyz,no\_rotation}+w_{/O}\times R_{B/A}
$$
The partial derivative is taken to be in the frame not rotating. Take a step further:
$$
a_{B/O}=(\frac{d v_{B/O}}{dt})_{Oxyz}=a_{A/O}+(a_{B/A})_{Axyz}+2w_{/O}\times (v_{B/A})_A+\dot w_{/O}\times R_{B/A}+w_{/O}\times(w_{/O}\times R_B/A)
$$
where $w$ is the angular velocity of the rotation of the frame and the sub $A$ or $Axyz$ means the vector is measured under the coordinate system under the frame $A$. Let’s introduce cylindrical coordinates and understand this.

## Cylindrical Coordinates

### Derivatives

In the 3D coordinate system, we change the $xOy$ plane into the polar coordinate, where the unit vector $\hat R$ points towards the position vector and the unit vector $\hat \theta$ is perpendicular to $\hat R$ on the right hand side. 

![1557065281848](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557065281848.png)

The velocity and acceleration is written to be:
$$
v_{B/O}=v_{A/O}+(\frac{d}{dt}R_{B/A})_{Oxyz},a_{B/O}=a_{A/O}+(\frac{d^2}{dt^2}R_{B/A})_{Oxyz}
$$
Express $R_{B/A}$ from the prospective of $Oxyz$:
$$
R_{B/A}=R\hat R+z\hat k,\frac{d}{dt}R_{B/A}=\dot R\hat R+R\dot{\hat R}+\dot z\hat k+z\dot{\hat k}=\dot R\hat R+R\dot{\hat R}+\dot z\hat k
$$
It may be found from the graph that:
$$
d\hat R=(\dot\theta dt)\hat\theta,\dot{\hat R}=\dot\theta\hat\theta
$$
Plug in:
$$
\dot R\hat R+\dot z\hat k=(\frac{\partial R_{B/A}}{\partial t})_{/A},R\dot{\hat R}=w_{/O}\times R_{B/A}\Rightarrow v_{B/A}=v_A+w_{/O}\times R_{B/A}
$$
where $v_A$ is the velocity under the coordinate system of frame $A$. By the same idea:
$$
a_{B/A}=a_{A/O}+\frac{d}{dt}(\dot z\hat k+\dot R\hat R+R\dot\theta\hat\theta)
$$
$z$ term:
$$
\frac{d}{dt}\dot z\hat k=\ddot z\hat k
$$
$\hat R$ term:
$$
\frac{d}{dt}\dot R\hat R=\ddot R\hat R+\dot R\dot{\hat R}=\ddot R\hat R+\dot R\dot\theta\hat\theta
$$
$\hat\theta$ term:
$$
\frac{d}{dt}R\dot\theta\hat\theta=\dot R(\dot\theta\hat\theta)+R\frac{d}{dt}(\dot\theta\hat\theta)
$$
By the same idea of $\dot{\hat R}$:
$$
\dot{\hat\theta}=-\dot\theta\hat R
$$
where the minus sign shows that the direction of the change in $\hat\theta$ is opposite to the direction of $R$.

Further expansion:
$$
\frac{d}{dt}(\dot\theta\hat\theta)=\ddot\theta\hat\theta-\dot\theta^2\hat R
$$
Final result:
$$
a_{B/A}=(\ddot z\hat k+\ddot R\hat R)+2\dot R\dot\theta\hat\theta+R\ddot\theta\hat\theta-R\dot\theta^2\hat R=a_A+a_{cor}+a_{angaccel}-a_{cent}
$$
where $a_A$ is measured under the coordinate system of frame $A$. The acceleration terms may be written in another form.
$$
2\dot R\dot\theta\hat\theta=2w_{/O}\times(v_{B/A})_{Axyz},R\ddot\theta\hat\theta=\dot w_{/O}\times R_{B/A},-R\dot\theta^2\hat R=w_{/O}\times(w_{/O}\times R_{B/A})
$$
Or in a better cylindrical coordinate form:
$$
a_{B/A}=(\ddot R-R\dot\theta^2)\hat R+\ddot z\hat k+(R\ddot\theta+2\dot R\dot\theta)\hat\theta
$$

### Angular Momentum

We can plug the result for velocity into the expression of angular momentum. Suppose $O$ is the reference point for the mass point. The mass point is $B$.
$$
h_{B/O}=R_{B/O}\times mv_{B/O}=mR_{B/O}\times(\dot R\hat R+R\dot\theta\hat\theta)=mR^2\Omega\hat k
$$
where $\Omega$ is the magnitude of angular momentum. Plug in torque.
$$
\frac{d}{dt}h_{B/O}=2mR\dot R\Omega\hat k=R_{B/O}\times F_{cor}
$$
Therefore, the Coriolis force is the necessary force increasing the angular momentum.

### Candy Shooter

![1557071974958](C:\Users\a\AppData\Roaming\Typora\typora-user-images\1557071974958.png)

When rotating the rod by force, the ball inside is going to come out. May it be frictionless.

Express velocity:
$$
v_{B/O}=\dot R\hat R+R\dot\theta\hat\theta
$$
Express acceleration:
$$
a_{B/O}=a_{A/O}+(\ddot R-R\dot\theta^2)\hat R+\ddot z\hat k+(R\ddot\theta+2\dot R\dot\theta)\hat\theta
$$
