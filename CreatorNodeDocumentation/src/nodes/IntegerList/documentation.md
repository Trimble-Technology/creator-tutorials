# Integer list

**_Creates a list of integer values._**

> This node has data inputs and outputs.
>
> This node does NOT have geometry inputs and outputs.


### Inputs

* _list_

  * The integer list to output.

* _size_

  * The size (length) of the list to output when the _initialize_ input is set to `true`.

* _iterator_

  * Sets the _list_ input to an iterative (sequential) list of integer values (i.e. 0, 1, 2, …, n) when the _initialize_ input is set to `true`.

* _default_

  * The default value to output when the _initialize_ input is set to `true`.

* _initialize_

  * Sets the _list_ input values as per the values of the _size_, _iterator, _and _default _inputs.


### Outputs

* _list_

  * The integer list as defined by the _list _input.


### Notes



* A custom list can be made by clicking on the `<integer list>` space of the _list _input via the “Add Item” button.
* When the _initialize_ input is `true`, manually inputted values will be overridden by the _default_ input value.
* When both the _initialize_ and _iterator _inputs are `true`, the iterative values override the _default_ input value.
* Other names for this node include: Number list.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:866137ad-bf24-4a85-8953-1c9ca1657d7b&version=latest" target="_blank">Isolating a primitive</a>
