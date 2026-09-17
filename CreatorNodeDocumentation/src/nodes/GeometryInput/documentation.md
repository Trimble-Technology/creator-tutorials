# Geometry input

**_Parses JSON encoded geometry into geometry primitives._**

---

> #### DEPRECATED
>
> The field `geometryToParse` of `input` is renamed to `value`.
>
> Superseded by [Geometry input](/nodes/GeometryInputV2/documentation.md)


#### Inputs

* _json geometry_

  * The JSON encoded string that defines the geometry to parse. This can be a single polyline or PolyMesh, or an array of them.
    * Defaults to a flat, `1000` unit square polyline (`{"id":"emptyPolyLine","points":[[0,0,0],[1000,0,0],[1000,1000,0],[0,1000,0],[0,0,0]]}`) — despite the `emptyPolyLine` id, this is real geometry, not an absence of it.

* _geometry schema_

  * An optional JSON schema to validate the incoming _json geometry_ against. Leave this empty to parse the geometry without validating it.

* _guidance type_

  * Sets whether the incoming JSON geometry is expected to follow a plane. These are `None` and `Align with a plane`. The geometry from the JSON needs to comply with this guidance to produce the expected output.

* _coordinate plane for guidance_

  * The coordinate plane the incoming JSON geometry should align with when _guidance type_ is set to `Align with a plane`. These are `XY`, `YZ`, and `ZX`.


#### Outputs

* **_geometry_**

  * Output geometry primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)

* This node is how geometry authored outside of the graph gets into it. Use the current [**geometry input**](/nodes/GeometryInputV2/documentation.md) node for new graphs.

* The expected JSON format follows the polyline and PolyMesh definitions in the <a href="https://github.com/Trimble-Technology/eidos-json-schema" target="_blank">eidos-json-schema</a> repository. Only those two [**primitive**](/concepts/GeneralConcepts/primitive.md) types are supported.

* Other names for this node include: GeometryInput.
