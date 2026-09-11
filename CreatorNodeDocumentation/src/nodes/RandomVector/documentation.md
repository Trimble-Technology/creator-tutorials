# Random vector

**_Creates random vector value(s)._**

---

> #### DEPRECATED
>
> Spherical random vectors are incorrectly distributed only in the positive area.
>
> Superseded by [Random vector](/nodes/RandomVectorV2/documentation.md)


#### Inputs

* _spherical_

  * Sets whether the random vector(s) are created spherically or not (i.e. all created vectors have a magnitude of `1`) or not. When set to `false`, random vectors will randomize each vector component (x, y, and z) between `-1` and `1` (or `0` and `1` if the _positive values_ input is set to `true`).

* _positive values_

  * Sets whether to only output positive vector components (x, y, and z) or not.

* _use seed_

  * Sets whether to use a seed or not. Only relevant when the _spherical_ input is set to `false`.

* _seed_

  * The seed of the created random vector value when _use seed_ is set to `true`.

* _#_

  * The number of random vector values that are created.


#### Outputs

* _result_

  * The created random vector value.

* _result list_

  * The list of created random vector values.


### Note(s)

* If the _use seed_ input is set to `false`, a new random vector value will be created each time the node is computed.

* Both the _use seed_ and _seed_ inputs are only relevant when the _spherical_ input is set to `false`.

* Other names for this node include: RandomVector.
