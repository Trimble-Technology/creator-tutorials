# Apply material

**_Applies the connected material to connected geometries._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _material_

  * The material definition to apply. Connect this from the _material_ output of a [**create material**](/nodes/CreateMaterial/documentation.md) node.


#### Outputs

* **_geometry_**

  * Output primitives with the connected material applied.


### Note(s)

* This node does not define material properties on its own. Connect a [**create material**](/nodes/CreateMaterial/documentation.md) node's _material_ output to this node's _material_ input.

* See [Material](/concepts/GeneralConcepts/material.md) for more information.

* Other names for this node include: ApplyMaterial, Material, Assign Material, Assign Colour, Assign Color, Paint, Apply Paint, Bucket, Paint Bucket, Set Material, Set Color, Shader, Set Shader, Apply Shader, and Assign Shader.
