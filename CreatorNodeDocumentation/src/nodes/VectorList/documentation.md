# Vector list

**_Creates a list of xyz vector values._**

> This node has data inputs and outputs.
>
> This node does NOT have geometry inputs and outputs.


### Inputs

* _list_

  * The vector list to output.

* _size_

  * The size (length) of the list to output when the _initialize_ input is set to `true`.

* _default_

  * The default value of the list to output when the _initialize_ input is set to `true`.

* _initialize_

  * Sets the _list_ input values as per the values of the _size _and _default _inputs.


### Outputs

* _list_

  * The vector list as defined by the _list _input.


### Notes



* A custom list can be made by clicking on the `<vector list>` space of the _list _input via the “Add Item” button.
* When the _initialize_ input is `true`, manually inputted values will be overridden by the _default_ input value.
* Other names for this node include: Point list, Coordinate list, Direction list, and xyz list.


### Examples


* <a href="https://creator.trimble.com/graph?assetURI=whp:3e5bc942-7604-4c0d-a534-b43d093bdb85&version=latest" target="_blank">Points to curve</a>
