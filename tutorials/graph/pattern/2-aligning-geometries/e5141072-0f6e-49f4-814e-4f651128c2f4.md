To align geometry to one another, we can use the **align** node. It is important to note that the second connected geometry will always be aligned to the first connected geometry.

We have three examples of the **align** node in this graph, though there are many more ways to use it. The top example shows the alignment of a smaller box to a larger one. If you go into the inputs of this aligned node, you’ll see exactly how it's being aligned. For example, align the x axis, it is aligning the “max” of the second connection to the first connection “min”.

The next two examples do a similar thing, but also utilize the *offset* in order to parametrically define how far the second object is offset from the first, after it is aligned. 