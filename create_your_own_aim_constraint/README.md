Notes from my video

Create two locators
-   make locator sizes 0.2
-   aim
-   up

Create Bifrost Arrows for the aim and up
-   set arrow size 0.05
-   set aim color to yellow (1, 1, 0)
-   set up color to light blue (0, 1, 1)
-   set bifrost node to reference mode so it’s not selectable
-   connect locators to bifrost

Matrix Vectors

Create another Bifrost Arrows to show matrix vectors
-   premake slots for x, y, z start, end and colors
-   set colors to r, g, b values
  
Create x_vector
-   normalize the aim
	- If you can't make a Normalize node
		- Create a VectorProduct node and set to None
		- Connect your vector to the first input
		- Make sure the Normalize checkbox is checked
-   connect x_vector to arrows

Create z_vector
-   create cross product of aim and up, this becomes the z_vector
	- aim vector into first input
	- up vector into second input
-   connect z_vector to arrows
-   normalize the z_vector

Create y_vector
-   create cross product of z_vector and aim, this becomes the y_vector
	- z_vector into first input
	- aim vector into second input
-   connect y_vector to arrows
-   normalize the y_vector

Aim Constraint

Set up Constraint
-   Create a cube, which will be constrained 
-   Create 4x4 Matrix Node
-   connect the x, y and z vectors to the matrix node
	- x_vector -> 4x4 in00, in01, in02 
	- y_vector -> 4x4 in10, in11, in12
	- z_vector -> 4x4 in20, in21, in22
-   connect the matrix node to the offset parent matrix of the cube

