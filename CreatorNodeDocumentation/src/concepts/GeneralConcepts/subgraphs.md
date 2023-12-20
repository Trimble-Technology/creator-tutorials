# Subgraphs

---

A subgraph is a fully functional [graph](/concepts/GeneralConcepts/graph.md) loaded within another graph. This is done by loading of a previously saved graph asset, using a [**graph asset**](/nodes/GraphAsset/documentation.md) node.

The graph is thus represented as a node, with

* The graph's [parameters](/concepts/GeneralConcepts/parameter.md) as the node's input,
* The graph's computed [primitives](/concepts/GeneralConcepts/primitive.md) (all primitives of all output nodes) as the node's output.

This makes graphs a nestable, or recursive, concept.

Care needs to be taken not to cause an infinite nesting loop, where graph A is nested in graph B, nested in graph A.

The parameters of a nested graph need to be provided to the [**graph asset**](/nodes/GraphAsset/documentation.md) node's parameters input as a JSON string containing key-value pairs of the nested graph's parameters. For example:

`{"Parameter A":3.14, "Parameter B":666,"Parameter C":42}`

The [**graph asset**](/nodes/GraphAsset/documentation.md) node's URI input takes a graph assetURI, which triggers load (and compute) of this referenced graph on compute of the parent graph's [**graph asset**](/nodes/GraphAsset/documentation.md) node. Example of an asset URI:

`whp:d65f2b43-7c90-4f45-97d0-d03b93abff85`


### Ephemeral behavior

A nested graph inherits its [ephemeral state](/concepts/GeneralConcepts/ephemeralState.md) from its parent graph. Specifically, a [**graph asset**](/nodes/GraphAsset/documentation.md) node will retrieve its parent graph's ephemeral state and forwards the state to its internal graph object only at the node's compute time, before the internal [graph](/concepts/GeneralConcepts/graph.md) is evaluated.
