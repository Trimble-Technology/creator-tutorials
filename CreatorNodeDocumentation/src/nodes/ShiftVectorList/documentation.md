# Shift vector list

**_Shifts the items of a vector list._**

---


#### Inputs

* _list_

  * The list of vector values to shift.

* _shift_

  * The value that defines the number of positions to shift the list.


#### Outputs

* _list_

  * The shifted list of vector values.


### Note(s)

* A shifted list is cyclic.

  * For example, if a list is shifted by a _shift_ input value of `-1`, the vector value at index `0` is now at index `1` and the vector value that was at the end of the list is now at index `0`.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:defc5672-835b-4cdb-91d0-f9da8727cb37&version=latest" target="_blank">Shift curve start</a>
