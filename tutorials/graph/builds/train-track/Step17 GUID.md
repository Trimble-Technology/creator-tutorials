The final step for the rails is to combine the loft and caps.

Create a **combine meshes** node and connect the relevant **get primitive**, **loft**, and **flip mesh normals**.

Then create a **loop** node from the **combine meshes** node and set the following inputs:

* _# of loops_		=	`2`
* _tag_			=	`perRail`