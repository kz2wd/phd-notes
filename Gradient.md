The gradient of a field indicates the direction and magnitude of where the field increases the fastest. It is pointwise and local.

[[Abstract Representation]]:
It produces an object of 1 rank above than its input (0, scalar -> 1, vector -> 2, matrix -> 3 tensor, ...).
Applied on a 3D scalar field, the output is a vector field. It is expressed as:
$$\nabla f =\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z}$$

and in general:
$$(\nabla f)_i =\frac{\partial f}{\partial x_i}$$
with $i$ spanning the dimensions.

Applied on a vector field $u$, the output is a matrix field with a vector for each component. It is expressed as:
$$(\nabla f)_{ij} =\frac{\partial f_j}{\partial x_i}$$
with $i$ spanning the dimensions and $j$ the components of the input. Note that the order of $i$ and $j$ is subject to convention.

The input field must belong to a differentiable space H1 at least.

[[Implementation]]:
The gradient is discretized into a matrix.
The difficulty of its implementation resides in the non-uniformity of the space of the input field.
In this project, we often assume periodicity in X and Z with uniform spacing and non-uniform spacing in Y with Neuman BC.
Following Incompact3D, the proposed implementation is to use 6th order [[Compact differentiation]] scheme along Y with Neuman BC.
For X and Z, unlike in Incompact, [[Spectral differentiation]] schemes are used. 