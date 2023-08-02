# Import & Export

---

The graph supports a limited set of geometry and image formats for import and export.

Imported geometry and images files need to be uploaded as [assets](/concepts/GeneralConcepts/assets.md) before they can be used.


### Images

Images are primarily used as textures for materials.

The following two formats are supported for upload:

* JPEG / JPG
* PNG

An image that was previously uploaded in one of these formats, can be loaded into a [graph](/concepts/GeneralConcepts/graph.md) using the [**image asset**](/nodes/ImageAsset/documentation.md) node.

See the [material](/concepts/GeneralConcepts/material.md) concept page for more on working with images as textures.


### Geometry import

The following formats are supported for import, with noted limitations:

* `IGES`: NURBS curves (126), patches (128), polylines (106) - no trimmed patches
* `Wavefront OBJ`: vertices, faces, groups, but no normals, nor UVs
* `DXF`: POLYLINE entity type only

Geometry that was previously uploaded in one of these formats, can be loaded into a [graph](/concepts/GeneralConcepts/graph.md) using the [**geometry asset**](/nodes/GeometryAsset/documentation.md) node.


### Geometry export

Geometry can be exported from the graph by either:

* Right mouse button clicking a node, navigating to `Download`, and selecting a file format.
* Right mouse button clicking the graph background, navigating to `Download all outputs`, and selecting a file format.

The latter option will download the geometry from all output selected nodes.

#### IGES
Exports following [primitive](/concepts/GeneralConcepts/primitive.md) types and properties:

* [NURBS curve](/concepts/GeneralConcepts/nurbsCurve.md)
* [NURBS surface](/concepts/GeneralConcepts/nurbsSurface.md)
* Their [albedo color](/concepts/GeneralConcepts/material.md)

#### Wavefront OBJ
Exports following [primitive](/concepts/GeneralConcepts/primitive.md) types:

* [Points primitive](/concepts/GeneralConcepts/points.md): points as vertices
* [PolyMesh](/concepts/GeneralConcepts/polyMesh.md)
* [NURBS surface](/concepts/GeneralConcepts/nurbsSurface.md), triangulated

Exports:

* Vertices
* Faces: 1 per triangle
* Groups: 1 per primitive
* Normals
* UVs if available

#### STL
Exports following [primitive](/concepts/GeneralConcepts/primitive.md) types:

* [PolyMesh](/concepts/GeneralConcepts/polyMesh.md)
* [NURBS surface](/concepts/GeneralConcepts/nurbsSurface.md), triangulated

ASCII STL only. STLs only contain triangle data. No normals, UVs, or groups.

#### DXF
Exports following [primitive](/concepts/GeneralConcepts/primitive.md) types:

* [NURBS curve](/concepts/GeneralConcepts/nurbsCurve.md): as DXF Polyline
* [Points primitive](/concepts/GeneralConcepts/points.md): as 3D DXF Points

Note that the curves only support 2D coordinates: XY, with Z coordinate effectively zeroed.

#### TRB
Exports following [primitive](/concepts/GeneralConcepts/primitive.md) types:

* [PolyMesh](/concepts/GeneralConcepts/polyMesh.md), as Faceted BREP
* [NURBS surface](/concepts/GeneralConcepts/nurbsSurface.md), triangulated as Faceted BREP
* [NURBS curve](/concepts/GeneralConcepts/nurbsCurve.md): as TRB Polyline
* [Materials](/concepts/GeneralConcepts/material.md): supports opacity, sideness, base color, base texture, metallicness and roughness.

Exports:

* Vertices
* Faces: 1 per triangle
* Groups: 1 per primitive
* UVs if available
