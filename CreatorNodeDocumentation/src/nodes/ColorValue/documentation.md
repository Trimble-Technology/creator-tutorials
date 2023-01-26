## Color:

Creates a color (vector) value.

When parameterized this node will appear as three input fields and a color picker in the “Parameter panel”.

>This node has data inputs and outputs.
>
>This node does NOT have geometry inputs and outputs.


#### Inputs

* _value_

  * The color value to output.

* _default_

  * The default value to output when the _set to default_ input is set to `true`.

* _set to default_

  * Sets the _value_ input to the value defined by the _default_ input.

* _hide control_

  * Hides the parameter control within the “Parameter panel” when the node is parameterized.

* _hide label_

  * Hides the parameter label (name) within the “Parameter panel” when the node is parameterized.


#### Outputs

* _value_

  * The color value as defined by the _value_ input.


#### Note(s)



* A color value is defined by three values between `0` and `1`.
    * Any inputted value above `1` will be rounded back down to `1`.
    * Any inputted value below `0` will be rounded back up to `0`.
* Vectors can be utilized as a color value.
* A color value can be set via the “color picker” by clicking on the colored box next to the _value_ and _default_ inputs.
* Other names for this node include: Parameter.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:bc96d8e6-ac0b-4daa-92e6-587764b8d6b4&version=latest" target="_blank">Set color</a>