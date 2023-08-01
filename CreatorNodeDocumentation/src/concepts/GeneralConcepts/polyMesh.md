# PolyMesh

---

A PolyMesh is a [primitive](/concepts/GeneralConcepts/primitive.md) representing a 3D polygonal mesh. A PolyMesh has following notable properties:

* _vertices_: A list of 3D vectors representing the 3D coordinates of the mesh's vertices.
* _indices_: A list of integer indices into the list of vertices. Three consecutive indices define a single triangle. Triangles can share vertices. Example: indices of a PolyMesh with 2 triangles sharing 2 vertices: `[0, 1, 2, 1, 2, 3]`.
* _normals_ (optional): A list of normalised 3D vectors representing the vertex normals of the mesh. One normal per vertex, exactly.
* _UVs_ (optional): A list of 2D vectors representing the UV texture coordinates of the mesh. One vector per vertex, exactly.
