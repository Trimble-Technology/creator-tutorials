Now we just need to place our randomly selected object into the proper position in the hexagonal module. We will need two pieces of data to do so; the center of the fully built module and the bounds of the offset hexagon (the internal dimensions of the module).

First with a geometry connection, create a **geometry centroid** node from the **extrude** node that makes the final uncolored geometry for the hexagonal module.

Then, create a **geometry bounds** node from the **offset 2d path** node that defines the thickness of the shelf material.

Once we’ve done that, create an **xyz to vector** node and make the following connections:

* **geometry centroid** nodes _centerX_ output	>	**xyz to vector** nodes _x_ input
* **geometry centroid** nodes _centerY_ output	>	**xyz to vector** nodes _y_ input
* **geometry bounds** nodes _zMin_ output	>	**xyz to vector** nodes _z_ input.

Then we can connect the _vector_ output of the **xyz to vector** node to the _translate_ input of the **transform** node that we made in the previous step.