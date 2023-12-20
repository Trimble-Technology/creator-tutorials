# Triangulate surface

**_Converts NURBS surfaces to meshes._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * Sets the mode in which the quality of the resulting triangulated mesh is determined. This can be `combine U & V quality` or `separate U & V quality`.

* _quality_

  * The value that defines the quality for both U & V coordinates of the resulting triangulated mesh when _mode_ is set to `combine U & V quality`.

* _qualityU_

  * The value that defines the quality for the U coordinate of the resulting triangulated mesh when _mode_ is set to `separate U & V quality`.

* _qualityV_

  * The value that defines the quality for the U coordinate of the resulting triangulated mesh when _mode_ is set to `separate U & V quality`.


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


### Note(s)

* Other names for this node include: TesselatePatch, NURBS to polygon, NURBS patch to triangles, Mesh, Tessellate, and Convert.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:58a0d810-9142-4b57-9c02-7f0564509ded&version=latest" target="_blank">Triangulate a NURBS surface</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:7ef97c31-05f2-48ac-a48f-4d231e7140d2&version=latest" target="_blank">Smooth lofted mesh</a>
