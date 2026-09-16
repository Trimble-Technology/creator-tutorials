# Get attribute

**_Extracts attribute (metadata) by name and data type._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * Sets where the attribute is read from. This can be `per point` (from each point of the input geometry), `per primitive` (from each primitive of the input geometry), `on node` (from the node), or `on graph` (from the graph).

* _type_

  * Sets the data type of the attribute to read. This can be `boolean, integer or float`, `vector`, or `string`.

* _attribute name_

  * The name of the attribute to read.

* _default_

  * The value to output when the named attribute is not found. The active default input depends on the selected _type_: a number for `boolean, integer or float`, a vector for `vector`, or a string for `string`.


#### Outputs

* _number_

  * The attribute value as a number (when _type_ is `boolean, integer or float` and a single value is returned).

* _vector_

  * The attribute value as a vector (when _type_ is `vector` and a single value is returned).

* _string_

  * The attribute value as a string (when _type_ is `string` and a single value is returned).

* _number list_

  * The attribute values as a number list (when reading per point or per primitive with _type_ `boolean, integer or float`).

* _vector list_

  * The attribute values as a vector list (when reading per point or per primitive with _type_ `vector`).

* _string list_

  * The attribute values as a string list (when reading per point or per primitive with _type_ `string`).


### Note(s)

* See [**Attribute**](/concepts/GeneralConcepts/attribute.md) for more information on attributes, and their function in the graph.

* Use this node with the [**Add attribute**](/nodes/AddAttribute/documentation.md) node to retrieve attribute data that was previously written.

* Other names for this node include: GetAttribute, Attribute To List, and Read Attribute.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:dc99eca7-c20c-4256-8fc2-d505f2e00029&version=latest" target="_blank">Adding and getting an attribute</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:a196c0b4-b55c-4601-a8ae-54a2a5dca83c&version=latest" target="_blank">Remove a choice option</a>
