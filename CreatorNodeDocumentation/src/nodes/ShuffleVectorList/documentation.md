# Shuffle vector list

**_Shuffles a vector list._**

---


#### Inputs

* _list_

  * The list of vector values to shuffle.


#### Outputs

* _list_

  * The shuffled list of vector values.


### Note(s)

* This node will shuffle the input vector list each time it is computed. In other words, it will re-shuffle the input vector list whenever the input vector list changes, a node upstream of it has changed (even if the values in the list itself seems to stay the same), or the graph is re-loaded.

* Other names for this node include: Randomize, and Randomise.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:655c7745-82cf-4da9-9268-da04a2658150&version=latest" target="_blank">Randomly select a set of vectors</a>
