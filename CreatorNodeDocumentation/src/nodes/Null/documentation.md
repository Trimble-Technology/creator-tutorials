# Null

**_Does nothing. Can be used for graph layout._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).


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

* When geometry is input into this node, the exact same geometry will be output with no modifications.

* There are two main uses for this node.

  * The first is where we can utilize its ability to output nothing. This can be useful in such cases where a graph can be configured to hide certain geometry of a final output (see the relevant example below).

  * The second is where we can utilize its ability to output the exact same geometry that is input. The can be helpful in such cases to clean a graph's layout (see the relevant example below). 

* Other names for this node include: Nothing, Layout, and Routing.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:4ec9496e-3129-4464-8f30-125fb0de860f&version=latest" target="_blank">Hiding geometry</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:1aaa9e16-e112-463e-bf9a-2c990de46a4e&version=latest" target="_blank">Isolate face holes & boundary</a> (an example of the node being used for cleaner graph layout)
