Now that we have our base curve, we will adjust its resolution so that we can place a series of sleepers along it at particular spacings.

Create a **curve to polyline** node from the **points to curve** node with a geometry connection. Start a connection from the _value_ output of the “Approx. sleeper spacing” **number** node and drop it on the _length_ input of the newly created **curve to polyline** node.

Then all we need to do is set the _mode_ to `approx segment length`.