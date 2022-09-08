# Looping; Wave extrude

This graph pattern demonstrates how to use a **loop** node to extrude rectangles based on a sine wave. A **loop** node, when paired with an **iterator**, cycles through connected primitives and applies logic to each one. One of the most important things to remember when pairing **loops** and **iterators** is to make sure that their *tag* is the same

This **loop** cycles through the connected rectangles and extrudes each one based on a different value in a sine wave.

There is a bit of math involved in making this graph work, so take your time exploring the output values of each node to understand the logic behind it.

# Points to curve

In this graph, we demonstrate how to create curves from a set of points. **Points to curve** is one of the most useful nodes you’ll find in Creator.

In this example, we can change the start point (vector) of the curve, as well as the *order*. Changing the order defines how many intersection points the curve has.

Explore the output of the **vector switch** node to understand how the starting point is changing.

Have a look through the rest of the graph to understand how the curve is being created.

# Loft as NURBS patch

The graph looks at lofting lines together to create a “NURBS” surface. Lofting as a “NURBS” surface takes input curves, and creates a smooth surface between them, based on the *order*.

Changing the *order* defines how smooth the final loft is. If you change the order to [ 2 ], you'll notice that the surface appears much more jagged and sharp. If you change it to [ 5 ], the surface is a lot smoother.

Click through the geometry nodes (start with the **line** node, then **copy**, then **loft**) in the graph to see how the final surface is created.

Try creating your own curves and loft them together using the **loft** node.

# Smart-sizing geometry

In this graph pattern, we look at the **smart size** node, and how you can resize your geometry while retaining its proportions.

**Smart size** allows you to define an *axis* as well as *lock zones* at the geometry minimum and maximum. These *lock zones* Let geometry within the zones be unaffected by the smart size, remaining the same proportion.

Have a look at the first **smart sizes** inputs to see what it’s doing. You’ll see that it is sizing the geometry along the Z axis (blue), while locking the geometry in the bottom 25% and the top 25% of the window frame. The next **smart size** node is doing the same thing, but along the X axis (red).

Adjust the number parameters to see the smart size in action.

# Assigning materials & textures

This graph looks at assigning materials and textures to geometry.

Assigning materials is very easy in Creator, and is done using the **material** node.

To assign a texture, you need to first use a **project UV** node. This will define how the texture is mapped to the geometry.

Click through each of the final **material** nodes in the graph to see each one in action. Try changing some of the inputs to see how the material changes.

# Curve to polyline

**Curve to polyline** can be used for multiple reasons. The first is to convert a “NURBS” curve to a “polyline”, while the second is to simply change the resolution of a “polyline”.

When converting a “NURBS” curve to a polyline, you will also need to define the resolution of the output curve.

You can define the resolution in multiple ways:

* *Number of segments*
* *Segment length*
* *Approx segment length*

Look at each **curve to polyline** output, and try changing the associated parameter to see how the output curve changes.

Hint: It helps if you turn on point rendering in the 3D viewer toolbar.

# Triangulate an outline

If you have a curve that you want to turn into a shape in the graph, you can do this using the **triangulate 2d path** node.

In this example, we first take a partial **circle**, turn it into a curve using **points** and **points to curve**, and then turn it back into a surface using the **triangulate 2d path** node.

To turn a curve into a surface using this node, the input curve must be planar (two-dimensional). Once you triangulate it, the surface will be projected back to the 0 value of whichever *work plane* you selected.

Click through the geometry nodes in the graph to see how the **triangulate 2D path** node works.