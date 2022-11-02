The width of the grid is a little more tricky than the height as we want to create a sort of honeycomb-esque grid. In this case we will copy the column of hexagons, first to fit snuggly next to the previous column, but also continually along for as many rows as we need.

To snuggly fit two columns next to each other, we first need to translate it up half the height of an individual hexagon.  So create a **divide** node and connect its _value 1_ input to the _sizeZ_ output of the **geometry size** node. Set the _value 2_ input on the **divide** node to `2`.

Create a **multiply** node and connect its _value 1_ input to the _sizeX_ output of the **geometry size** node. Set the _value 2_ input to `0.75` on the **multiply** node.