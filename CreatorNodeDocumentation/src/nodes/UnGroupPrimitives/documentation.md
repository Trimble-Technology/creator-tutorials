## Ungroup

**_Ungroups “group” primitives._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _mode_

  * Sets the mode in which group primitives are ungrouped. This can be `flatten whole hierarchy` (which ungroups all groups, even groups within other groups) or `ungroup one level` (which only ungroups the first layer of groups, any group within another group is not ungrouped).


#### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


#### Note(s)



* Primitives can be grouped together with the **group** node.
* Other names for this node include: Ungroup primitives, Disassemble, and Split group.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:f3ba7c99-3b5d-4114-8f93-9c299fb03507&version=latest" target="_blank">Hexagon grid</a>