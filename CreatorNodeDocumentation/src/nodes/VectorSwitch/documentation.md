# Vector switch

**_Switches between vector inputs using an index._**

---


#### Inputs

* _index_

  * The index of the vector value to output. This can only be `0`, `1`, `2`, or `3`.

* _value 0_

  * The vector value of index `0`.

* _value 1_

  * The vector value of index `1`.

* _value 2_

  * The vector value of index `2`.

* _value 3_

  * The vector value of index `3`.


#### Outputs

* _result_

  * The vector value of the selected index.

* _result list_

  * The list of vector values of the selected index.


### Note(s)

* Unlike the [**Switch**](/nodes/Switch/documentation.md) node, all upstream nodes of input connections are computed.

* Other names for this node include: VectorSwitch, Case, and If.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:f36aaf63-e8f5-467e-a373-8070ad7b9cde&version=latest" target="_blank">Points to curve</a>
