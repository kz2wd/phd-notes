Expresses the change in [[velocity]] $u$ of a flow over time as a function of time and space depending on the [[pressure]] $p$, the [[density]] $\rho$ and the [[viscosity]] $\nu$ of the flow.



$$\frac{\delta u}{\delta t} = -(u . \nabla) u - \frac{\nabla p}{\rho} + \nu \nabla^2 u $$

This expression can be read as: The variation in velocity over time at a certain point in space is defined by the viscous forces minus the convective derivative minus the pressure gradient over the density.

Moving from the [[abstract representation]] to the [[implementation]] requires a discretization of the fields and operators.

For the [[velocity]], and [[pressure]], [[grid]]s are used.
[[Viscosity]] and [[density]] are uniform scalars.