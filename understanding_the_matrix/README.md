Video Creation Notes

Create four locators
*  x_vector
*  y_vector
*  z_vector
*  t_vector
*  Set locator sizes to 0.2
*  Hide all the rotate, scale and visibility attributes

Set up Bifrost arrows
*  rename to bifrost_arrows
*  expose start, end and colors
*  add 4 new items to each
*  make the bifrost node into reference mode, so it can’t be selected
*  connect the locators to end positions
*  set colors, red, green, blue and white
*  position locators in place and text move around to show arrows

An additional note for the start positions of the bifrost arrows
*  The start positions need a connection, or they may not exist when the file is next loaded in
*  If the arrows are not showing, check the start positions

Set up rotate object using a sphere
*  rename the sphere "rotate"
*  make the sphere radius 0.2
*  parent constrain the x, y, z locators to the sphere

Set up a poly cube, which will show the result of the matrix
*  in draw override
*  put into reference mode and turn off shading
*  the cube will be non-selectable and only show the edges

In the node editor
*  create a 4x4 matrix node
*  connect the loc translates to the matrix node
*  Connect the matrix output to the cube parent offset matrix

Action
*  select cube and copy the attribute editor tab, then show the matrix for offset parent matrix
*  rotate the sphere to show the x, y, z vectors changing
*  move the x, y, z vectors to show scaling
*  move the x, y, z, vectors to show shearing
*  move the t vector to show translation

