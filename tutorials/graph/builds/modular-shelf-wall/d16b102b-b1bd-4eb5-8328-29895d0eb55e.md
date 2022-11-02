Next we will define the distance the hexagons need to be moved in order to form a grid in the vertical direction.

Create a **geometry size** node from the **circle** node via a geometry connection. We will use the height of the hexagon as the distance the copies need to be moved. Create an **xyz to vector** node and connect the _sizeZ_ output from the **geometry size** node to the _z_ input of the new **xyz to vector** node.

Now all we need to do is connect the _vector_ output from the **xyz to vector** node to the _translate_ input on the **copy** node.

Then create a **group** node from the **copy** node via a geometry connection. Why we do this will become clear soon.