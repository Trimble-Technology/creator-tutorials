The **copy using vectors** node can be used to copy inputted geometry to a particular vector, or set of vectors.

In this case, we will copy a box primitive along a straight line.

Connect the geometry output of the **box** node and connect it to the **copy using vectors** node. Then connect the *points* output of the **line** node and connect it to the *positions* input of the **copy using vectors** node. Thus, the boxes will be copied to the points along the line.