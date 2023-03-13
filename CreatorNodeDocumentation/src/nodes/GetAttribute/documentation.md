# Get attribute

**_Extracts attribute (metadata) by name and data type._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _type_

  * Sets the type of attribute to add. This can be `per point` (added to each point of the input geometry), `per primitive` (added to each primitive of the input geometry), `on node` (added to the node), or `on graph` (added to the graph).

* _attribute name_

  * The name to give the attribute.

* _value_

  * The value to assign to the attribute. This can be any of the basic data types (number (number, integer, and boolean), vector (vector and color), and string).


### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes



* See [Attribute](/concepts/GeneralConcepts/attribute.md) for more information on attributes, and their function in the graph.
* The _value_ input is a special type of input that can accept any type of data.
* Other names for this node include: Attribute to list and Read attribute.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:dc99eca7-c20c-4256-8fc2-d505f2e00029&version=latest" target="_blank">Adding and getting an attribute</a>
