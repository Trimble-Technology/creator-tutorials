# Offset 2d path

**_Offsets curves in the chosen workplane._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _work plane_

  * The work plane in which the 2D offset operation will be performed in. This can be `X=0`, `Y=0`, or `Z=0`.

* _pre-flatten_

  * Flattens the input curves into the work plane defined by the _work plane_ input before the 2D offset operation.

* _offset_

  * The distance the input curves will be offset.

* _join_

  * Sets the type of join that will be performed at the vertices of the 2D offset. This can be  `miter`, `square`, `round`, or `simple (none)`.

* _miter limit_

  * The distance limit before a miter join is made. If joins of an offset are beyond the limit, then a bevel join will be made at the limit value.

* _arc precision_

  * The level of precision of the round join offset. The closer to `0`, the higher the precision of the rounded join.

* _close resulting curves_

  * Sets whether to close the resulting curves after the 2D offset operation.


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output curve primitives.

* _points.x_

  * The list of x values of the points of the output curve primitives.

* _points.y_

  * The list of y values of the points of the output curve primitives.

* _points.z_

  * The list of z values of the points of the output curve primitives.


### Notes

* Both the _miter limit_ and _arc precision_ inputs only affect the `miter` and `round` join types respectively and will only be available when those types are defined in the _join_ input.

* Other names for this node include: OffsetCurve, Offset curve, and Offset polygon.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:4116d118-97d3-4d27-a68f-09df21dcd0c2&version=latest" target="_blank">Offset joins</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:fd24181a-8fa7-40b2-8404-00224cc84e6c&version=latest" target="_blank">Filet using offset</a>
