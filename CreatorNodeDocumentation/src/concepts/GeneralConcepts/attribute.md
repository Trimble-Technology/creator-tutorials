# Attribute

---

Attributes are metadata that can be attached to [primitives](/concepts/GeneralConcepts/primitive.md), points, [nodes](/concepts/GeneralConcepts/node.md), and [graphs](/concepts/GeneralConcepts/graph.md).

Attributes "piggy back" on points and [primitives](/concepts/GeneralConcepts/primitive.md) as they flow through the [graph](/concepts/GeneralConcepts/graph.md). This avoids the need to use separate graph branches for metadata and geometry.

If so desired, attributes can also enrich the computed output with custom data that is industry or application-specific.

Examples:

* Attach IFC (Industry Foundation Classes) data to the geometry of architectural products, like doors and windows.
* Enrich [locators](/concepts/GeneralConcepts/locator.md) to become connectors or snapping points.

### Attribute value types

Attributes can be of the following value type:

* Number (example: `1.234`)
* String (example: `"ABC"`)
* Vector (example: `[1, 2, 3]`)

### Attribute name

Each attribute has a given name.

### Types of attributes

Attributes are computed state, carried by [nodes](/concepts/GeneralConcepts/node.md).

Attributes are _node centric_. So for example, primitive attributes cannot be different per-primitive in a node. Nor can point attributes. Every primitive in a node is paired to the same point and primitive attributes.

#### Point

Point attributes come in list form. This is list of attribute values, paired to [primitives'](/concepts/GeneralConcepts/primitive.md) points.

Each point attribute's list contains one list item per point in the computed output of a node. The list is as long as the total number of points across all [primitives](/concepts/GeneralConcepts/primitive.md) in a node's computed output.

So if a computed node contains two primitives, one with 10 points and another with 20 points, the point attribute lists will be 30 items long.

#### Primitive

Primitive attributes come in list form. This is list of attribute values, paired to [primitives](/concepts/GeneralConcepts/primitive.md) of a node.

Each primitive attribute's list contains one list item per primitive in the computed output of a node. The list is as long as the total number of primitives in a node's computed output.

So if a computed node contains 10 primitives, the primitive attribute lists will be 10 items long.

#### Node

Node attributes are single values, and get passed downstream from node to node in the directed acyclic graph (<a href="https://en.wikipedia.org/wiki/Directed_acyclic_graph" target="_blank">DAG</a>) flow of a graph.

#### Graph

Node attributes are single values, and get set at the graph level.

Best to declare graph attributes only once.


### Attribute merging

When attributes flow through a graph's <a href="https://en.wikipedia.org/wiki/Directed_acyclic_graph" target="_blank">DAG</a>, some some merging rules apply.

#### Point and primitive attributes

As noted above, attributes are node centric. All [primitives](/concepts/GeneralConcepts/primitive.md) and points in a node's computed output must carry the exact same attributes.

The graph will fill in the gaps. If a set of primitives with attributes `A` and `B` get merged with primitives carrying attribute `C`, the graph will extend attribute `A` and `B` to the second batch of primitives, and `C` to the first batch, so that the current node's primitives all carry `A`, `B` and `C`.

Default values for each type are used to fill the gaps:

* Number : `0`
* String: `""`
* Vector: `0,0,0`

#### Node attributes

If two or more incoming [nodes](/concepts/GeneralConcepts/node.md) carry the same node attribute, the last connected input node will be the one used.

#### Graph attributes

If the same [graph](/concepts/GeneralConcepts/graph.md) attribute is declared on two or more nodes, the last evaluated node will be the one used. Note that this can lead to unexpected results. It is likely better to make sure a graph attribute is only declared once.


### Nodes

All types of attributes can be added using the [**add attribute**](/nodes/AddAttribute/documentation.md) node.

The [**get attribute**](/nodes/GetAttribute/documentation.md) node allows querying of attribute metadata to/from graphs, nodes, primitives and points.
