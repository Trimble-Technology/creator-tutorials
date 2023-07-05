# Ephemeral

**_Outputs the ephemeral state of the graph. This state is set programmatically._**


#### Inputs

No inputs.


#### Outputs

* _is ephemeral_

  * The boolean value signifying whether the graph is in an ephemeral state or not.


### Note(s)

* Knowing and understanding the ephemeral state of a graph can be a key part to creating optimized configurable components. In layman's terms, the ephemeral state is simply a way to explain when a graph has its inputs actively changing (such as dragging a slider of a parameter).

  * This is useful as we can utilize this state with the special functionality of the [**Switch**](/nodes/FloatSwitch/documentation.md) node whereby we can switch between computationally light and heavy geometry based on what state the graph is in. If the graph is in an ephemeral state, switching to a computationally light geometry will give more immediate and efficient temporary output versus a more computationally heavy (and therefore slower) version of the output. See the graph below for an example.

  * It is important to note that simply creating a simple version of an output based on the computationally heavy version will NOT make the overall graph more optimized. The light version will need to be largely isolated from the heavy version (node and connection wise) in order to maximize optimization. This is because of the inherent way the graph computes geometry and data (see the [Graph](/concepts/GeneralConcepts/graph.md) section for more information).

* For more information on the concept of Ephemeral state, see: [Ephemeral state](/concepts/GeneralConcepts/ephemeralState.md)

* Other names for this node include: Temporary state, Dragging slider, and Preview.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:f23d0929-141a-4670-af58-8878d6b858fa&version=latest" target="_blank">Ephemeral State</a>
