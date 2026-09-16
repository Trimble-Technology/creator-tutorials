# Sphere

**_Creates a sphere._**

---


#### Inputs

* _center_

  * The vector value that defines the center of the output sphere.

* _radius_

  * The value that defines the radius of the output sphere.

* _type_

  * Sets the type of sphere to output. This can be `ico` (an icosphere constructed from equilateral triangles), `columns & rows` (a sphere constructed from columns and rows), or `CSG` (a sphere constructed from the CSG system).

* _detail_

  * The value that defines the level of detail of the output sphere when the _type_ input is set to `ico`.

* _columns_

  * The value that defines the number of columns of the output sphere when the _type_ input is set to `columns & rows` or `CSG`.

* _rows_

  * The value that defines the number of rows of the output sphere when the _type_ input is set to `columns & rows` or `CSG`.

* _phi start_

  * The value that defines the start angle (in the same axis as the _columns_ input) of the output sphere when the _type_ input is set to `columns & rows`.

* _phi end_

  * The value that defines the end angle (in the same axis as the _columns_ input) of the output sphere when the _type_ input is set to `columns & rows`.

* _theta start_

  * The value that defines the start angle (in the same axis as the _rows_ input) of the output sphere when the _type_ input is set to `columns & rows`.

* _theta end_

  * The value that defines the end angle (in the same axis as the _rows_ input) of the output sphere when the _type_ input is set to `columns & rows`.


#### Outputs

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
* When the _type_ input is set to `columns & rows`, adjusting the _phi_ and _theta_ start/end inputs will create domes and partial spheres.

* Other names for this node include: PolySphere, Icosphere, Globe, Ball, and Poly Sphere.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:4958d06e-7d71-4881-893a-6c7ae2efd16e&version=latest" target="_blank">Sphere</a>
