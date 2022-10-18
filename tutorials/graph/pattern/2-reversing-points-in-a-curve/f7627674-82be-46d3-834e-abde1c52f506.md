All points in a curve have an associated value. The curve is drawn by starting at point `0`, then drawing a line to point `1`, point `2`, etc. If we want to reverse the order of these points, we can do this by using **reverse vector list**, **points** and **points to curve** nodes. 

The **reverse vector list** takes the points in the circle, and reverses their number in the list i.e. point `0` will now be the last point, and the last point will be point `0`. The **points** node converts the list of vectors into “point primitives”, and the final **points to curve** node draws a curve out of that list of points.

Click through the inputs and outputs of the nodes to see how the data is being transferred to get the final reversed curve.
