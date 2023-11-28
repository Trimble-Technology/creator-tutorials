# Mirror

**_Mirrors geometry across a selected axis._**

---

### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _axis_

  * Sets the axis in which input primitives are mirrored across. This can be `x`, `y`, or `z`.

* _mode_

  * Sets the position of the mirror axis in which input primitives are mirrored. This can be `around min`, `around center`, `around max`, or `around pivot value` (which sets a custom mirror axis).

* _pivot_

  * The vector value that defines the mirror plane when the _mode_ input is set to `around pivot value`.

* _keep input geo_

  * Sets whether to keep the input primitives or not.

* _combine result_

  * Sets how resulting meshes are combined. This can be `leave as is` (will not combine meshes), `combine pairs of meshes` (will combine an individual [PolyMesh](/concepts/GeneralConcepts/polyMesh.md) primitive with its mirrored pair), or `combine all meshes`.

* _mask_

  * The list of boolean values that defines which primitives to mirror. If empty, all primitives will be mirrored.


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

* The _mode_ inputs first three options (`around min`, `around center`, and `around max`) set the mirror axis position at the bounds of the input primitives.

* Mirrored primitives will also have their UV’s ([NURBS curves](/concepts/GeneralConcepts/nurbsCurve.md) and [surfaces](/concepts/GeneralConcepts/nurbsSurface.md)) and normals mirrored as well.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:a562497a-84f6-44e1-a061-3aec106c2029&version=latest" target="_blank">Mirroring geometry</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:aa44f91a-92e4-4c34-a541-3392071e5065&version=latest" target="_blank">Bifold opening</a>