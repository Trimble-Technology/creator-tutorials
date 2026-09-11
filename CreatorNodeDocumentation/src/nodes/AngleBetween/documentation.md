# Angle between

**_Finds the (smallest) angle between two vectors._**

---


#### Inputs

* _vector 1_

  * The first vector value to find the angle from.

* _vector 2_

  * The second vector value to find the angle to.

* _output radians_

  * Sets whether to output radians (rather than degrees) or not.


#### Outputs

* _result_

  * The angle between two vectors.

* _result list_

  * The list of angles between two vectors.


### Note(s)

* Calculates the angle between two vectors from `0,0,0`. To measure an angle at a different origin, use three vectors: the two to find the angle between, and the origin; transform the two vectors relative to that origin (so it becomes `0,0,0`) then perform the operation.

* Other names for this node include: AngleBetween and Angle Between Vectors.


### Example(s)


* <a href="https://creator.trimble.com/graph?assetURI=whp:514e4ba3-642f-46de-87d9-b85710d2f725&version=latest" target="_blank">Angle between</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:9ef59923-271d-4f24-b660-5dcb0d2482b6&version=latest" target="_blank">Radial point sorting</a>
