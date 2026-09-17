# AutoFit

---

An AutoFit Live Component is a [Live Component](/concepts/GeneralConcepts/liveComponent.md)  featuring a **[geometry input](/nodes/GeometryInput/documentation.md)** node—it ingests SketchUp surfaces to automatically adapt its shape using a chosen face.

![](images\AutofitExample.gif)

### In Situ

When an AutoFit Live Component is applied to a face in SketchUp, that face is converted to JSON and passed into the [graph](/concepts/GeneralConcepts/graph.md) through its **[geometry input](/nodes/GeometryInput/documentation.md)** node. The graph then [computes](/concepts/GeneralConcepts/compute.md) its output utilizing this new geometry.

Once placed an AutoFit Live Component can have its input geometry changed by right clicking and selecting 'Refit Live Component'.

![](images\Refit.png)

### In Graph

An AutoFit graph uses a **[geometry input](/nodes/GeometryInput/documentation.md)** node as one of its parametric inputs. 

Most often the incoming geometry is used as base geometry — something to build from or within — rather than as a set of measurements. The face stays a primitive and the graph can operate on it directly:

- Build from it with nodes like **[extrude mesh](/nodes/Extrude/documentation.md)** to give it thickness, **[offset 2d path](/nodes/OffsetCurve/documentation.md)** to inset or outset its boundary, or **[loft](/nodes/Skin/documentation.md)** to build a surface between its boundary and another curve derived from it.
- Build within it by treating it as the boundary that contains what the graph generates, e.g. laying a pattern of panels across the face and keeping only the part that sits inside its edges.

Measuring the incoming geometry is the other option, and the two are usually combined — take dimensions off the face, then build against those measurements rather than against [parameter](/concepts/GeneralConcepts/parameter.md) values:

- Measure it with nodes like **[geometry bounds](/nodes/GeometryBounds/documentation.md)**, **[geometry size](/nodes/GeometrySize/documentation.md)**, and **[geometry center](/nodes/GeometryCentroid/documentation.md)**, or work directly from the *points* outputs of the **[geometry input](/nodes/GeometryInput/documentation.md)** node.
- Place and scale against it with nodes like **[align](/nodes/Align/documentation.md)**, **[transform](/nodes/TransformPrimitives/documentation.md)**, and **[smart size](/nodes/SmartSize/documentation.md)** — **[smart size](/nodes/SmartSize/documentation.md)** is particularly useful here, as it lets a component stretch to an arbitrary incoming size while preserving detail inside its lock zones.
- Distribute repeated detail across it with nodes like **[copy](/nodes/Copy/documentation.md)**, **[copy using vectors](/nodes/Copy2/documentation.md)**, or **[iterator](/nodes/Iterator/documentation.md)**, using the measured size to work out how many copies are needed.



### Notes

- The **[geometry input](/nodes/GeometryInput/documentation.md)** node must be paramaterized to make the Live Component an AutoFit Live Component.
- It is up to the author to make sure the graph resolves sensibly for as many different geometry inputs as possible. Things worth handling explicitly:
  - Nothing supplied at all — the **[geometry input](/nodes/GeometryInput/documentation.md)** node's default is a flat `1000` unit square polyline (not truly empty geometry, despite its `emptyPolyLine` id), so a graph should still produce something reasonable before it has been given a face in SketchUp.
  - Geometry outside the range the component was designed for, e.g. a face far smaller or larger than any sensible instance of the component.
- If the graph errors, or otherwise ends up producing no geometry at all, SketchUp falls back to its own error handling and flags the Live Component as having no geometry. That flag is all a user gets — it doesn't say what went wrong or how to recover — so the more cases the graph handles itself, the better the user experience.
- AutoFit and a [size frame](/concepts/GeneralConcepts/sizeFrame.md) can both be present in the same Live Component, but be deliberate about it — if a size frame drives the same dimensions the incoming geometry does, the two will fight. Instead only use the sizeframe to adjust dimensions not controlled by the **[geometry input](/nodes/GeometryInput/documentation.md)** , or have a toggle to switch between the LC using the size frame or the geometry input.



### Examples

- [Simple Extrude](https://creator.trimble.com/graph?asset=whp:7334e873-94f9-46d2-a994-4c5c8cb516eb)

