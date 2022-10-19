To set a random color, we will use the **random vector** node. Create a **random vector** node and connect the *value* output of the **iterator** to the *seed* input of our new **random vector** node. This will set a random vector (or in this case, color value) based on each iteration value of the loop.

Then connect the *result* output of the **random vector** node to the *color* input of the **set color** node, applying the random color.
