To apply the scale, create a **transform** node from the **switch** node via a geometry connection. Set the _center pivot_ input on the **transform** node to `false`.

Create an **xyz to vector** node and create a connection from the _result_ output of the **expression** node to all of the inputs of the **xyz to vector** node (_x_, _y_, and _z_).

Connect the _vector_ output of the **xyz to vector** node to the _scale_ input of the **transform** node.