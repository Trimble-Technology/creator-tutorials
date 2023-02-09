## Loft

**_Creates lofted geometry between curves._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _mode_

  * Sets the mode in which input curves are lofted. These can be `per geometry input` (which lofts between curves from each separate geometry input), `between geometry inputs` (which lofts between curves in each geometry input), and `all input curves` (which lofts every input curve regardless of geometry input).

* _loft type_

  * Sets the type of loft that the node will output. These can be `mesh` and `NURBS surface`.

* _per_

  * The number of curves that define a single loft when the _mode_ input is set to `all input curves`. Multiple lofts can be made from the same list of curves by setting this input to a multiple of the number of input curves. Setting this to `0` will loft all input curves.

* _mesh smoothness_

  * The amount of subdivision along the direction of input curves that have an order greater than `2` when the _loft type_ input is set to `mesh`.

* _weld_

  * Sets whether to weld the resulting loft or not when the _loft type_ input is set to `mesh`.

* _interpolate_

  * Sets whether to interpolate the resulting loft or not when the _loft type_ input is set to `NURBS surface`.

* _order U_

  * The order (perpendicular to the input curves) of the resulting loft when the _loft type_ input is set to `NURBS surface`.


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



* Other names for this node include: Skin and Revolve.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:0bf18a7f-413b-4cdd-aa4f-35d723236da1&version=latest" target="_blank">Loft as NURBS surface</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:d82b650f-092e-44de-b58c-4410848f8b48&version=latest" target="_blank">Loft along curve</a>
