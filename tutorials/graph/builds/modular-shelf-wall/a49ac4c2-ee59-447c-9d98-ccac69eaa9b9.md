Next we will scale the randomly selected object so that it’ll fit nicely into the hexagon module. We will need three pieces of data to do so; the “Shelf depth”, the size of the offset hexagon (internal dimensions of the module), and the original size of our object.

First, create an **expression** node and connect its _a_ input to the _value_ output of the “Shelf depth” **number** node. Set the _expression_ input on the **expression** node to `min(a,b)/c*0.75`.

Then, create a **geometry size** node from the **offset 2d path** node that defines the thickness of the shelf material. Create a **divide** node and set its _value 2_ input to `1.5` and make the following connections:



* **geometry size** nodes _sizeX_ output 	>	**divide** nodes _value 1_ input.
* **divide** nodes _result_ output		>	**expression** nodes _b_ input.

Finally, from the **switch** node, create another **geometry size** node and connect its _sizeZ_ output to the _c_ input of the **expression** node.