# Error check

**_Checks whether an input node is errored._**

---


#### Inputs

* **_geometry_**

 * Accepts a single geometry connection (unless the SHIFT key is held).

* _input_

  * The data input to check for errored data nodes.

* _message_

  * The message (as a string value) to output when the node detects an errored input. If left blank, the specific error of the errored node will be output.


#### Outputs

* _error_

  * The boolean value signaling whether a connected node has errored or not.

* _error message_

  * The error message of the connected node that has errored.


### Note(s)

* Other names for this node include: Error switch.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:8a3f9eb9-542d-4d31-9c63-796510e250fe&version=latest" target="_blank">Switch when graph errors</a>
