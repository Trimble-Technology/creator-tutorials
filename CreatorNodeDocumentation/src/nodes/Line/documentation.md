# Line

**_Creates lines as NURBS curves._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


### Inputs

* _mode_

  * Sets the mode in which the line is created. This can be `centered` (as defined by a center point vector and direction vector), `origin + direction` (as defined by a start point vector and direction vector), or `point to point` (as defined by start and end point vectors).

* _center_

  * The vector value that defines the center of the output line when the _mode _input is set to `center`.

* _start point_

  * The vector value that defines the start of the output line  when the _mode _input is set to `origin + direction` or `point to point`.

* _end point_

  * The vector value that defines the end of the output line when the _mode _input is set to `point to point`.

* _direction_

  * The vector value that defines the direction of the output line when the _mode _input is set to `origin + direction`.

* _length_

  * The value that defines the length of the output line when the _mode _input is set to `origin + direction`.

* _number of points_

  * The value that defines the number of points within the output line.

* _order_

  * The value that defines the order of the output line. See <a href="/concepts/GeneralConcepts/nurbsCurve.md" target="_blank">NURBS curves</a> for more information.


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



* Other names for this node include: Curve and Polyline.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:1b2f283c-c260-45c4-a95b-6728344d91d9&version=latest" target="_blank">Line modes</a>
