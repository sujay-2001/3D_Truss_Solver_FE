# 3D_Truss_Solver_FE
## Description:
A generalised code that would solve for any 3D truss structure was developed using the principles of direct stiffness
method in FEM. This can be then used for analysing the nodal displacements, element stresses, and check if any 
element is subject to failure using yield stress of that material.
An example problem is solved here to show how the program works.
The program can be broken into these segments:
### Importing libraries:
The required libraries (numpy, numpy, matplotlib.pyplot) were imported
### Getting inputs:
Number of elements, Number of nodes, Number of fixed nodes, Fixed nodes, Starting and ending node for each
element, Area of each element, Modulus of Elasticity of each element, Coordinates of each node are accepted from
user, and are stored accordingly for further computations.
### Transformation of stiffness matrix:
The transformed stiffness matrix for each element (in global coordinates) is computed using transformation matrix
(Direction ratios). More details are given in the report.
### Computing Global stiffness matrix (Assembling):
The global stiffness matrix is computed by assembling the individual stiffness matrices of each elements.
### Boundary Conditions:
The boundary conditions (fixed nodes, nodal loads) are applied using the inputs from user. The fixed nodes’ entries
are made zeros and stored in a new variable.
### Solving for nodal displacements:
The fixed nodes entries (all zeros) are removed to solve for the other nodal displacements using numpy’s linalg.solve.
These are then stored in the displacement variable for later analysis
### Computing elemental quantities:
The elemental quantities (in local coordinates)- axial displacements, elemental forces and stresses are computed
from nodal displacements.
### Results:
The required results (Nodal displacements, Element stresses) were printed, and the scaled deformed structure is plotted.
