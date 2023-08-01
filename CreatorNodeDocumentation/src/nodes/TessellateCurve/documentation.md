# Curve to polyline

**_Subdivides curves into polylines._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * The mode in which input curves are subdivided. This can be `# of segments` (divides the input curve into equal length segments), `segment length` (divides the input curve into segments of specified length), or `approx segment length` (divides the input curve into equal lengths closest to the specified approximate length).

* _segments_

  * The value that defines the number of segments the input curves are subdivided into when the _mode_ input is set to `# of primitives`.

* _length_

  * The value that defines the length of the segments the input curves are subdivided into.

* _accuracy_

  * The value that defines the number of u coordinates sampled per segment.

* _per order 2 segment_

  * Sets whether to subdivide the existing segments of the input curves, or the curve as a whole.


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

* _u coordinates_

  * The list of U coordinates where the curve was subdivided.

* _curve lengths_

  * The list of lengths of the subdivided curves (full curve lengths, not curve segment lengths).


### Notes

* If the _mode_ input is set to `segment length` and the input value does not evenly divide the curve, the last segment length will be the remainder.

* Other names for this node include: TessellateCurve, Tessellate curve, Redraw, and Divide curve.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:988bd2be-bde4-48e8-bc03-ffef4efe8996&version=latest" target="_blank">Curve to polyline</a>
* <a href="https://kind-dune-0f6b12f1e.1.azurestaticapps.net/?assetURI=whp:2162d907-1f8f-4cfe-bb9a-3a302b0a5038&version=latest" target="_blank">Tessellate a polyline into line segments</a>
* <a href="https://kind-dune-0f6b12f1e.1.azurestaticapps.net/?assetURI=whp:90a9d506-7b56-4643-b174-3376a0546514&version=latest" target="_blank">Tessellate a polyline into segments across the length of the full line</a>
