To copy the sleeper along the curve, create a **copy using vectors** node and connect the **box** node to it.

At the moment nothing will happen because we haven’t set any points to copy the sleeper to. This is where our curve comes into play.

Connect the _points_ output of the **curve to polyline** node to the _positions_ input of the **copy using vectors** node.