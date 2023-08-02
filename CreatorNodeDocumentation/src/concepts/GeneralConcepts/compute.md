# Compute

---

### Evaluation

[Graph](/concepts/GeneralConcepts/graph.md) evaluation is used to determine which nodes within the graph require compute. In general, commands changing the graph state will cause the graph to be evaluated.

Evaluation determines the 'upstream' dependencies of a graph's [output nodes](/concepts/GeneralConcepts/outputNode.md).

The [graph](/concepts/GeneralConcepts/graph.md) utilises lazy evaluation to determine the need for compute. Not all nodes in the graph will necessarily be computed every cycle. In general, nodes 'downstream' of changed nodes, and 'upstream' of a graph's [output nodes](/concepts/GeneralConcepts/outputNode.md), are candidates for compute.


### Compute

Compute is the act of executing the logic described by a [graph](/concepts/GeneralConcepts/graph.md). Compute will occur after graph evaluation, if required.

Below is a visualisation of a simple graph containing three nodes and the 3d view representing the computed output of graph:

<p align="center">
  <img width="600" src="images\GraphCompute.gif"/>
</p>

In this visualisation the highlighted [node](/concepts/GeneralConcepts/node.md) is set to be an [output node](/concepts/GeneralConcepts/outputNode.md) of this [graph](/concepts/GeneralConcepts/graph.md), and as such, computed.

* The [**box**](/nodes/PolyBox/documentation.md) node named "box" creates a polygonal box primitive on compute.
* The [**sphere**](/nodes/PolySphere/documentation.md) node named "sphere" creates a polygonal sphere primitive on compute.
* The [**collect**](/nodes/Collect/documentation.md) node named "collect" does not modify or create geometry. It simply collects input primitives and outputs these on compute.

1. "box" node is set to be an output node.
    * Graph state is updated and evaluated.
    * "box" node computes and displays in the 3d view.
2. "sphere" node is set to be an output node.
    * Graph state is updated and evaluated.
    * "sphere" node computes and displays in the 3d view.
3. "collect" node is first set to be an output node.
    * Graph state is updated and evaluated.
    * "collect" node computes and outputs nothing (as the "collect" node creates creates nothing itself).
4. "box" node's output is connected to the input of the "collect" node.
    * Graph state is updated and evaluated.
    * "collect" node computes and displays the box.
5. "sphere" node's output is additionally connected to the input of the "collect" node:
    * Graph state is updated and evaluated.
    * "collect" node computes and the view displays both the sphere and the box.

It is possible for multiple [nodes](/concepts/GeneralConcepts/node.md) to be set to be the graph's output. In this example, if the "box" node and "sphere" node were both set to be output nodes, the compute result would be a polygonal box and sphere.