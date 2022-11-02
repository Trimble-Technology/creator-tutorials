Create a **collect** node and connect the **group** and **transform** nodes to it with geometry connections. We will use this as our basis to copy the number of modules across the width of the shelf.

From the **collect** node create a **copy** node via a geometry connection. As we have two columns that we will be copying across, we will first need to divide the “Modules wide” **integer** node by 2. Create a **divide** node and connect its _value 1_ input to the _value_ output of the “Modules wide” **integer** node. Then set the **divide** nodes _value 2_ input to `2`.

We will also need to round this value up to the nearest whole number, so create a **ceiling** node and connect its _value_ input to the _result_ output of the **divide** node.

Now we can connect the _result_ output of the **ceiling** node to the _# of copies_ of the **copy** node.