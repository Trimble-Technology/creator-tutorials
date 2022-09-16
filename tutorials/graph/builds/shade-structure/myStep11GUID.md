To specify how many copies we will need, we need to do a little math. In order to manipulate data, create an **expression** node and input the value output from the “Length” parameter node into the a input of the **expression** node.

The expression we will be using in this case is [a/500+1]. This is a simple equation which divides the a input (the length) by a spacing of 500, then adding an extra purlin on the end (+1).

Connect the result output of the **expression** node into the *# of copies* input of the **copy** node.
