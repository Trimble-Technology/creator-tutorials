# Output Node

Any node (or set of nodes) can be tagged as the output of a graph, e.g. by left-clicking the node in the graph viewer. This will enforce compute of these nodes by the compute engine. The computed output of these nodes can be considered the desired output of a graph.

Modification to the graph state will trigger a graph evaluation, and potentially compute.

<p align="center">
  <img width="400" src="images/CreatorCow.png"/>
</p>

In the graph depicted above, the green highlighted **material** node is set to be an output, and as such, computed.

It is possible for multiple nodes to be set to be the graph's output (e.g. by holding the SHIFT key when output selecting nodes in the graph viewer), in which case both of the output selected nodes will be computed.