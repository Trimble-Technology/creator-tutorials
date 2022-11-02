Now we will use the single column of hexagons and move them based on the values we calculated in the previous step.

Create an **xyz to vector** node and make the following connections:

* **divide** node’s _result_ output	>	**xyz to vector** node’s _z_ input
* **multiply** node’s _result_ output	>	**xyz to vector** node’s _x_ input

From the **group** node, create a **transform** node via a geometry connection. Connect its _translate_ input to the _vector_ output of the **xyz to vector** node.