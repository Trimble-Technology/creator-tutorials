Next we’ll translate the copies.

Create a **multiply** node and connect its _value 1_ input to the _result_ of the original **multiply** node we made in a previous step. Set the _value 2_ input on the new **multiply** node to `2`.

Create an **xyz to vector** node and connect its _x_ input to the _result_ output of the newly made **multiply** node.

Now all we need to do is connect the _vector_ output of that **xyz to vector** node to the _translate_ input of the **copy** node.