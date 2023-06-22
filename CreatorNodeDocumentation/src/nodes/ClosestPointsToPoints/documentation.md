# Closest points to points

**_Finds the closest target points to source points._**

---


#### Inputs

* _mode_

  * Sets the method in which points are found. This can be either `closest point` or `number of points within radius`.

* _source points_

  * The list of source points to find the closest points among the _target points_.

* _target points_

  * The list of target points among which the closest points are found from the _source points_.

* _calculate distance_

  * Sets whether to calculate the distances between the _source points_ and their nearest _target points_ or not.

* _radius_

  * The value that defines the size of the radius in which a number of points are found when the _mode_ is set to `number of points within radius`.


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

* _indices_

  * The list of indices of the closest target points.

* _distances_

  * The distances between the source points and the closest target points.

* _number of points within radius_

  * The number of target points within the defined radius from each source point when the _mode_ intput is set to `number of points within radius`.


### Note(s)

* Other names for this node include: Nearest, Distance, Radius, and Neighbour.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:503a598c-eea1-4420-8df9-316e4ad683c7&version=latest" target="_blank">Find shortest distance between two polygons</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:f35138ca-d980-4b82-a088-b8fa0d2b554e&version=latest" target="_blank">Loft polygons with unequal points</a>
