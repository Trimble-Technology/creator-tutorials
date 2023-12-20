# Graph

---

The core concept of the app is a graph. Graphs represent logic that [computes](/concepts/GeneralConcepts/compute.md) geometry (and other data).

Graphs are a collection of connected [nodes](/concepts/GeneralConcepts/node.md).

<p align="center">
  <img width="600" src="images\CreatorCow.png"/>
</p>


### Graph Concepts

A graph describes:

* A set of particular [nodes](/concepts/GeneralConcepts/node.md), and their input and output properties.
* Those nodes' [input properity values](/concepts/GeneralConcepts/inputOutput.md).
* [Connections](/concepts/GeneralConcepts/connection.md) between those nodes' properties.
* [Parameters](/concepts/GeneralConcepts/parameter.md) and their values, which can be considered the graph's input.
* A set of [output nodes](/concepts/GeneralConcepts/outputNode.md): which of the above nodes should be [computed](/concepts/GeneralConcepts/compute.md) to obtain the desired result from the graph's logic.
* The [ephemeral state](/concepts/GeneralConcepts/ephemeralState.md) of the graph.


The graphs are directed acyclic graphs (<a href="https://en.wikipedia.org/wiki/Directed_acyclic_graph" target="_blank">DAG</a>) that evaluate lazily.
