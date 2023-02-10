## Align

**_Aligns input primitives to each other._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _mode_

  * Sets the mode in which input primitives are aligned. This can be `between primitive connections` (which will align input geometry to the primitives within the first geometry connection) or `all input primitives` (which will align input geometry to the first primitive).

* _x align target_

  * Sets what boundary/value that primitives are aligned by in the x-axis. This can be `None` (which will not align primitives in the x-axis), `min`, `centroid`, or `max`.

* _x source_

  * Sets what source that primitives are aligned to in the x-axis. This can be `first connection or primitive` (as defined by the _mode_ input), `average of all` (which takes the bounds of all input primitives), or `value` (which aligns to a particular value rather than the bounds of primitives).

* _of x source_

  * Sets what boundary/value that primitives are aligned to in the x-axis. This can be `min`, `centroid`, or `max`.

* _x value_

  * The value that primitives are aligned to in the x-axis when the _x source_ input is set to `value`.

* _x offset_

  * The value that defines how much to offset primitives from the alignment in the x-axis.

* _y align target_

  * Sets what boundary/value that primitives are aligned by in the y-axis. This can be `None` (which will not align primitives in the y-axis), `min`, `centroid`, or `max`.

* _y source_

  * Sets what source that primitives are aligned to in the y-axis. This can be `first connection or primitive` (as defined by the _mode_ input), `average of all` (which takes the bounds of all input primitives), or `value` (which aligns to a particular value rather than the bounds of primitives).

* _of y source_

  * Sets what boundary/value that primitives are aligned to in the y-axis. This can be `min`, `centroid`, or `max`.

* _y value_

  * The value that primitives are aligned to in the y-axis when the _y source_ input is set to `value`.

* _y offset_

  * The value that defines what to offset primitives from the alignment in the y-axis.

* _z align target_

  * Sets what boundary/value that primitives are aligned by in the z-axis. This can be `None` (which will not align primitives in the z-axis), `min`, `centroid`, or `max`.

* _z source_

  * Sets what source that primitives are aligned to in the z-axis. This can be `first connection or primitive` (as defined by the _mode_ input), `average of all` (which takes the bounds of all input primitives), or `value` (which aligns to a particular value rather than the bounds of primitives).

* _of z source_

  * Sets what boundary/value that primitives are aligned to in the z-axis. This can be `min`, `centroid`, or `max`.

* _z value_

  * The value that primitives are aligned to in the z-axis when the _z source_ input is set to `value`.

* _z offset_

  * The value that defines what to offset primitives from the alignment in the z-axis.

* _first object_

  * Sets what to do with the first geometry connection/primitive. This can be `keep position`, `include in align`, or `delete`.


#### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


#### Note(s)



* When the _mode_ input is set to `between primitive connections` the primitives in each geometry connection are treated as a group.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:92e7e780-0b33-4970-bc97-d32c2f6ee4bc&version=latest" target="_blank">Align geometries</a>
