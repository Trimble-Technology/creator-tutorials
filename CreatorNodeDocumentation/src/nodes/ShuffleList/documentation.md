# Shuffle number list

**_Shuffles the items of a number list._**

---


#### Inputs

* _list_

  * The list of values to shuffle.


#### Outputs

* _list_

  * The shuffled list of values.


### Note(s)

* This node will shuffle the input list each time it is computed. In other words, it will re-shuffle the input list whenever the input list changes, a node upstream of it has changed (even if the values in the list itself seems to stay the same), or the graph is re-loaded.

* Other names for this node include: Randomize, and Randomise.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:fbed43f7-7809-4058-a081-0be7b4d282ca&version=latest" target="_blank">Shuffle number list</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:011d4f37-c270-4b29-ae82-641ea371f336&version=latest" target="_blank">Shuffle primitive list</a>
