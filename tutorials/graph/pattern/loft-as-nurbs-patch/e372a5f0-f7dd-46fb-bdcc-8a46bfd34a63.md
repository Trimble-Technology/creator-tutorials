The graph looks at lofting lines together to create a “NURBS” surface. Lofting as a “NURBS” surface takes input curves, and creates a smooth surface between them, based on the *order*.

Changing the *order* defines how smooth the final loft is. If you change the order to [ 2 ], you'll notice that the surface appears much more jagged and sharp. If you change it to [ 5 ], the surface is a lot smoother.

Click through the geometry nodes (start with the **line** node, then **copy**, then **loft**) in the graph to see how the final surface is created.

Try creating your own curves and loft them together using the **loft** node.