# Sort number list

**_Sorts the values of a number list._**

---


#### Inputs

* _list_

  * The list of values to sort.

* _near value_

  * The value that is used to find the closest value to it (above and below) in the _list_ input.


#### Outputs

* _sorted list_

  * The sorted list of values.

* _original indexes_

  * The list of original indexes in the order of the sorted list.

* _reverse indexes_

  * The list of sorted indexes in the order of the original list.

* _value below_

  * The value immediately below the value defined by the _near value_ input in the sorted list.

* _value above_

  * The value immediately above the value defined by the _near value_ input in the sorted list.

* _below index_

  * The index value of the _value below_ output.

* _above index_

  * The index value of the _value above_ output.


### Note(s)

* This can also be used to find the closest values to an input value from within a sorted list by using the _near value_ input and the _value below_, _value above_, _below index_, and _above index_ outputs.

* Other names for this node include: SortFloatList.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:c4c3fa14-5ff0-45d2-872d-c1acfc8d9729&version=latest" target="_blank">Get geometry based on size</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:e48847b9-ef91-4c0c-8583-69961a23f647&version=latest" target="_blank">Sort vector list</a>
