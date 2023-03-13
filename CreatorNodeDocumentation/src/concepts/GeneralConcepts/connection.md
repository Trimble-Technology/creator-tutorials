# Connection

A connection is between an output of one node, and an input of another node. Connections define the dependencies of nodes in the graph.

Upstream and downstream nodes describe nodes relative to each other in terms of dependencies. An upstream node's output can be a downstream node's input.

Circular connections/dependencies are impossible in a directed acyclic graphs (DAG) (outputs of a node cannot be connected to the inputs of the same node or upstream nodes).