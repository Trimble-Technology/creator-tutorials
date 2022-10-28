As we will need to copy and loft each rail individually, we will need to have a loop that does these functions per rail profile.

Create a **get primitive** node from the **copy using vectors** node with the two rail profile meshes. Next, make a geometry connection from our newly created **get primitive** node to the **copy using vectors** node that we copy/pasted in the previous step.

Then, create a **iterator** node and connect its _value_ output to the **get primitive** _index_ input. Also, set the **iterator** node’s _tag_ input to `perRail`.