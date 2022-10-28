To array the profiles along the base curve, we will be using the same logic that we used previously to copy the sleepers.

Copy and paste the **curve to polyline**, **normals**, and **copy using vectors** nodes and their associated connections. Then all we need to do is make a few adjustments:



1. Delete the geometry connection between the **box** and **copy using vectors** nodes.
2. Delete the data connection between the “Approx. sleeper spacing” **number** and **curve to polyline** nodes.
3. On the copy/pasted **curve to polyline** node set the following inputs:
    * _mode_ =	`approx segment length`
    * _length_ =	`300`