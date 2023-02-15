# Copy

**_Copies and transforms geometry._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


### Inputs

* _# of copies_

  * The number of copies to make of the input primitives.

* _translate_

  * The vector value that defines how much each copy will be translated (moved). Each copy of the input primitives will be translated from the transform of the previous copy.

  * For example, a box with a center at `0,0,0` is copied at a _translate_ input of `500,0,0`. The first copy will be translated to `500,0,0`, the second copy will be translated another `500,0,0` for a total translation of `1000,0,0`, and so on.

* _rotate_

  * The vector value that defines how much each copy will be rotated. Each copy of the input primitives will be rotated from the transform of the previous copy.

  * For example, a box with a starting rotation of `0,0,0` is copied at a _rotate _input of `0,0,45`. The first copy will be rotated by `0,0,45`, the second copy will be rotated another `45,0,0` for a total rotation of `0,0,90` (from the original input primitives), and so on.

* _scale_

  * The vector value that defines how much each copy will be scaled. Each copy of the input primitives will be scaled from the transform of the previous copy.

  * For example, a box (with dimensions `1000,1000,1000`) is copied at a _scale_ input of `1,1,1.5`. The first copy will be scaled by `1.5,1.5,1.5` (now with dimensions of `1000,1000,1500`), the second copy will scale the first copy (that has the dimensions of `1000,1000,1500`) by `1,1,1.5` (now with dimensions of `1000,1000,2250`), and so on.

* _uniform scale_

  * The value that defines how much each copy will be scaled uniformly. Each copy of the input primitives will be scaled from the transform of the previous copy.
  
  * For example, a box (with dimensions `1000,1000,1000`) is copied at a _uniform scale_ input of `1.5`. The first copy will be uniformly scaled by `1.5` to the dimensions of `1500,1500,1500`, the second copy will uniformly scale the first copy (that has the dimensions of `1500,1500,1500`) by `1.5` to the dimensions of `2250,2250,2250`, and so on.

* _combine meshes_

  * Sets whether to combine all copied meshes into a singular mesh primitive. Only meshes are combined. Curves, NURBS surfaces, and other primitive types are ignored with this function.


### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)



* The _combine meshes_ input has the same function as the **combine meshes** node with its _group behavior_ input set to `exclude meshes from groups`.
* Other names for this node include: Duplicate.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:f303c34e-2e54-495f-9948-f7542bcc844d&version=latest" target="_blank">Copying geometry</a>
* <a href="https://kind-dune-0f6b12f1e.1.azurestaticapps.net/?assetURI=whp:d62fe689-b7c0-4fd6-8d17-70deef935725&version=latest" target="_blank">Loft as NURBS patch</a>
