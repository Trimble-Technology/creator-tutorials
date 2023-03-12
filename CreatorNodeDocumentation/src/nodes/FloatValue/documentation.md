# Number

**_Creates a number (floating point) value._**

---


### Inputs

* _value_

  * The number value to output.

* _default_

  * The default value to output when the _set to default_ input is set to `true` or the _value_ input is `null`.

* _set to default_

  * Sets the _value_ input to the value defined by the _default_ input.

* _min/max mode_

  * The mode in which the _value_ input is constrained. See the <a href="/concepts/GeneralConcepts/misc.md" target="_blank">min/max mode</a> section for more information.

* _min_

  * The minimum value of the slider range.

* _max_

  * The maximum value of the slider range.

* _hide control_

  * Hides the parameter control within the “Parameter panel” when the node is parameterized.

* _hide label_

  * Hides the parameter label (name) within the “Parameter panel” when the node is parameterized.

* _hide input field_

  * Hides the parameter input field within the “Parameter panel” when the node is parameterized.

* _hide slider_

  * Hides the parameter slider within the “Parameter panel” when the node is parameterized.


### Outputs

* _value_

  * The integer value as defined by the _value_ input.

* _input is null_

  * Outputs a boolean value that indicates whether the _value_ input is `null` (`true`) or not (`false`).


### Note(s)



* When parameterized this node will appear as a slider and input field in the Parameter panel.
* Other names for this node include: Float, Double, Decimal, Real, and Parameter.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:2b2bfb2f-ffeb-4cd3-ae15-fe1f0b59cf33&version=latest" target="_blank">Scaling a box</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:b783bdc2-5bea-49b6-b68e-a7eabee7993c&version=latest" target="_blank">Smart sizing geometry</a>
