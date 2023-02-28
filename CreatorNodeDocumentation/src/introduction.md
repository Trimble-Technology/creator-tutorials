# Introduction

Trimble Creator's core concept is a graph. Trimble Creator graphs represent logic that computes geometry (and other data).

<p align="center">
  <img width="400" src="concepts\GeneralConcepts\images\CreatorCow.png"/>
</p>

Graphs are a collection of connected nodes. Individual nodes represent compute functions, like the creation of a polygonal box, the noise math operation, or the act of joining two curves.

_NOTE: This documentation is currently in an 'in-progress' state and is therefore incomplete. Updates will be made periodically._


### Node types

#### Value & Parameter nodes

These nodes represent Trimble Creator's base type values, and lists thereof.

Some value nodes can be tagged as parameters, ie: inputs to the graph.

Examples can be found in the [Parameter nodes](nodeSections/parameterSection.md) section.

#### Geometry Creation nodes

These nodes create primitives. They usually do not feature a geometry input.

Some nodes produce NURBS geometry, others meshes, etc. Some create multiple types of primitives depending on their input properties.

Some examples can be found in the [Creation nodes](nodeSections/creationSection.md) section.

#### Geometry Modifier nodes

These are the meat of Trimble Creator's compute engine. These nodes take incoming geometry and modify it. Sometimes the input and output geometry are of different primitive types.

Some examples can found in the [Geometry nodes](nodeSections/geometrySection.md) section.
