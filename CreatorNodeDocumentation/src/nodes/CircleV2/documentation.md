# Circle

**_Creates a circle._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


### Inputs

* _type_

  * Sets the type of circle to output. These are `NURBS curve`, `polyline`, and `mesh`.

* _center_

  * The vector value that defines the center of the output circle.

* _orientation_

  * Sets the plane in which the output circle is orientated. These are `XZ`, `YZ`, and `XY`.

* _radius_

  * The value that defines the radius of the output circle.

* _segments_

  * The value that defines how many segments the output circle has.

* _start angle_

  * The value that defines the starting angle of the output circle.

* _end angle_

  * The value that defines the ending angle of the output circle.


### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes



* Only the `polyline` and `mesh` settings on the _type_ input have the _segments_, _start angle_, and _end angle_ inputs.
    * Adjusting the _start angle_ and _end angle_ inputs will create an arc/semicircle.
* A mesh circle is unwelded by default.
* The _segments_ input can be used to make any regular polygon (triangle, quadrilateral, pentagon, etc.).
* Other names for this node include: Arc.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:34803f98-fb91-4c48-a4a4-ef9ad88c8fa1&version=latest" target="_blank">Circle</a>
