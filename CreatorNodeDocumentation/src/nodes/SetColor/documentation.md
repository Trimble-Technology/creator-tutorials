## Set color

**_Sets the color and alpha of primitives._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _set_

  * Sets what aspect of the input primitives to set the color. This can be either the `surface (diffuse) color` or the `mesh wireframe colors`.

* _color_

  * The color value (vector) that defines what color to set the input primitives.

* _alpha_

  * The value that defines the alpha (transparency) of the set color (between a range of `0` and `1`).

* _primitive mask_

  * The list of boolean values that defines which input primitives to set the color to. If empty, all input primitives will be set to the defined color.


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



* Other names for this node include: Alpha, Wireframe, and Transparency.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:bc96d8e6-ac0b-4daa-92e6-587764b8d6b4&version=latest" target="_blank">Set Color</a>
* <a href="https://creator.trimble.com/?viewLayout=verticalSplit&assetURI=whp:d81bdd83-7204-4718-898b-645127deac74&version=latest" target="_blank">Deleting primitives with a boolean pattern</a>
