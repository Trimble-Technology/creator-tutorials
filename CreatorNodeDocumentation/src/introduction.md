# Introduction

The core concept of the app is a [graph](/concepts/GeneralConcepts/graph.md). Graphs represent logic that computes geometry [primitives](/concepts/GeneralConcepts/primitive.md) (and other data), which flows through the graph.

<p align="center">
  <img width="600" src="concepts\GeneralConcepts\images\CreatorCow.png"/>
</p>

A [graph](/concepts/GeneralConcepts/graph.md) is a collection of two main elements:

1. [Nodes](/concepts/GeneralConcepts/node.md)
   * Individual nodes represent compute functions, like the creation of a [polygonal box](/nodes/PolyBox/documentation.md) [primitive](/concepts/GeneralConcepts/primitive.md), a [noise](/nodes/SimplexNoise/documentation.md) generator, or the act of [joining](/nodes/JoinCurves/documentation.md) two curves.
   *  <a href="https://creator.trimble.com/graph?assetURI=whp:1b4e8dd2-0de7-431a-b60e-a8c5a9412250&version=latest" target="_blank">This graph</a> has most nodes that exist within the app.  Check it out!
   * More information can be found in the [Node](/concepts/GeneralConcepts/node.md) conecept section.

2. [Connections](/concepts/GeneralConcepts/connection.md)
   * Connections represent the relationship between an output of one node, and the output of another node.
   * More information can be found in the [Connection](/concepts/GeneralConcepts/connection.md) concept section.


Together, nodes and connections represent the flow of geometry and data to generate and compute an authored output.