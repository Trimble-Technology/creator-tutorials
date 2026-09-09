# Clamped number list

**_Clamps a list of numbers to a range and forces a minimum gap between the values._**

---


#### Inputs

* _list_

  * The list of values to clamp and space.

* _mode_

  * Sets the direction that values move in when they sit closer together than the _minimum spacing_. These are `collapse out from index`, `collapse up`, and `collapse down`.
    * `collapse out from index` holds the value at the _index_ input in place and pushes the values on either side of it away from it.
    * `collapse up` pushes values towards the _maximum_.
    * `collapse down` pushes values towards the _minimum_.

* _index_

  * The index of the value in the incoming list that the rest of the list collapses out from. The first value in the list is index `0`.

* _minimum_

  * The value that defines the lower bound of the output list.

* _maximum_

  * The value that defines the upper bound of the output list.

* _minimum spacing_

  * The value that defines the smallest gap allowed between two values in the output list.

* _pad borders_

  * When `true`, the _minimum spacing_ gap is also applied between the first value and the _minimum_, and between the last value and the _maximum_. When `false`, values are allowed to sit on the bounds.


#### Outputs

* _list_

  * The list of values after clamping and spacing have been applied.


### Note(s)

* The _index_ input only has an effect when _mode_ is set to `collapse out from index`.

* The _index_ input counts positions in the incoming list, before any spacing is applied. The output list is sorted into ascending order once the operation has finished.

* Useful for tidying up the output of a [**Random number**](/nodes/RandomFloat/documentation.md) node, keeping generated values inside a usable range and stopping them from bunching together.

* Other names for this node include: ClampedList and Clamped list.
