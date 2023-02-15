# Loop

**Loop _nodes repeat a section of the graph._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


### Inputs

* _# of loops_

  * The number of loops to iterate through.

* _iterator tag_

  * The tag of an **iterator **node to reference an **iterator**-**loop** pair.

* _cumulative_

  * Sets whether the loop is cumulative or not. See the Note(s) section below for more information.


### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)



* Loop types:
    * A non-cumulative loop (the default loop) is a type of loop that repeats the section of a graph between an **iterator**-**loop** node pair for the defined number of loops. The geometry output of the **loop** node with this type of loop is the result of every iteration/loop, acting similarly to the **copy** node.
    * A cumulative loop is a type of loop that also repeats a section of the graph for a defined number of loops. Only with a cumulative loop, the previous iteration is used to inform the next iteration, accumulating changes each iteration.
        * The current iteration of the loop as defined by the _idling value_ of the relevant **iterator** node will only compute the nodes as though it were a non-cumulative loop. The full computation of a cumulative loop can only be seen from the final **loop** node.
* To be used in conjunction with an **iterator** node assigned with the same tag.
* Other names for this node include: Iterate.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:0892473a-e280-4dbf-8186-752079bef11e&version=latest" target="_blank">Loops: 2D boolean two sets of curves</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:cbceb42a-0345-480c-9ecb-31ea52eec5c5&version=latest" target="_blank">Loops: Recursive align</a>
