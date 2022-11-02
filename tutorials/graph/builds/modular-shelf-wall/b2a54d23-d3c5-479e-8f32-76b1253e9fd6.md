For the _radius_ input of our **circle** node turned hexagon, we will need to divide the _value_ input from the “Module diameter” **number** node by 2.

Create a **divide** node and connect its _value 1_ input to the _value_ output of the “Module diameter” **number** node.

Set the **divide** nodes _value 2_ input to `2`, and connect its _result_ output to the _radius_ input of the **circle** node.