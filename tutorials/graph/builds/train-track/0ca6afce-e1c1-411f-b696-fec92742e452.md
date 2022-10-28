Now that we have the sleepers copied along the curve, we also want them to point in the direction of that curve. We can use the same **copy using vectors** node to do this by setting the _normals_ and _up vectors_ inputs.

The _normals_ in this case refer to the direction that the copied objects will face, which will be the tangents of the points within the curve. We can get the tangents by creating a **normals** node from the **curve to polyline** node and setting the _mode_ input to `tangents, normals, binormals (basis)`.

Then, connect the _tangents_ output on the **normals** node to the _normals_ input on the **copy using vectors** node.