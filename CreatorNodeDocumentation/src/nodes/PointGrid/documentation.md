# Point grid

**_Creates a grid of points._**

---


#### Inputs

* _origin_

  * The vector value that defines the origin (the position of the first point) of the output points.

* _resolutionX_

  * The value that defines the resolution (number of points) within the x-axis.

* _resolutionY_

  * The value that defines the resolution (number of points) within the y-axis.

* _resolutionZ_

  * The value that defines the resolution (number of points) within the z-axis.

* _spacing_

  * The vector value that defines the spacing between points within the grid.


#### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes

* The points defined by the resolution inputs are set within the positive direction of their respective axes.

* Other names for this node include: PointGrid.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:5866ad6e-2308-4113-b199-d6d875b7a175&version=latest" target="_blank">Point grids</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:a6e51888-ac0a-41e9-8660-31e752841386&version=latest" target="_blank">Rectangle grid</a>
