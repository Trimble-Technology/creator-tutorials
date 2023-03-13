# Graph

Trimble Creator's core concept is a graph. Trimble Creator graphs represent logic that computes geometry (and other data).

Graphs are a collection of connected nodes.

<p align="center">
  <img width="400" src="images\CreatorCow.png"/>
</p>


### Graph Concepts

A graph describes:

* A set of particular nodes, and their input and output properties.
* Those nodes' input property values.
* Connections between those nodes' properties.
* Parameters and their values, which can be considered the graph's input.
* A set of output nodes: which of the above nodes should be computed to obtain the desired result from the graph's logic.
* The ephemeral state of the graph.


Materia graphs are directed acyclic graphs (DAG) that evaluate lazily.