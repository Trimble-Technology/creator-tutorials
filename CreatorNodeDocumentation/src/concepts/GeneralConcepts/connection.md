# Connection

---

A connection is between an output of one [node](/concepts/GeneralConcepts/node.md), and an input of another node. Connections define the dependencies of nodes in the [graph](/concepts/GeneralConcepts/graph.md).

Upstream and downstream nodes describe nodes relative to each other in terms of dependencies. An upstream node's output can be a downstream node's input.

Circular connections/dependencies are impossible in a directed acyclic graphs (<a href="https://en.wikipedia.org/wiki/Directed_acyclic_graph" target="_blank">DAG</a>).  Outputs of a node cannot be connected to the inputs of the same node or upstream nodes.


### Connection types

There are two types of connections in the [graph](/concepts/GeneralConcepts/graph.md). A thicker white connection, which represents the flow of geometry, and a thinner grey connection which represents the flow of data.