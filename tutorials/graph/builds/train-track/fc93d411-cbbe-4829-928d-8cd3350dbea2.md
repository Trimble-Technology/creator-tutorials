Next, we will use the points created in the **points** node to create our Bézier curve. From the **points** node, create a **points to curve** node with a geometry connection.

Initially, this will create a zig-zag line between the points. What we want though is to smoothen this curve into a Bézier by setting the following inputs:

* _order_	=	`4`
* _beziers_	=	`true`
