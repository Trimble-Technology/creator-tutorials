# Normals

**_Calculates the normals, tangents and binormals of primitives._**

---


### Inputs

* **_geometry_**

 * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * Sets the mode in which certain information is calculated and output.

  * There are two different modes: `normals only`, and `normals, tangents and binormals (basis)`.

* _tangents_

  * The list of tangent values to replace the calculated tangent values (these values will be used to calculate the other _normals_ and _binormals_ outputs. If left blank, the input primitives _tangents _are used).

* _normals_

  * The list of normal values to replace the calculated normal values (these values will be used to calculate the other _tangents _and _binormals_ outputs. If left blank, the input primitives _normals_ are used).

* _binormals_

  * The list of binormal values to replace the calculated binormal values (these values will be used to calculate the other _tangents _and _normals_ outputs. If left blank, the input primitives _binormals_ are used).

* _default normal_

  * The default normal value.


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

* _tangents_

  * The list of tangent values of the input primitives.

* _normals_

  * The list of normal values of the input primitives.

* _binormals_

  * The list of binormal values of the input primitives.


### Examples

* <a href="https://creator.trimble.com/graph?assetURI=whp:de8a6a01-27bb-4c73-80ee-89b4997807cc&version=latest" target="_blank">Curve point information</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:f54a5965-07e7-4a97-877f-870bd5e25172&version=latest" target="_blank">Copy using vectors</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:b9cbcf7c-7a42-4f0f-b5b3-69a9243d869a&version=latest" target="_blank">Loft along curve</a>
