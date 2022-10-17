This pattern outlines the method of switching between geometries using a **switch** node and a **choice** node.

The **switch** node is what we will connect our geometry to, to define what geometry we want to switch between. The **choice** node is what we use to control which connected geometry is visible in the 3D viewer. Explore the inputs into the **switch** node to see where the **choice** is connected. Also have a look at the input for the **choice** node to see how the parameter is defined.

An important thing to note in this pattern is that the connection order into the **switch** node plays a big part in the final output of the graph.

bs  acaa