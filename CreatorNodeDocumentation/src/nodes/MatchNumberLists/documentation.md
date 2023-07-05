# Match number lists

**_Checks the commonality between two number lists._**

---


#### Inputs

* _list 1_

  * The first list to match against.

* _list 2_

  * The second list to match against.


#### Outputs

* _list 1 matches_

  * The list of booleans signaling whether the value at a particular index in _list 1_ matches any value within _list 2_.

* _list 2 matches_

  * The list of booleans signaling whether the value at a particular index in _list 2_ matches any value within _list 1_.


### Note(s)

* This node returns two lists of booleans, one for each input list (same length) - items are true if the number at their index is found in the other list.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:5e22d8ba-e52f-45fb-b2da-01466b706c69&version=latest" target="_blank">Identify and apply commonality</a>
