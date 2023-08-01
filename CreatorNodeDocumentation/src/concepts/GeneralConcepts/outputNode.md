# Output Node

---

Any [node](/concepts/GeneralConcepts/node.md) (or set of nodes) can be tagged as the output of a graph, e.g. by left-clicking the node in the graph viewer. This will enforce [compute](/concepts/GeneralConcepts/compute.md) of these nodes by the compute engine. The computed output of these nodes can be considered the desired output of a [graph](/concepts/GeneralConcepts/graph.md).

Modification to the graph state will trigger a graph evaluation, and potentially [compute](/concepts/GeneralConcepts/compute.md).

<p align="center">
  <img width="600" src="images/CreatorCow.png"/>
</p>

In the graph depicted above, the green highlighted [**material**](/nodes/SetMaterial/documentation.md) node is set to be an output, and as such, computed.

It is possible for multiple [nodes](/concepts/GeneralConcepts/node.md) to be set to be the graph's output (e.g. by holding the SHIFT key when output selecting nodes in the graph viewer), in which case both of the output selected nodes will be [computed](/concepts/GeneralConcepts/compute.md).