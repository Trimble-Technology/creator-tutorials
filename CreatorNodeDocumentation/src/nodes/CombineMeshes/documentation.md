# Combine meshes

**_Combines meshes into a single mesh._**

---


### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.

* _group behavior_

  * Sets how input groups will behave. This can be `exclude meshes from groups` (will not combine meshes within input groups), `include meshes from groups` (will combine meshes within all input groups), or `combine per top-level group` (will only combine meshes within each input group).


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes

* If you wish to treat multiple primitives as a single primitive (whilst preserving individual primitives) instead, use the [**group**](/nodes/GroupPrimitives/documentation.md) and [**ungroup**](/nodes/UnGroupPrimitives/documentation.md) nodes.

* This node is a [destructive operation](/concepts/GeneralConcepts/destructive.md) if there is more than one primitive in it's _geometry_ input.

* If input meshes have differing [material](/concepts/GeneralConcepts/material.md) properties, then the output combined mesh will adopt the properties of the last input mesh primitive.

* Other names for this node include: CombineMeshes, Merge meshes, Unify meshes, and Join.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:99cc263d-67d8-4de1-9f6f-4a0bd4f2d975&version=latest" target="_blank">Combine meshes</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:5866ad6e-2308-4113-b199-d6d875b7a175&version=latest" target="_blank">Point grids</a>
