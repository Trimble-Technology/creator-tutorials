The _y_ and _z_ inputs/size for the sleeper box is easy, set the _y_ and _z_ input for the **xyz to vector** node to `100` and `200` respectively. As for the _x_ input, this will be the sum of the “Track width” **number** node, the width of the “Rail profile”, and a little bit of extra width on either side of the rails.

To do so, first, create an **expression** node and set the _expression_ input to `a+b+100`.

Secondly, make a connection from the _value_ output of the “Track width” **number** node to the _a_ input of the **expression** node.
 
Thirdly, create a **geometry size** node from the “Rail profile.iges” node via a geometry connection and connect its _sizeX_ output to the _b_ input of the **expression** node.

Finally, with all our inputs connected to the **expression** node, we can make a connection between its _result_ output to the _x_ input of the **xyz to vector** node.