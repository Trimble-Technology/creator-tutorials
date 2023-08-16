# Node

---

A node within a [graph](/concepts/GeneralConcepts/graph.md) represents a function.

Each node has a defined set of input and output properties.


### Node Input

A node has a defined set of inputs, or input properties. Node input properties can be considered the arguments to the function that the node represents. For example: the _radius_ input of a [**sphere**](/nodes/PolySphere/documentation.md) node. Internally this is a float value argument to the function that creates the sphere.

<p align="center">
  <img width="600" src="images/sphereInput.png"/>
</p>

Node inputs can be set directly, but also by other nodes through [connections](/concepts/GeneralConcepts/connection.md).

For more specifics, see node [input and output types](/concepts/GeneralConcepts/inputOutput.md).


### Node Output

A node also has a defined set of outputs, or output properties. The [property values](/concepts/GeneralConcepts/inputOutput.md) can be considered the result of executing the function that the node represents.

<p align="center">
  <img width="600" src="images/sphereOutput.png"/>
</p>

Output values are calculated on compute.

For more specifics, see node [input and output types](/concepts/GeneralConcepts/inputOutput.md).


### Node Error

Nodes can error when the engine has been unable to successfully compute the output of a node. This could be due to a combination of inputs which is impossible to solve, or an internal operator error.

An errored node will cause downstream nodes to error as well, sometimes invalidating the graph's output. Care needs to be taken to avoid putting nodes in an errored state. To un-error an errored node, change its input value(s), which sometimes requires changing upstream node inputs.

An example is dividing by zero using the [**divide**](/nodes/Divide/documentation.md) node.

<p align="center">
  <img width="400" src="images/erroredNode.png"/>
</p>

Errors can be 'caught' using graph logic, by the [**error check**](/nodes/Error/documentation.md) node.


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