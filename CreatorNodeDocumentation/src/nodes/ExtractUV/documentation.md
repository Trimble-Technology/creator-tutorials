# Get UV

**_Gets UVs from mesh points._**

---


#### Inputs

* _default u_

  * The value to output if there are no U values on an input point.

* _default v_

  * The value to output if there are no V values on an input point.


#### Outputs

* _u_

  * The list of U values of the points within an input mesh.

* _v_

  * The list of V values of the points within an input mesh.


### Note(s)

* Currently only operates on PolyMesh primitives, not NURBS surfaces etc. If any primitive type other than a PolyMesh is input, the _default u_ and _default v_ values will be output.

* Other names for this node include: Extract UVs.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:9fcc6f91-c9eb-4b58-bd23-a77689aa20ba&version=latest" target="_blank">Using UVs to deform meshes</a>
