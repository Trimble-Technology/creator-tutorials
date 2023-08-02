# Project UV

**_Creates UV coordinates on a mesh by projecting along an axis._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _axis_

  * Sets the axis in which the UV coordinates are projected. This can be `X`, `Y` or `Z`.

* _repeat U_

  * The value that defines how many times a U coordinate will be projected along its respective dimension.

* _repeat V_

  * The value that defines how many times a V coordinate will be projected along its respective dimension.

* _repeat bounds_

  * Sets the bounds by which UV coordinates are projected. These can be `per object` (per each individual primitive) or `all objects` (over all input primitives).


### Outputs

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


### Note(s)

* Other names for this node include: ProjectUV, Texture, and Map.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:b432f0b3-3b32-4867-8b38-8647efa60924&version=latest" target="_blank">Assigning materials & textures</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:3277c528-95fb-4229-9eda-dd914d66460b&version=latest" target="_blank">Flip texture UVs on a mesh</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:170a9259-2c1d-4629-bdc2-89b15db3f853&version=latest" target="_blank">Tiling textures</a>
