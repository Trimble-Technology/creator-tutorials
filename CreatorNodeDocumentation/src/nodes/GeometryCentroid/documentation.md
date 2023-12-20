# Geometry center

**_Calculates the center of the input primitives._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * Sets the mode in which this node calculates the center of the input primitives. This can be `center` (the midpoint of the geometry bounds) or `centroid` (the average of the points within the geometry).

* _output opposite_

  * Sets whether to invert the output geometry center or not.


#### Outputs

* _center_

  * The vector value of the calculated geometry center of all input primitives.

* _centerX_

  * The x value of the calculated geometry center of all input primitives.

* _centerY_

  * The y value of the calculated geometry center of all input primitives.

* _centerZ_

  * The z value of the calculated geometry center of all input primitives.

* _primitive centers_

  * The list of vector values of the geometry centers of each individual input primitive.


### Notes


* Other names for this node include: GeometryCentroid, Centroid, and Barycenter.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:2d0e0c34-7abb-4d9a-8059-f52783a2bb4b&version=latest" target="_blank">Geometry center</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:db2e8f1e-4682-4580-89c4-b5b9ad60cc96&version=latest" target="_blank">Create a bounding box</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:9be3e2e0-6dbb-4c83-a1f1-49a80e7f1cb2&version=latest" target="_blank">Spiral curve</a>
