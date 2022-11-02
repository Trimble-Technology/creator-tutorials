Now we will create a loop that will iterate through each hexagon, give it geometry, and place a random object into it. We will initially just make the loop, then add the filling after.

First though, from the **switch** node create an **ungroup** node via a geometry connection. Then to construct our loop:



1. From the **ungroup** node create a **get primitive** node via a geometry connection.
2. Create an **iterator** node and set its _tag_ input to `perHex`.
3. Connect the **iterator** nodes _value_ output to the _index_ input of the **get primitive** node we just made.
4. Create a **loop** node from the **get primitive** node via a geometry connection.
5. Set the **loop** nodes _tag_ input to `perHex`.
6. Create a **# of primitives** node from the **ungroup** node via a geometry connection.
7. Connect the **# of primitive** nodes _numPrimitives_ output to the _# of loops_ input on the **loop** node.

If done correctly you should just have the same set of hexagons as before when selecting the **loop** node (aka. nothing has changed), but this will set up the groundwork for what we are about to do.