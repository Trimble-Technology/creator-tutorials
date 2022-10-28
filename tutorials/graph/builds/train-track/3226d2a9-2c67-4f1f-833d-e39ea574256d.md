To make our sleepers we will use a **box** node (so create one!). To adjust the size of the box, we will need to supply it with a _scale_ input which requires a vector.

Create an **xyz to vector** node and connect its _vector_ output to the _scale_ input of the **box** node.

And as a bit of housekeeping, set the _uniform scale_ input of the **box** node to `1`, and the _center_ input to `0,-50,0`.