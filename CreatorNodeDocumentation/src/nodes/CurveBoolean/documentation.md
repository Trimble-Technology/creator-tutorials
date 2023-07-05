# Boolean 2d paths

**_Performs 2D boolean operations on curves/polygons._**

---


### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.

* _work plane_

  * The work plane in which the 2D boolean operation will be performed in. This can be `X=0`, `Y=0`, or `Z=0`.

* _pre-flatten_

  * Flattens the input curves/polygons into the work plane defined by the _work plane_ input before the 2D boolean operation.

* _boolean type_

  * Sets the type of 2D boolean operation to be performed. This can be `intersect`, `union`, `difference`, or `xor`.

* _fill type_

  * Sets the type of fill that is considered when the 2D boolean operation is performed. For more information visit: [http://www.angusj.com/delphi/clipper/documentation/Docs/Units/ClipperLib/Types/PolyFillType.htm](http://www.angusj.com/delphi/clipper/documentation/Docs/Units/ClipperLib/Types/PolyFillType.htm)

* _primary polygon_

  * Sets which input curve/polygon is to be considered as the primary polygon in the 2D boolean operation. This can be the `first` or `last` of the list of input curves/polygons.

* _primary role_

  * Sets the role of the primary curve/polygon (as defined by the _primary polygon_ input). This can be `clip` (the curve/polygon to operate with), or `subject` (the curve/polygon to operate on).

* _close resulting curves_

  * Sets whether to close the resulting curves/polygons after the 2D boolean operation.


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output curve/polygon primitives.

* _points.x_

  * The list of x values of the points of the output curve/polygon primitives.

* _points.y_

  * The list of y values of the points of the output curve/polygon primitives.

* _points.z_

  * The list of z values of the points of the output curve/polygon primitives.


### Note(s)



* 2D boolean operations are projected back to the selected work plane defined by the _work plane_ input.
    * If _pre-flatten_ is `false`, then all curves that are to be operated on need to be on the defined work plane. Otherwise the operation will fail, or curves/polygons will be excluded from the operation.
* Requires at least two curve/polygon input primitives.
* Other names for this node include: Curve boolean and Polygon boolean.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:c505ab4f-1489-4013-b8b8-a396821a6203&version=latest" target="_blank">Boolean union curves</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:9fe15144-82d8-4984-90fc-6fa110f4fbbd&version=latest" target="_blank">Triangulate overlapping outlines</a>
