## Geometry center

**_Calculates the center of the input primitives._**

> This node has data inputs and outputs.
>
> This node has geometry inputs, but does NOT have geometry outputs.


#### Inputs

* _mode_

  * Sets the mode in which the **geometry center** node calculates the center of the input primitives. This can be `center` (the midpoint of the geometry bounds) or `centroid` (the average of the points within the geometry).

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


#### Note(s)



* Other names for this node include: Centroid and Barycenter


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:2d0e0c34-7abb-4d9a-8059-f52783a2bb4b&version=latest" target="_blank">Geometry center</a>
* <a href="Create a bounding box" target="_blank">https://creator.trimble.com/graph?assetURI=whp:db2e8f1e-4682-4580-89c4-b5b9ad60cc96&version=latest</a>
