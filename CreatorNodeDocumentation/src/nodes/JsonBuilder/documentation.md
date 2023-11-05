# JSON builder

**_Creates an array or a dictionary, and serializes it to JSON._**

---


#### Inputs

* _mode_

  * Sets the mode in which a JSON is built. This can be: `Array` or `Dictionary`.

* _keys_

  * The list of string values that defines the dictionary keys when _mode_ is set to `Dictionary`.

* _values_

  * The list of varying values to be built into a JSON string. This can be a list of any data type (number, string, or vector).


#### Outputs

* _JSON_

  * The array, or dictionary, as a JSON string.


### Note(s)

* When the _mode_ input is set to `Dictionary` the input lists of _keys_ and _values_ must be of equal length.

* Typically this node is used to build a JSON string to provide a list of parameters and values to a [**graph asset**](/nodes/GraphAsset/documentation.md) node.

  * If you are building a parameter set for a graph asset, parameter names (a [**string list**](nodes/StringList/documentation.md)) need to be provided as _keys_, and values for those parameters need to be provided as _values_ within a `dictionary` format. 

  * As parameters can be of many different data types, a [**combine data**](/nodes/CombineData/documentation.md) node is often used to supply the input for the _values_ input.

* Other names for this node include: JSONBuilder and JSON string.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:335c3935-fd41-4dff-b56c-81ae45b1e904&version=latest" target="_blank">Graph referencing • Using the JSON builder and combine data to build a parameter set</a>
