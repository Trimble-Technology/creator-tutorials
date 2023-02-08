## Attribute

Attributes are metadata that can be attached to Trimble Creator geometry (<a href="/concepts/GeneralConcepts/primitive.md" target="_blank">primitives</a>), points, nodes, and graphs.

In Trimble Creator, attributes "piggy back" on points and primitives as they flow through the graph. This avoids the need to use separate graph branches for metadata and geometry.

If so desired, attributes can also enrich the computed output with custom data that is industry or application-specific.

Examples:

* Attach IFC (Industry Foundation Classes) data to the geometry of architectural products, like doors and windows.
* Enrich <a href="/concepts/GeneralConcepts/locator.md" target="_blank">locators</a> to become connectors or snapping points.

#### Attribute value types

Attributes can be of the following value type:

* Number (example: `1.234`)
* String (example: `"ABC"`)
* Vector (example: `[1, 2, 3]`)

#### Attribute name

Each attribute has a given name.

#### Types of attributes

Attributes are computed state, carried by nodes.

Attributes are _node centric_. So for example, primitive attributes cannot be different per-primitive in a node. Nor can point attributes. Every primitive in a node is paired to the same point and primitive attributes.

##### Point

Point attributes come in list form. This is list of attribute values, paired to primitives' points.

Each point attribute's list contains one list item per point in the computed output of a node. The list is as long as the total number of points across all primitives in a node's computed output.

So if a computed node contains two primitives, one with 10 points and another with 20 points, the point attribute lists will be 30 items long.

##### Primitive

Primitive attributes come in list form. This is list of attribute values, paired to primitives of a node.

Each primitive attribute's list contains one list item per primitive in the computed output of a node. The list is as long as the total number of primitives in a node's computed output.

So if a computed node contains 10 primitives, the primitive attribute lists will be 10 items long.

##### Node

Node attributes are single values, and get passed downstream from node to node in the directed acyclic graph (DAG) flow of a graph.

##### Graph

Node attributes are single values, and get set at the graph level.

Best to declare graph attributes only once.