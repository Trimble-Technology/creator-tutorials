## Add attribute

**_Adds attributes (metadata) to points, primitives, nodes, or graphs._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _type_

  * Sets the type of attribute to add. These are `per point` (added to each point of the input primitives), `per primitive` (added to each of the input primitives), `on node` (added to the node), and `on graph` (added to the graph).

* _attribute name_

  * The name to give the attribute.

* _value_

  * The value to assign to the attribute. This can be any of the basic data types (number (number, integer, and boolean), vector (vector and color), and string).


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



* The _value_ input is a special type of input that can accept any type of data.
* This node can be used in conjunction with the **get attribute** node to later retrieve the attribute data.
* Other names for this node include: Set attribute and Write attribute.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:dc99eca7-c20c-4256-8fc2-d505f2e00029&version=latest" target="_blank">Adding and getting an attribute</a>
