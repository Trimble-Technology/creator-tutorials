# Add attribute

**_Adds attributes (metadata) to points, primitives, nodes, or graphs._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _type_

  * Sets the type of attribute to add. These are `per point` (added to each point of the input primitives), `per primitive` (added to each of the input primitives), `on node` (added to the node), and `on graph` (added to the graph).

* _attribute name_

  * The name to give the attribute.

* _value_

  * The value to assign to the attribute. This can be any of the basic data types (number (number, integer, and boolean), vector (vector and color), or string).


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)

* See [Attribute](/concepts/GeneralConcepts/attribute.md) for more information on attributes, and their function in the graph.

* The _value_ input is a special type of input that can accept any type of data.

* This node can be used in conjunction with the [**get attribute**](/nodes/GetAttribute/documentation.md) node to later retrieve the attribute data.

* Other names for this node include: AddAttribute, Set attribute and Write attribute.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:dc99eca7-c20c-4256-8fc2-d505f2e00029&version=latest" target="_blank">Adding and getting an attribute</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:a196c0b4-b55c-4601-a8ae-54a2a5dca83c&version=latest" target="_blank">Remove a choice option</a>
