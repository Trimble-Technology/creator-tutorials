# Summary

[Introduction](introduction.md)

---

# Nodes

- [Value]()
  - [Parameters]()
    - [Boolean](nodes/BooleanValue/documentation.md)
    - [Choice](nodes/EnumValue/documentation.md)
    - [Color](nodes/ColorValue/documentation.md)
    - [Integer](nodes/IntegerValue/documentation.md)
    - [Number](nodes/FloatValue/documentation.md)
    - [String](nodes/StringValue/documentation.md)
    - [Vector](nodes/VectorValue/documentation.md)
  - [Lists]()
    - [Boolean list](nodes/BooleanList/documentation.md)
    - [Integer list](nodes/IntegerList/documentation.md)
    - [Number list](nodes/FloatList/documentation.md)
    - [String list](nodes/StringList/documentation.md)
    - [Vector list](nodes/VectorList/documentation.md)
- [Geometry]()
  - [2D path]()
    - [Boolean 2d paths](nodes/CurveBoolean/documentation.md)
    - [Offset 2d path](nodes/OffsetCurve/documentation.md)
  - [Attributes]()
    - [Add attribute](nodes/AddAttribute/documentation.md)
    - [Get attribute](nodes/GetAttribute/documentation.md)
  - [Copy & Loops]()
    - [Copy](nodes/Copy/documentation.md)
    - [Copy using vectors](nodes/Copy2/documentation.md)
    - [Iterator](nodes/Iterator/documentation.md)
    - [Loop](nodes/Loop/documentation.md)
  - [Creation]()
    - [Box](nodes/PolyBox/documentation.md)
    - [Circle](nodes/CircleV2/documentation.md)
    - [Cylinder](nodes/PolyCylinder/documentation.md)
    - [Line](nodes/Line/documentation.md)
    - [Locator](nodes/Locator/documentation.md)
    - [Point grid](nodes/PointGrid/documentation.md)
    - [Points](nodes/Points/documentation.md)
    - [Rectangle](nodes/Plane/documentation.md)
    - [Sphere](nodes/PolySphere/documentation.md)
    - [Tetrahedron](nodes/TetrahedronV2/documentation.md)
  - [Import]()
    - [Geometry asset](nodes/GeometryAsset/documentation.md)
    - [Graph asset](nodes/GraphAsset/documentation.md)
    - [Image asset](nodes/ImageAsset/documentation.md)
  - [Material & Texture]()
    - [Material](nodes/SetMaterial/documentation.md)
    - [Set color](nodes/SetColor/documentation.md)
    - [Project UV](nodes/ProjectUV/documentation.md)
  - [Measure]()
    - [Geometry bounds](nodes/GeometryBounds/documentation.md)
    - [Geometry center](nodes/GeometryCentroid/documentation.md)
    - [Geometry size](nodes/GeometrySize/documentation.md)
    - [# points](nodes/NumPoints/documentation.md)
    - [# primitives](nodes/NumPrimitives/documentation.md)
    - [Closest point on curve](nodes/ClosestPointOnCurve/documentation.md)
    - [Closest points to points](nodes/ClosestPointsToPoints/documentation.md)
    - [Mesh area](nodes/PolyArea/documentation.md)
    - [Normals](nodes/Normals/documentation.md)
    - [Triangle centroids](nodes/PolyCentroids/documentation.md)
  - [Modify]()
    - [Curve]()
      - [Curve to polyline](nodes/TessellateCurve/documentation.md)
      - [Extrude curve](nodes/ExtrudeCurve/documentation.md)
      - [Insert knot](nodes/InsertKnot/documentation.md)
      - [Join curves](nodes/JoinCurves/documentation.md)
      - [Points to curve](nodes/PointsToCurve/documentation.md)
      - [Simplify curve](nodes/SimplifyCurve/documentation.md)
      - [Split curve](nodes/SplitCurve/documentation.md)
      - [Unroll curve](nodes/UnrollCurve/documentation.md)
      - [Curve from surface](nodes/ExtractCurve/documentation.md)
    - [Surface]()
      - [Loft](nodes/Skin/documentation.md)
      - [Split surface](nodes/SplitPatch/documentation.md)
      - [Triangulate surface](nodes/TesselatePatch/documentation.md)
    - [Mesh]()
      - [Clean mesh](nodes/PolyClean/documentation.md)
      - [Combine meshes](nodes/CombineMeshes/documentation.md)
      - [Extrude mesh](nodes/Extrude/documentation.md)
      - [Flip mesh normals](nodes/ReverseMesh/documentation.md)
      - [Mesh boundary](nodes/MeshBoundary/documentation.md)
      - [Unweld vertices](nodes/UnweldVertices/documentation.md)
      - [Weld vertices](nodes/WeldVertices/documentation.md)
      - [Triangulate 2d path](nodes/TriangulateCurve/documentation.md)
    - [Point]()
      - [Delete points](nodes/DeletePoints/documentation.md)
      - [Get points](nodes/ExtractPoints/documentation.md)
      - [Set point weight](nodes/SetPointWeight/documentation.md)
      - [Set points](nodes/SetPoints/documentation.md)
    - [Primitive]()
      - [Delete primitives](nodes/DeletePrimitives/documentation.md)
      - [Get primtive](nodes/GetPrimitive/documentation.md)
      - [Group](nodes/GroupPrimitives/documentation.md)
      - [Ungroup](nodes/UnGroupPrimitives/documentation.md)
      - [Reverse primtive list](nodes/ReversePrimitiveList/documentation.md)
      - [Shift primtive list](nodes/ShiftPrimitiveList/documentation.md)
    - [Boolean 3d geometry](nodes/MeshBoolean/documentation.md)
  - [Transform]()
    - [Align](nodes/Align/documentation.md)
    - [Mirror](nodes/Mirror/documentation.md)
    - [Smart size](nodes/SmartSize/documentation.md)
    - [Transform](nodes/TransformPrimitives/documentation.md)
  - [UV nodes]()
    - [Flip uv](nodes/FlipUV/documentation.md)
    - [Get uv](nodes/ExtractUV/documentation.md)
  - [Collect](nodes/Collect/documentation.md)
  - [Null](nodes/Null/documentation.md)
  - [Switch](nodes/Switch/documentation.md)
- [Lists]()
  - [Number lists]()
    - [Clamped number list]()
    - [Closest value](nodes/ClosestValue/documentation.md)
    - [Combine number lists](nodes/CombineLists/documentation.md)
    - [Cull number list](nodes/CullList/documentation.md)
    - [Get number list item](nodes/GetListItem/documentation.md)
    - [Match number lists](nodes/MatchNumberLists/documentation.md)
    - [Reverse number list](nodes/ReverseList/documentation.md)
    - [Set number list item](nodes/SetListItem/documentation.md)
    - [Set number list items](nodes/SetListItems/documentation.md)
    - [Shift number list](nodes/ShiftList/documentation.md)
    - [Shuffle number list](nodes/ShuffleList/documentation.md)
    - [Sort number list](nodes/SortFloatList/documentation.md)
  - [String Lists]()
    - [Combine string lists](nodes/CombineStringLists/documentation.md)
    - [Cull string list](nodes/CullStringList/documentation.md)
    - [Find string in list](nodes/FindInStringList/documentation.md)
    - [Get string list item](nodes/GetStringListItem/documentation.md)
    - [Reverse string list](nodes/ReverseStringList/documentation.md)
    - [Set string list item](nodes/SetStringListItem/documentation.md)
    - [String list to string](nodes/StringListToString/documentation.md)
  - [Vector lists]()
    - [Combine vector lists](nodes/CombineVectorLists/documentation.md)
    - [Cull vector list](nodes/CullVectorList/documentation.md)
    - [Get vector list item](nodes/GetVectorListItem/documentation.md)
    - [Reverse vector list](nodes/ReverseVectorList/documentation.md)
    - [Set vector list item](nodes/SetVectorListItem/documentation.md)
    - [Set vector list items](nodes/SetVectorListItems/documentation.md)
    - [Shift vector list](nodes/ShiftVectorList/documentation.md)
    - [Shuffle vector list](nodes/ShuffleVectorList/documentation.md)
  - [List length](nodes/ListLength/documentation.md)
- [Math]()
  - [Basic math]()
    - [Absolute value](nodes/Abs/documentation.md)
    - [Add](nodes/Add/documentation.md)
    - [Divide](nodes/Divide/documentation.md)
    - [Modulo](nodes/Modulo/documentation.md)
    - [Multiply](nodes/Multiply/documentation.md)
    - [Power](nodes/Power/documentation.md)
    - [Square root](nodes/SquareRoot/documentation.md)
    - [Subtract](nodes/Subtract/documentation.md)
  - [Clamp]()
    - [Clamp](nodes/Clamp/documentation.md)
    - [Maximum](nodes/Max/documentation.md)
    - [Minimum](nodes/Min/documentation.md)
  - [Compare]()
    - [Equal](nodes/Equal/documentation.md)
    - [Equal vectors](nodes/EqualVectors/documentation.md)
    - [Greater](nodes/Greater/documentation.md)
    - [Less](nodes/Less/documentation.md)
  - [Logic]()
    - [And](nodes/And/documentation.md)
    - [Not](nodes/Not/documentation.md)
    - [Or](nodes/Or/documentation.md)
  - [Mapping]()
    - [Ease](nodes/Ease/documentation.md)
    - [Range](nodes/Range/documentation.md)
  - [Random]()
    - [Noise](nodes/SimplexNoise/documentation.md)
    - [Random number](nodes/RandomFloat/documentation.md)
    - [Random vector](nodes/RandomVectorV2/documentation.md)
  - [Rounding]()
    - [Ceiling](nodes/Ceiling/documentation.md)
    - [Floor](nodes/Floor/documentation.md)
    - [Round](nodes/Round/documentation.md)
  - [Value switch]()
    - [Number switch](nodes/FloatSwitch/documentation.md)
    - [String switch](nodes/StringSwitch/documentation.md)
    - [Vector switch](nodes/VectorSwitch/documentation.md)
  - [Trigonometry]()
    - [Arc cosine](nodes/Acos/documentation.md)
    - [Arc sine](nodes/Asin/documentation.md)
    - [Arc tangent](nodes/Atan/documentation.md)
    - [Arc tangent 2](nodes/Atan2/documentation.md)
    - [Cosine](nodes/Cos/documentation.md)
    - [Degrees to radians](nodes/DegToRad/documentation.md)
    - [Pi](nodes/Pi/documentation.md)
    - [Radians to degrees](nodes/RadToDeg/documentation.md)
    - [Sine](nodes/Sin/documentation.md)
    - [Tangent](nodes/Tan/documentation.md)
  - [Vector math]()
    - [Add vectors](nodes/AddVectorsV2/documentation.md)
    - [Angle between](nodes/AngleBetween/documentation.md)
    - [Cross product](nodes/Cross/documentation.md)
    - [Dot product](nodes/Dot/documentation.md)
    - [Multiply vector](nodes/MultiplyVector/documentation.md)
    - [Normalize vector](nodes/Normalize/documentation.md)
    - [Subtract vectors](nodes/SubtractVectors/documentation.md)
    - [Vector magnitude](nodes/Magnitude/documentation.md)
    - [Vector to xyz](nodes/VectorToXYZ/documentation.md)
    - [Xyz to vector](nodes/XYZToVector/documentation.md)
  - [Expression](nodes/ExpressionParser/documentation.md)
- [String]()
  - [Equal strings](nodes/EqualStrings/documentation.md)
  - [Join strings](nodes/StringJoin/documentation.md)
  - [Split string](nodes/StringSplit/documentation.md)
  - [JSON builder](nodes/JsonBuilder/documentation.md)
- [Utility]()
  - [Combine data](nodes/CombineData/documentation.md)
  - [Ephemeral state](nodes/Ephemeral/documentation.md)
  - [Error check](nodes/Error/documentation.md)

# Concepts

- [General concepts]()
  - [Graph](concepts/GeneralConcepts/graph.md)
    - [Node](concepts/GeneralConcepts/node.md)
      - [Input & Output types](concepts/GeneralConcepts/inputOutput.md)
    - [Connection](concepts/GeneralConcepts/connection.md)
    - [Parameter](concepts/GeneralConcepts/parameter.md)
    - [Output node](concepts/GeneralConcepts/outputNode.md)
    - [Import & Export](concepts/GeneralConcepts/importExport.md)
    - [Ephemeral state](concepts/GeneralConcepts/ephemeralState.md)
    - [Compute](concepts/GeneralConcepts/compute.md)
    - [Subgraph](concepts/GeneralConcepts/subgraphs.md)
  - [Primitive](concepts/GeneralConcepts/primitive.md)
    - [PolyMesh](concepts/GeneralConcepts/polyMesh.md)
    - [NURBS curve](concepts/GeneralConcepts/nurbsCurve.md)
    - [NURBS surface](concepts/GeneralConcepts/nurbsSurface.md)
    - [Points](concepts/GeneralConcepts/points.md)
    - [Locator](concepts/GeneralConcepts/locator.md)
  - [Attribute](concepts/GeneralConcepts/attribute.md)
  - [Asset](concepts/GeneralConcepts/assets.md)
  - [Material](concepts/GeneralConcepts/material.md)
