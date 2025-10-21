# Size frame

---

A size frame defines the positions of grips when the <a href="https://help.sketchup.com/en/sketchup/scaling-your-model-or-parts-your-model" target="_blank">Scale Tool</a> is used on a [Live Component](/concepts/GeneralConcepts/liveComponent.md) in SketchUp.

### In Situ

The size frame in SketchUp will automatically appear when using the Scale Tool.

<p align="center">
  <img width="500" src="images\SizeFrameExample.gif"/>
</p>


### In Graph

#### Bound Axes

When a size frame’s axis is bound to a parameter and a user stretches the size frame (in SketchUp), the parameter's "value" input will be automatically updated as if the user had directly edited that parameter.

Only either a parameterized [number](nodes/FloatValue/documentation.md) node or parameterized [integer](nodes/IntegerValue/documentation.md) node will be able to have a size frame's axis bound to it. To bind a particular axis of a size frame to a particular parameter, right-click a parameterized node and navigate to the "Set Size" menu option. There are three options: `Use size X`, `Use size Y`, and `Use size Z`; each will bind the parameterized node to its respective axis.

Keep in mind that when an axis is bound to a parameter, the parameter receives only the scalar size along that axis, not any directional or orientation information.

<p align="center">
  <img width="500" src="images\SetParameterBindings.png"/>
</p>

#### Alignment

As the size frame is not defined by a [Live Component's](/concepts/GeneralConcepts/liveComponent.md) bounding box (like a normal component), the alignment of the size frame needs to be manually set.

To set the alignment of a size frame, right-click the background of the graph (no nodes or connections) and navigate to the "Size frame alignment" menu option. There are three options: `x`, `y`, and `z`, each with three options: `min`, `center`, and `max`; each will align the size frame by its extents to the world center / `0,0,0`.

<p align="center">
  <img width="500" src="images\SetAlignment.png"/>
</p>

### Notes

* There is only one size frame per [Live Component](/concepts/GeneralConcepts/liveComponent.md).
* It is important to note that it is up to the author to ensure that the effects of the size frame accurately reflect the expected behavior of the [Live Component](/concepts/GeneralConcepts/liveComponent.md). Here are a couple of things to look out for:
    * Be sure that the size frame's intended alignment matches the geometry it's intended to manipulate
        * e.g., the size frame should be aligned to `center` for each axis if the component is centered on `0,0,0`.
    * Be sure that the intended direction of a geometry being manipulated by the size frame is behaving as intended.
        * e.g., a parameter with a binding of "size x" isn’t changing the size in the y direction.
* If you are familiar with the [align](nodes/Align/documentation.md) node, aligning the size frame works similarly to if you were aligning geometry to a `value` rather than other geometry.
* Resizing a [Live Component](/concepts/GeneralConcepts/liveComponent.md) with the Scale Tool automatically makes that instance of the Live Component unique.
* The visibility of a [Live Component's](/concepts/GeneralConcepts/liveComponent.md) grips is determined by two things:
    * If an axis has been bound to a parameter or not.
    * If the bound parameter's "hide control" input is set to `true` or not.
* Visibility of the Scale Tool's edge or corner grips is determined by whether all relevant axes are visible (e.g. if both "size x" and "size y" are bound to parameters and visible, then the edge grips associated with those axes will also be visible).

### Examples

* <a href="https://creator.trimble.com/graph?asset=whp:104b90f3-fb5f-4dc9-a59d-1dc6232b30ae" target="_blank">Simple Box</a> (With "correct" parameter bindings)
* <a href="https://creator.trimble.com/graph?asset=whp:617d1e08-5fcc-4b24-bb0b-fd10699c96a3" target="_blank">Simple Box</a> (With "incorrect" parameter bindings)
* <a href="https://creator.trimble.com/graph?layout=bottom&asset=whp:599ac203-fcd3-40b3-a902-d4063466bd88" target="_blank">Window Template</a> (Size Frame aligned to min, min, min)
