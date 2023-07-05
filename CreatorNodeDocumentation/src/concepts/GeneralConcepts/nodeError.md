# Node Error

Nodes can error when the engine has been unable to successfully compute the output of a node. This could be due to a combination of inputs which is impossible to solve, or an internal operator error.

An errored node will cause downstream nodes to error as well, sometimes invalidating the graph's output. Care needs to be taken to avoid putting nodes in an errored state. To un-error an errored node, change its input value(s), which sometimes requires changing upstream node inputs.

An example is dividing by zero using the **Divide** node.

<p align="center">
  <img width="400" src="images/erroredNode.png"/>
</p>
