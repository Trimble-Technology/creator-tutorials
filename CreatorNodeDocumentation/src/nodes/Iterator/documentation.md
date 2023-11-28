# Iterator

**_Iterates through a number of loops as defined by a paired loop node with the same tag._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _idling value_

  * The integer value to output.

  * This value doesn’t have any effect on the computed result of the paired [**loop**](/nodes/Loop/documentation.md) node, rather it allows the change of the _value_ output to inspect nodes within specific iterations.

* _tag_

  * The tag that is used to reference an **iterator** - [**loop**](/nodes/Loop/documentation.md) pair.


### Outputs

* **_geometry_**

  * Output primitives.

* _value_

  * The integer value output as defined by the current iteration of a loop. The _idling value_ input allows you to change this output to view nodes within specific iterations.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes



* The geometry output of the **iterator** node changes depending on if the paired [**loop**](/nodes/Loop/documentation.md) node has its _cumulative_ input set to `true` or not.
    * If the paired [**loop**](/nodes/Loop/documentation.md) node's _cumulative_ input is set to `false`, then the geometry output of the relevant **iterator** node will be the input primitives.
    * If the paired [**loop**](/nodes/Loop/documentation.md) node's _cumulative_ input is set to `true`, then the geometry output of the relevant **iterator** node will be the result of the previous iteration.


### Examples

* <a href="https://creator.trimble.com/graph?assetURI=whp:0892473a-e280-4dbf-8186-752079bef11e&version=latest" target="_blank">Loops: 2D boolean two sets of curves</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:d1ff11e5-3999-40b1-bd15-680d8d3a91d0&version=latest" target="_blank">Loops: Random colors</a>
