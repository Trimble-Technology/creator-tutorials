# Combine data

**_Combine incoming data into a list of data._**

---


#### Inputs

* _input 1_

  * The first data value to combine. Can be of any data type (number, string, or vector).

* _input 2_

  * The second data value to combine. Can be of any data type (number, string, or vector).

* _input 3_

  * The third data value to combine. Can be of any data type (number, string, or vector).

* _input 4_

  * The fourth data value to combine. Can be of any data type (number, string, or vector).

* _input 5_

  * The fifth data value to combine. Can be of any data type (number, string, or vector).

* _input 6_

  * The sixth data value to combine. Can be of any data type (number, string, or vector).

* _input 7_

  * The seventh data value to combine. Can be of any data type (number, string, or vector).

* _input 8_

  * The eighth data value to combine. Can be of any data type (number, string, or vector).

* _expand mode_

  * Sets how lists are expanded when combining them. This can be `Preserve lists` (keeps list nesting / does not expand lists), `Expand lists` (unpacks/expands lists by one level), or `Expand lists recursively` (unpacks/expands lists recursively into a single unnested list).


#### Outputs

* _data list_

  * The list of combined data.


### Note(s)

* If _input 1 - 8_ is empty/unconnected, it will be ignored from the combination.

* Typically this node is used to build a set of values for a JSON string to provide a list of parameters and values to a [**graph asset**](/nodes/GraphAsset/documentation.md) node.

  * Connect the _data list_ output of this [**Combine data**](/nodes/CombineData/documentation.md) node to the _values_ input of a [**JSON builder**](/nodes/JsonBuilder/documentation.md) node to provide these parameter values.

* Other names for this node include: CombineData.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:335c3935-fd41-4dff-b56c-81ae45b1e904&version=latest" target="_blank">Graph referencing • Using the JSON builder and combine data to build a parameter set</a>
