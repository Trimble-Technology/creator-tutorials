# Box

**_Creates a box._**

---


### Inputs

* _type_

  * Sets the type of box to output. This can be `normal` or `csg`.

* _center_

  * The vector value that defines the center of the output box.

* _scale_

  * The vector value that defines the scale of the output box.

* _uniform scale_

  * The vector value that defines the uniform scale of the output box.


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



* The scale of a box in both the _scale_ and _uniform scale_ inputs are additive and are both considered in the operation of the node.
* The size of a box when both the _scale_ and _uniform scale_ inputs are `1` are the same unit scale as the set “graph length unit”. For example if the “graph length unit” is in millimeters, then the size of the box will be `1mm,1mm,1mm`.
* Other names for this node include: Cube and Poly box.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:f70fe738-3bee-486c-a016-5b19b2102d22&version=latest" target="_blank">Scaling a box</a>
