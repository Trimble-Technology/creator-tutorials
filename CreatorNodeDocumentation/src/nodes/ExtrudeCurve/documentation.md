## Extrude curve

**_Extrudes curves in a vector direction._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _extrusion_

  * The vector value that defines the extent that the output NURBS surface primitive will be extruded.

* _order_

  * The value that defines the order of the output line. See <a href="/concepts/GeneralConcepts/nurbsSurface.md" target="_blank">NURBS surface</a> for more information.

* _number of spans_

  * The number of spans that the output NURBS surface will be divided into.


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



* The geometry output of this node is a NURBS surface primitive type. In order to convert it to a PolyMesh primitive type use the **triangulate surface** node.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:fb5b6019-be5a-4bc8-b2a4-624287e4a444&version=latest" target="_blank">Extrude curve</a>
