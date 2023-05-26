# Ephemeral State

Graphs have a boolean value representing their ephemeral state, and this state is exposed to graph logic through the **ephemeral** node (see [Ephemeral](nodes/Ephemeral/documentation.md) for more information). A graph is in an ephemeral state when parameters are actively being configured/adjusted. For example, when one is dragging a number slider in the Parameter panel.

The ephemeral state can, for example, be used to lower detail and compute load when a user is configuring the graph.