# Destructive Operations

---

A destructive operation refers to a node's operation/function that will alter geometry in such a way that may result in the loss of information (such as [Attributes](/concepts/GeneralConcepts/attribute.md)). These kinds of operations typically occur in nodes which completely rebuild the geometry they operate on.

Some examples of nodes with destructive operations are:

* [**Combine mesh**](/nodes/CombineMesh/documentation.md)
* [**Boolean 3D geometry**](/nodes/MeshBoolean/documentation.md)