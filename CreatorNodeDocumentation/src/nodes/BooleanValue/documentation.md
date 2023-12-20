# Boolean

**_Creates a boolean value._**

---


#### Inputs

* _value_

  * Boolean value to output.

* _default_

  * The default value to output when the _set to default_ input is set to `true`.

* _set to default_

  * Sets the _value_ input to the value defined by the _default_ input.

* _hide control_

  * Hides the parameter control within the parameter panel when the node is parameterized.

* _hide label_

  * Hides the parameter label (name) within the parameter panel when the node is parameterized.


#### Outputs

* _value_

  * The boolean value as defined by the _value_ input.


### Notes

* When parameterized this node will appear as a false/true toggle in the parameter panel.

* A boolean value is in essence a `0` or `1` integer value. `0` is `false` and `1` is `true`.

* The _value_ input can accept any numerical value (floating value or integer). The **boolean** node will convert a value of `0` to `false` (`0`) whereas any other value other than `0` will return `true` (`1`).

* Other names for this node include: BooleanValue, Checkbox, State, Bit, Binary, On/Off, True/False, or Parameter.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:89687422-0229-4242-99ba-05c8ab7bba7b&version=latest" target="_blank">Hiding geometry</a>
