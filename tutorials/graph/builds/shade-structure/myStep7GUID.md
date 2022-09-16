Each of the imported geometries contain two individual “primitives”, a purlin and the supporting structure. We want to separate them so that we can parameterize them in different ways.

To do so we will use the **get primitive** node.

From the **switch**, create two **get primitive** nodes. The **get primitive** node works similarly to the **switch**, in that if we supply it with an index, it will output the geometry of that index. In this case we can just set the index input of both **get primitive**’s to [0], and on one of them, set the invert input to [true] (this node will output everything BUT the geometry in index 0, in this case our purlin).

Note: the same effect can be done by setting one of the **get primitive** *index* inputs to [1].
