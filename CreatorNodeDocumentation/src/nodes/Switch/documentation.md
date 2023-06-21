# Switch

**_Switches between geometry inputs using an index value._**

---


### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.

* _index_

  * The index of the geometry connection to output.


### Outputs

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

* A special function of the **switch** node is that the graph will not compute geometry that isn't within the connection selected by the _index_ input.
  * As such, a **switch** node can be used to optimize the computation of the graph. Either, by switching between a higher or lower polygon count geometry, or with the **ephemeral** node (for more information, see [Ephemeral State](/concepts/GeneralConcepts/ephemeralState.md)).
  * This is not true, however, for the [Number switch](/nodes/FloatSwitch/documentation.md), [Vector switch](/nodes/VectorSwitch/documentation.md), or [String switch](/nodes/StringSwitch/documentation.md) nodes.

* Other names for this node include: Choose and Pick.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:cf9c93de-1888-468b-9853-b03e2ec1e38e&version=latest" target="_blank">Switch</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:8ef44cc4-9f21-46a0-9d96-e067882c64db&version=latest" target="_blank">Switching between geometries</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:fe7bed58-ff6c-4a0b-a05a-49dd8ddbe5e8&version=latest" target="_blank">Ephemeral state</a>
