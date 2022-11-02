For this graph we want to assign each of the hexagon modules with a random object.

First off, create a **switch** node and connect the three **weld vertices** nodes to it via geometry connections.

Then we want to retrieve a random _index_ for the **switch** based on the iteration that the loop is on. To do so create the following nodes and connections:



1. Create a **random** **number** node.
2. Connect the **iterator** nodes _value_ input to the _seed_ input of the **random number** node.
3. Create a **range** node and set the _maximum out_ input to `2`.
4. Connect the **random number** nodes _result_ output to the _value_ input of the **range** node.
5. Create a **round** node.
6. Connect the **range** nodes _result_ output to the _value_ input of the **round** node.
7. Connect the **round** nodes _result_ output to the _index_ input of the **switch** node.