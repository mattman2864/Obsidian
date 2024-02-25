#CS #FTC
Based on the [[Closed Loop Control]] and the [[Proportional Controller]], we can roughly control a system's state using the formula:
$$u(t)=k(r(t)-x(t))$$
Where:
$u(t)$ is our current motor input;
$x(t)$ is our current system state; and,
$r(t)$ is our current reference

Full state feedback takes a slightly different approach than PID control, but has the same idea.

One can model a linear system in the form:
$$\dot x=Ax+Bu$$
where $\dot x$ is the vector that represents the state of yoursystem