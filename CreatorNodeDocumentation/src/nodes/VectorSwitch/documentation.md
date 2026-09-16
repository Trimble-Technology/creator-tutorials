# Vector switch

**_Switches between vector inputs using an index._**

---


#### Inputs

* _index_

  * The index of the vector value to output. This can only be `0`, `1`, `2`, or `3`.

* _vector 0_

  * The vector value of index `0`.

* _vector 1_

  * The vector value of index `1`.

* _vector 2_

  * The vector value of index `2`.

* _vector 3_

  * The vector value of index `3`.


#### Outputs

* _vector_

  * The vector value of the selected index.

* _x_

  * The x component of the selected vector.

* _y_

  * The y component of the selected vector.

* _z_

  * The z component of the selected vector.

* _vector list_

  * The list of vector values of the selected index.

* _x list_

  * The list of x components of the selected vector values.

* _y list_

  * The list of y components of the selected vector values.

* _z list_

  * The list of z components of the selected vector values.


### Note(s)

* Unlike the [**Switch**](/nodes/Switch/documentation.md) node, all upstream nodes of input connections are computed.

* Other names for this node include: VectorSwitch, Case, and If.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:f36aaf63-e8f5-467e-a373-8070ad7b9cde&version=latest" target="_blank">Points to curve</a>
