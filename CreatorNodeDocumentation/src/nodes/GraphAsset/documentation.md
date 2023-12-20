# Graph asset

**_References graphs._**

---


#### Inputs

* _preload asset_

  * Sets whether to load the referenced graph when the parent graph is loaded or not.

* _asset uri_

  * The asset URI (as a string value) that defines what referenced graph asset to output. See [Assets](/concepts/GeneralConcepts/assets.md) for more information.

* _latest version_

  * Sets whether to load the latest version of the referenced graph or not.

* _parameters_

  * A JSON string containing key-value pairs that defines what values to set parameters in the referenced graph.


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

* _asset uri_

  * The asset URI (a string value) of the referenced graph. See [Assets](/concepts/GeneralConcepts/assets.md) for more information.

* _asset name_

  * The name of the referenced graph as a string value.

* _parameters_

  * The JSON string containing key-value pairs of the referenced graph’s parameters.


### Note(s)

* Some examples of a JSON string for the _parameter_ input are as follows (which can be input as a string value type):

  * {“Parameter1”:value,“Parameter2”:value}

  * {“Length”:1000,“Width”:500,“Thickness”:300}

* The JSON string can be constructed using various methods, but it is recommended to use the [**Combine data**](/nodes/CombineData/documentation.md) and [**JSON builder**](/nodes/JsonBuilder/documentation.md) nodes to do so. An example of this can be found in the example graphs linked below.

* Other names for this node include: GraphAsset, Graph import, Graph reference, Subgraph.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:335c3935-fd41-4dff-b56c-81ae45b1e904&version=latest" target="_blank">Graph referencing: Using JSON builder and combine data to build a parameter set</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:e80c57db-bf81-427d-995d-939bbf014fe0&version=latest" target="_blank">Graph referencing: Referenced graph</a>
