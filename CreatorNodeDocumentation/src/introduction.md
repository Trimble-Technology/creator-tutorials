# Introduction

Trimble Creator's core concept is a graph. Graphs represent logic that computes geometry primitives (and other data), which flows through the graph.

<p align="center">
  <img width="400" src="concepts\GeneralConcepts\images\CreatorCow.png"/>
</p>

Graphs are a collection of connected nodes. Individual nodes represent compute functions, like the creation of a polygonal box primitive, a noise generator, or the act of joining two curves.

 <a href="https://creator.trimble.com/graph?assetURI=whp:f790227f-a092-4595-86ca-f6e7d2eeac14&version=latest" target="_blank">This graph</a> has most nodes that exists within Trimble Creator.  Check it out!


### Node types

#### Value & parameter nodes

These nodes represent base type values, and lists thereof.

Some value nodes can be tagged as parameters, ie: inputs to the graph.

Examples can be found in the [Parameter nodes](nodeSections/parameterSection.md) section.

#### Geometry creation nodes

These nodes create geometry primitives.

Some nodes produce NURBS geometry, others polygon meshes, etc. Some create multiple types of primitives depending on their input properties.

Examples can be found in the [Creation nodes](nodeSections/creationSection.md) section.

#### Geometry modifier nodes

These are the meat of Trimble Creator's compute engine. These nodes take incoming geometry and modify it. Sometimes the input and output geometry are of different primitive types.

Some examples can found in the [Geometry](nodeSections/geometrySection.md) section.

#### Geometry measurement nodes

These nodes typically convert from input to data: they take geometry primitives as input, but do not feature a geometry output.

Some examples can be found in the [Measure nodes](nodeSections/measureSection.md) section.

#### Loop & switch nodes

Loops and switches are special case nodes that enrich the flow in a graph. These nodes allow elegant solutions to complex problems. They reduce graph size, increase performance, and unlock otherwise impossible graph logic.

A geometry Switch plays a special role in graphs, as it evaluates only one upstream input branch, and blocks evaluation of all other inputs. This contributes to performance.

Some examples can be found in the [Copy & Loop nodes](nodeSections/copyAndLoopSection.md) section.

#### Math nodes

Trimble Creator features an Expression node, but simple math problems can be represented by small chains of math nodes. These are orders of magnitude faster than expressions.

Math nodes can operate on single values, or lists. This includes trigonometry and vector math nodes.

Some examples can be found in the [Math](nodeSections/mathSection.md) section.

#### Logic nodes

Compare values, negate flags, and otherwise combine boolean values.

Prep (boolean) lists of logical bits to act as filters/masks in the graph.

Some examples can be found in the [Compare nodes](nodeSections/compareSection.md) and [Logic nodes](nodeSections/logicSection.md) sections.

#### Mapping, rounding, and clamping nodes

Map number ranges, clamp, round, etc.

Some examples can be found in the [Mapping nodes](nodeSections/mappingSection.md), [Rounding nodes](nodeSections/roundingSection.md), and [Clamp nodes](nodeSections/clampSection.md) sections.

#### Random number nodes

Generate random numbers, vectors, noise.

Some examples can be found in the [Random nodes](nodeSections/randomSection.md) section.

#### List nodes

These nodes manipulate lists of incoming data.

Trimble Creator only features straight lists of a single type. No nested lists or structures.

Some examples can be found in the [Lists](nodeSections/listSection2.md) section.

#### String nodes

These nodes manipulate strings.

Some examples can be found in the [String](nodeSections/stringSection.md) section.

#### Rendering nodes

These nodes provide tools to apply materials and textures to geometry primitives.

Some examples can be found in the [Material & Texture nodes](nodeSections/materialTextureSection.md) section.

More information on the concept of Materials in Trimble Creator can be found in the [Material](concepts/GeneralConcepts/material.md) section.

#### Attribute nodes

Add and extract metadata to/from graphs, nodes, primitives and points.

Some example can be found in the [Attribute nodes](nodeSections/attributeSection.md) section.

More information the concept of Attributes in Trimble Creator can be found in the [Attribute](concepts/GeneralConcepts/attribute.md) section.