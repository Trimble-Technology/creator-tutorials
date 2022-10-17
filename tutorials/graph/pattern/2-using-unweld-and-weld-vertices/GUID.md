Quite often when we bring geometry into Creator, the edges are all welded together at unideal angles. We can see when this happens, as the geometry will have a ‘shimmer’ to it (you can see this if you click on the “window frame” node). 

We can fix this welding by using the **unweld vertices** and **weld vertices** nodes.

First, the **unweld vertices** completely unwelds all vertices in the input geometry, then, the **weld vertices** rewelds the geometry based on an *angle threshold*.

Adjust the angle threshold **number** parameter to see what different weld angles do to the geometry. We generally find that a good *angle threshold* is around `120`. 