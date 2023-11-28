# Boolean list

**_Creates a list of boolean values._**

---


### Inputs

* _list_

  * The boolean list to output.

* _size_

  * The size (length) of the list to output when the _initialize_ input is set to `true`.

* _default_

  * The default value to output when the _initialize_ input is set to `true`.

* _pattern_

  * Sets the _list_ input to a pattern of boolean values as defined by the _start_, _end_, _skip_, and _every_ inputs when the _initialize_ input is set to `true`.

* _start_

  * The index of the _list_ input where the pattern starts.

* _end_

  * The index of the _list_ input where the pattern ends.

* _skip_

  * The number of indexes to skip within a repeated section of the pattern of the _list_ input.

* _every_

  * The number of indexes within a repeated section of the pattern of the _list_ input.

* _initialize_

  * Sets the _list_ input values as per the values of the _size_, _default_, _pattern_, _start_, _end_, _skip_, and _every_ inputs.


### Outputs

* _list_

  * The boolean list as defined by the _list_ input.


### Notes



* A custom list can be made by clicking on the `<boolean list>` space of the _list_ input via the “Add Item” button.

* When the _initialize_ input is set to `true`, any values manually entered into the _list_ input will be replaced with the _default_ input value.

* When the _initialize_ input is `true`, manually inputted values will be overridden by the _default_ input value.

* The _pattern_ input:
    * When both the _initialize_ and _pattern_ inputs are set to `true`, the _default_ input (and therefore _list_ input) will be replaced with the pattern set by the _start_, _end_, _skip_, and _every_ inputs.
    * Changing the _default_ input value will invert the set pattern.
    * List indexes outside of the pattern range (as set by the _start_ and _end_ inputs) will be set to the value according to the _default_ input.

* Other names for this node include: BooleanList, Mask, and Bitmask.


### Examples



* <a href="https://creator.trimble.com/?viewLayout=verticalSplit&assetURI=whp:d81bdd83-7204-4718-898b-645127deac74&version=latest" target="_blank">Deleting primitives with a boolean pattern</a>
