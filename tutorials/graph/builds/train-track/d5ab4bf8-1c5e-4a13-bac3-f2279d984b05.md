At its core, this graph consists of a line to which we will attach geometry. In this case, the line we will use is a Bézier curve. A Bézier curve is a smooth curve that is defined by a set of control points.

To create a Bézier curve in Creator, we need to first define our control points by creating a list of vectors. To do so, create a **combine vector lists** node and connect the following **vector** nodes to it in order:

* “Track start point”	_value_	>	_list1_
* “First track control”	_value_	>	_list2_
* “Second track control”	_value_	>	_list3_
* “Track end point”	_value_	>	_list4_