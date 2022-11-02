We can actually go ahead and delete the connection between the **get primitive** node and the **loop** node before moving on. In its place we will create an **offset 2d path** node from the **get primitive** node via a geometry connection. Set the _work plane_ input on the **offset 2d path** node to `Y = 0`.

To give the hexagon some thickness, we need to be using the negative value of the “Shelf material thickness” parameter as we want to offset the curve inwards, rather than outwards.

Create a **subtract** node and connect its _value 2_ input to the _value_ output of the “Shelf material thickness” **number** node. Then, connect the **subtract** nodes _result_ output to the _offset_ input of the **offset 2d path** node.