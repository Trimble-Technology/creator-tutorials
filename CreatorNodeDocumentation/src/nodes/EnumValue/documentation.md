## Choice:

Creates an enumeration (choice), shown as a dropdown.

When parameterized this node will appear as a dropdown in the “Parameter Panel”.

>This node has data inputs and outputs.
>
>This node does NOT have geometry inputs and outputs.


#### Inputs

* _value_

  * The option index and text to output.

* _options_

  * A comma separated list of options (e.g. `Option1,Option2,Option3`).

* _index offset_

  * Offset the chosen option index by this value.

* _default index_

  * The default option index to output when the _set to default_ input is set to `true` or the _value_ input is reset.

* _set to default_

  * Sets the _value_ input to the option index defined by the _default index_ input.

* _reset mode_

  * Sets the mode in which the option index is reset to the value defined by the _default index_ input. These can be `when any input changes` (resets the _value_ input whenever a connected input is changed) or `do not reset index` (does not reset the _value_ input at all).

* _hide control_

  * Hides the parameter control within the “Parameter panel” when the node is parameterized.

* _hide label_

  * Hides the parameter label (name) within the “Parameter panel” when the node is parameterized.


#### Outputs

* _value_

  * The chosen option index as defined by the _value_ input (with offset as defined by the _index offset_ input).

* _text_

  * The chosen option text as defined by the _value_ input.


#### Note(s)



* Other names for this node include: Dropdown, Menu, Choose, Enum, Enumeration, or Parameter.


#### Example(s)


* <a href="https://creator.trimble.com/graph?assetURI=whp:2a6de14a-1611-4d3a-959f-a1c34eae6bca&version=latest" target="_blank">Switching between geometries</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:c7dc99f1-334b-47ae-9622-fb38812db203&version=latest" target="_blank">Changing choice options</a>