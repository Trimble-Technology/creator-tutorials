# Transform

**_Performs transformations (translate, rotate, and scale) on geometry._**

---


### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.

* _translate_

  * The vector value that defines the translation input primitives will move.

* _rotate_

  * The vector value that defines the rotation input primitives will rotate around based on the _center pivot_ or _pivot_ inputs.

* _scale_

  * The vector value that defines how much the input primitives will be scaled by.

* _center pivot_

  * Sets whether the input primitives will be manipulated with respect to their centers or not.

* _pivot_

  * The vector value that defines the position of the pivot that the input primitives will be manipulated with respect to when the _center pivot _ input is set to `false`.


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

* _translate_

  * The list of vector values that input primitives have been translated by.

* _rotate_

  * The list of vector values that input primitives have been rotated by.

* _scale_

  * The list of vector values that input primitives have been scaled by.


### Note(s)

* Other names for this node include: Move, Translate, Rotate, Scale, Position, and Size.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:775eaeb4-45fd-4082-85a6-fa72d30f0825&version=latest" target="_blank">Transforming geometry</a>