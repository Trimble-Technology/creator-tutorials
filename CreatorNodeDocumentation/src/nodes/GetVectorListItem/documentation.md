# Get vector list item

**_Gets a vector from a vector list using an index value._**

---


#### Inputs

* _list_

  * The list of vectors to get a list item from.

* _index_

  * The index value that defines which list item to get from the _list_ input.

* _errorMode_

  * Sets how the node will behave when errored. This can be `error this node` or `output default vector`.

* _default vector_

  * The default vector to output when the _errorMode_ input is set to `output default vector`.


#### Outputs

* _vector_

  * The vector of the gotten list item.

* _x_

  * The x value of the gotten list item vector.

* _y_

  * The y value of the gotten list item vector.

* _z_

  * The z value of the gotten list item vector.

* _vector list_

  * The list of vectors of gotten list items.

* _x list_

  * The list of x values of the gotten list items vectors.

* _y list_

  * The list of y values of the gotten list items vectors.

* _z list_

  * The list of z values of the gotten list items vectors.


### Note(s)

* Multiple list items can be gotten by inputting a list of indices into the _index_ input.

* Other names for this node include: GetVectorListItem, Switch, Choose, Pick, Choice, or List item.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:28271a8c-c0b2-41a1-9647-534eff8a4c24&version=latest" target="_blank">Isolate a point from a curve via index</a>
