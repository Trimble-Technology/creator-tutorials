All we need to do now is to make a geometry connection between the **transform** node with the randomized object to the **collect** node at the end of the loop.

And just to align the shelf nicely within the world space, create an **align** node from the **loop** node and set the following inputs on the **align** node:

* _x align target_		=	`centroid`
* _x source		_=	`value`
* _x value_			=	`0`
* _z align target_		=	`min`
* _z source_		=	`value`
* _z value_			=	`0`
* _First object_		=	`include in align`