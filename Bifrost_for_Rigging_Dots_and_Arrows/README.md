Create a system for just one dot
* Create locator
* Create new Bifrost system
* Create Point Scope node
	* Connect point scope to output
* Create Construct Points node
	* Connect the construct points to Point Scope node
	* Connect the construct points to the input node
* Go into node editor
	* connect the locator translate to bifrostNode.translateInput
* Go back into the Bifrost editor
	* Select the point scope node and adjust the default size so the dot can be better seen
	* change the shape and show what that looks likes
	* End up selecting the disk shape
	* Set coloring mode to "color"
	* Set color values to yellow
	* Demonstrate the color bug, where there needs to be at least two points connected for the color change to take affect
	* From the node editor, connect the locator translate to a second point position item
* Go to the maya view and move the locator around, showing the dot following
* Group the locator and move the group around, showing the dot does not follow
* Go back to the bifrost editor
	* create a Matrix to SRT node
	* connect the matrix to the input and rename to "matrixInput"
	* connect the matrix translate to the construct points node
	* on the input, delete the translate input attribute
* Go to the node editor
	* connect the locator world matrix to bifrostNode.matrixInput
* Go to the maya view and move the group around, showing the dot now follows

Adjust the bifrost node so it can take multiple inputs
* Go into the bifrost editor
	* Disconnect the matrix to SRT node
	* delete the input attribute
	* On the matrix node, change the transform attribute type to array matrix
	* Connect to the input and rename matrixInputs
	* Connect the matrix translate output to the construct points node
* Go into the maya view and create three more locators
* Go into the node editor and connect the locator worldmatrix attrs to the bifrost matrix inputs
* Go back to the maya vew and move the locators around

Create bifrost arrow systems
* Create new bifrost node
* in bifrost editor
	* create "create_arrow_strands" node
	* connect start and end positions to the input node
	* connect the strands to the output node
* in the maya view, select two of the locators
* from the node editor
	* connec the two locator translates to the start and end positions of the bifrost node
* from the maya view, move the locators around to the results
* from the node editor
	* connect the rest of the locators to the start and end positions
* from the bifrost editor
	* connect the "create arrows" node colors attribute to the input
* from the maya view
	* select the bifrost node and open the attribute editor
	* make sure the bifrost shape node tab is selected
	* add three color items
	* change the colors to red, green blue
	* move the locators around to show the result
* from the bifrost editor
	* select the create arrows node and adjust the arrowhead size and stem width ratio
* from the maya view, move the group around and show the arrows do not follow
* from the bifrost editor
	* create two matrix_to_srt nodes
	* change the transform input types to matrix array
	* connect the matrix nodes to the input and rename start_matrix and end_matrix
	* connect the matrix translate outputs to the start and end positions of the create arrow node
	* on the input node, delete the start and end position attributes
* from the node editor
	* connect the locator world matrices to the start and end matrix attributes
* from the maya view
	* move the group around to show the arrows now follow

Make the bifrost nodes unselectable
* select the bifrost nodes and add to a layer and set the layer to reference mode
