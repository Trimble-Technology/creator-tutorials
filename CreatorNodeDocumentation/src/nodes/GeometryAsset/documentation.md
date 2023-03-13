# Geometry asset

**_Imports a geometry asset._**

---


### Inputs

* _preload asset_

  * Sets whether to load the output geometry asset on graph load or not.

* _asset uri_

  * The asset URI (as a string value) that defines what uploaded geometry asset to output. See [Assets](/concepts/GeneralConcepts/assets.md) for more information.

* _use OBJ groups_

  * Sets whether the output geometry asset utilizes OBJ groups as separate primitives or not (this is only relevant if the geometry asset is of the Wavefront OBJ file format).


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

* _asset uri_

  * The asset URI of the uploaded geometry asset as defined by the _asset uri_ input (as a string value). See [Assets](/concepts/GeneralConcepts/assets.md) for more information.

* _asset name_

  * The name of the uploaded geometry asset (as a string value). 


### Notes



* Geometry can be uploaded to Trimble Creator by dragging and dropping the file into the “Graph Viewer”.
* Trimble Creator supports following geometry file formats for import, with noted limitations:
    * TrimBIM (.trb)
    * IGES
        * NURBS curves (126), patches (128), polylines (106) - no trimmed patches.
    * Wavefront OBJ
        * Vertices, faces, groups, but no normals, nor UVs.
    * DXF
        * Polyline entity type only.
* Other names for this node include: Geometry, Load, OBJ, IGES, IGS, STL, DXF, and TrimBIM.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:40b0b7fe-81f5-45a9-bb89-926664d698fa&version=latest" target="_blank">Geometry Assets</a>
