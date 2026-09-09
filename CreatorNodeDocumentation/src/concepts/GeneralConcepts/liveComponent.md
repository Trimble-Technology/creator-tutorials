# SketchUp Live Components (LCs)

---

In SketchUp, a Live Component’s behavior is defined by a [graph](/concepts/GeneralConcepts/graph.md) authored in Trimble Creator.

For more info on SketchUp Live Components, see the <a href="https://help.sketchup.com/en/sketchup-live-components" target="_blank">help page here</a>.


### Notable features

There are a couple notable features you'll find in Trimble Creator that were specifically designed or enabled for SketchUp Live Components, they are listed below:

* A Live Component can have a [Size frame](/concepts/GeneralConcepts/sizeFrame.md) which can be activated and used by a user in SketchUp using the Scale Tool.

* A Live Component can [AutoFit](/concepts/GeneralConcepts/autoFit.md) to geometry that already exists in a user’s model, rebuilding itself to suit the face it is applied to.

* A Live Component can receive that geometry through a [**geometry input**](/nodes/GeometryInput/documentation.md) node, which is the entry point for geometry authored outside of the graph.


### Authoring an LC

In order for a [graph](/concepts/GeneralConcepts/graph.md) to be a Live Component, click on the SketchUp logo button on the left-hand side of the Trimble Creator app. This will take you to a page where you can download an SKP file containing the LC.


Note that the downloaded SKP must be imported in order for the LC to function properly (not just opened directly) as it requires that outer component layer in order to function properly.
