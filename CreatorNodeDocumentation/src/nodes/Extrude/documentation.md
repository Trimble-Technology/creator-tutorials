## Extrude mesh

**_Extrude all input faces._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _distance_

  * The distance input faces will be extruded by.

* _keep_

  * Sets which faces of the output primitives to keep. `all` keeps all faces (input faces as well as extruded faces and sides), `sides` keeps only the extruded sides, `extruded cap` keeps only the extruded faces, `caps` keeps only the input faces and the extruded faces, and `sides & extruded cap` keeps the extruded sides and caps, but not the input faces.

* _flip direction_

  * Sets whether to flip the direction of the extrusion.

* _flip normals_

  * Sets whether to flip the normals of the output primitives.


#### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:e5f67d6d-434f-4c5a-a0b2-443372979203&version=latest" target="_blank">Extrude mesh</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:3ea02aa1-c685-4932-960e-0580ebcf86ed&version=latest" target="_blank">Weld angles</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:6f0b7d7c-77ec-45c8-985a-213f54961d01&version=latest" target="_blank">Wave extrude</a>
