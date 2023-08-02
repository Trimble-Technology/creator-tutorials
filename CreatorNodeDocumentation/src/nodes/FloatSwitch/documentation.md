# Number switch

**_Switches between number inputs using an index._**

---


#### Inputs

* _index_

  * The index of the value to output. This can only be `0`, `1`, `2`, or `3`.

* _value 0_

  * The value of index `0`.

* _value 1_

  * The value of index `1`.

* _value 2_

  * The value of index `2`.

* _value 3_

  * The value of index `3`.


#### Outputs

* _result_

  * The value of the selected index.

* _result list_

  * The list of values of the selected index.


### Note(s)

* Unlike the [Switch](/nodes/Switch/documentation.md) node, all upstream nodes of all input connections are computed.

* Other names for this node include: FloatSwitch, Case, If, and Value switch.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:910bb39f-e209-4813-a66b-2ead7b0f592c&version=latest" target="_blank">Switch between set parameters</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:99d2fb7d-2b36-4a9b-a1fb-229ecdb543e0&version=latest" target="_blank">Parametrically selecting particular options from a dropdown input</a>
