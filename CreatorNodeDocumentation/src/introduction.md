# Introduction

The core concept of the app is a [graph](/concepts/GeneralConcepts/graph.md). Graphs represent logic that computes geometry [primitives](/concepts/GeneralConcepts/primitive.md) (and other data), which flows through the graph.

<p align="center">
  <img width="600" src="concepts\GeneralConcepts\images\CreatorCow.png"/>
</p>

Graphs are a collection of [connected](/concepts/GeneralConcepts/connection.md) [nodes](/concepts/GeneralConcepts/node.md). Individual nodes represent compute functions, like the creation of a [polygonal box](/nodes/PolyBox/documentation.md) [primitive](/concepts/GeneralConcepts/primitive.md), a [noise](/nodes/SimplexNoise/documentation.md) generator, or the act of [joining](/nodes/JoinCurves/documentation.md) two curves.

 <a href="https://creator.trimble.com/graph?assetURI=whp:1b4e8dd2-0de7-431a-b60e-a8c5a9412250&version=latest" target="_blank">This graph</a> has most nodes that exist within the app.  Check it out!


### Node types

#### Value & parameter nodes

* These nodes represent base type [values](/concepts/GeneralConcepts/inputOutput.md), and lists thereof.
* Some value nodes can be tagged as [parameters](/concepts/GeneralConcepts/parameter.md), ie: inputs to the [graph](/concepts/GeneralConcepts/graph.md).


#### Geometry creation nodes

* These nodes create geometry [primitives](/concepts/GeneralConcepts/primitive.md).
* Some nodes produce NURBS [surfaces](/concepts/GeneralConcepts/nurbsSurface.md)/[curves](/concepts/GeneralConcepts/nurbsCurve.md), others [polygon meshes](/concepts/GeneralConcepts/polyMesh.md), etc. Some create multiple types of [primitives](/concepts/GeneralConcepts/primitive.md) depending on their [input](/concepts/GeneralConcepts/inputOutput.md) properties.


#### Geometry modifier nodes

* These are the meat of the [graph's](/concepts/GeneralConcepts/graph.md) compute engine. These nodes take incoming geometry and modify it. Sometimes the input and output geometry are of different [primitive](/concepts/GeneralConcepts/primitive.md) types.


#### Geometry measurement nodes

* These nodes typically convert from geometry input to data: they take geometry [primitives](/concepts/GeneralConcepts/primitive.md) as input, but do not feature a geometry output.


#### Loop & switch nodes

* [Loops](/nodes/Loop/documentation.md) and [switches](/nodes/Switch/documentation.md) are special case nodes that enrich the flow in a [graph](/concepts/GeneralConcepts/graph.md). These nodes allow elegant solutions to complex problems. They reduce graph size, increase performance, and unlock otherwise impossible graph logic.
* A geometry [Switch](/nodes/Switch/documentation.md) plays a special role in graphs, as it evaluates only one upstream input branch, and blocks evaluation of all other inputs. This contributes to performance.


#### Math nodes

* The [graph](/concepts/GeneralConcepts/graph.md) features an [Experssion](/nodes/ExperssionParser/documentation.md) node, but simple math problems can be represented by small chains of math nodes. These are orders of magnitude faster than expressions.
* Math nodes can operate on single [values](/concepts/GeneralConcepts/inputOutput.md), or lists. This includes trigonometry and vector math nodes.


#### Logic nodes

* Compare [values](/concepts/GeneralConcepts/inputOutput.md), negate flags, and otherwise combine boolean values.
* Prep (boolean) lists of logical bits to act as filters/masks in the [graph](/concepts/GeneralConcepts/graph.md).

#### Mapping, rounding, and clamping nodes

* Map number [ranges](/nodes/Range/documentation.md), [clamp](/nodes/Clamp/documentation.md), [round](/nodes/Round/documentation.md), etc.


#### Random number nodes

* Generate random [numbers](/nodes/RandomFloat/documentation.md), [vectors](/nodes/RandomVectorV2/documentation.md), and [noise](/nodes/SimplexNoise/documentation.md).


#### List nodes

* These nodes manipulate lists of incoming data.
* The [graph](/concepts/GeneralConcepts/graph.md) only features straight lists of a single type. No nested lists or structures.


#### String nodes

* These nodes manipulate strings.


#### Rendering nodes

* These nodes provide tools to apply [materials](/nodes/SetMaterial/documentation.md) and textures to geometry [primitives](/concepts/GeneralConcepts/primitive.md).
* More information on the concept of Materials in the [graph](/concepts/GeneralConcepts/graph.md) can be found in the [Material](concepts/GeneralConcepts/material.md) concept section.

#### Attribute nodes

* [Add](/nodes/AddAttribute/documentation.md) and [extract](/nodes/GetAttribute/documentation.md) metadata to/from [graphs](/concepts/GeneralConcepts/graph.md), nodes, [primitives](/concepts/GeneralConcepts/graph.md) and points.
* More information the concept of Attributes in the app can be found in the [Attribute](concepts/GeneralConcepts/attribute.md) concept section.