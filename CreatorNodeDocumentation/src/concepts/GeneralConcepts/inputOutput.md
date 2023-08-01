# Input & Output Types

---

### Geometry

An input or output representing a [node's](/concepts/GeneralConcepts/node.md) entry and exit point for [primitives](/concepts/GeneralConcepts/primitive.md). This input cannot be set, except by a [connection](/concepts/GeneralConcepts/connection.md) from one or more geometry outputs from other nodes.


### Boolean

An input or output representing a binary value: `true/false`, `on/off`, `show/hide`, etc.

* Default value: `false`.
* Can convert from: `float`, `integer`.
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**boolean**](/nodes/BooleanValue/documentation.md) node.
* Examples of valid values:
  * `true`
  * `false`


### Integer

This is a <a href="https://en.wikipedia.org/wiki/Integer_(computer_science)" target="_blank">signed 32bit integer</a>.

* Default value: `0`.
* Can convert from: `boolean`, `float`.
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**integer**](/nodes/IntegerValue/documentation.md) node.
* Examples of valid values:
  * `0`
  * `-58`
  * `1234567890`


### Nullable integer

This is a <a href="https://en.wikipedia.org/wiki/Nullable_type" target="_blank">nullable</a> <a href="https://en.wikipedia.org/wiki/Integer_(computer_science)" target="_blank">signed 32bit integer</a>.

* Default value: `0`.
* Can convert from: `boolean`, `float`, `null`.
* The only property which has this type is the value input of an [**integer**](/nodes/IntegerValue/documentation.md) node.
* Examples of valid values:
  * `null`
  * `0`
  * `-58`
  * `1234567890`


### Float

This is a <a href="https://en.wikipedia.org/wiki/Double-precision_floating-point_format" target="_blank">64bit double-precision floating point type</a>.

* Default value: `0.0`.
* Can convert from: `integer`, `boolean`.
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**number**](/nodes/FloatValue/documentation.md) node.
* Examples of valid values:
  * `0`
  * `0.0`
  * `-123.456`
  * `4.567e-8`
  * `-9.87E+0065`


### Nullable float

This is a<a href="https://en.wikipedia.org/wiki/Nullable_type" target="_blank">nullable</a> <a href="https://en.wikipedia.org/wiki/Double-precision_floating-point_format" target="_blank">64bit double-precision floating point type</a>.

* Default value: `0.0`.
* Can convert from: `integer`, `boolean`.
* The only property which has this type is the value input of a [**number**](/nodes/FloatValue/documentation.md) node.
* Examples of valid values:
  * `null`
  * `0`
  * `0.0`
  * `-123.456`
  * `4.567e-8`
  * `-9.87E+0065`


### Vector

A vector typically represents an XYZ coordinate in 3D space. It is an array of 3 <a href="https://en.wikipedia.org/wiki/Double-precision_floating-point_format" target="_blank">64bit double-precision floating point types</a>.

* Default value: `0, 0, 0`
* Can convert from: `color`
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**vector**](/nodes/VectorValue/documentation.md) node.
* Examples of valid values:
  * `1, 2, 3`
  * `-12.34, 56.78, 9.0e-10`


### Color

A color typically represents an RGB color value. But data-wise, it is essentially the same as a vector type (see above). It is an array of 3 <a href="https://en.wikipedia.org/wiki/Double-precision_floating-point_format" target="_blank">64bit double-precision floating point types</a>.

* The normal value range for each component is 0 to 1, but any double precision value is allowed. For example to obtain high dynamic range coloring.
* Default value: `0, 0, 0`
* Can convert from: `vector`
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**color**](/nodes/ColorValue/documentation.md) node.
* Examples of valid values:
  * `1, 0, 0` (red)
  * `0, 2.0, 0` (superbright green)
  * `0.0, 0, 1` (blue)
  * `1, 1, 0` (yellow)
  * `-1.3, 0, 0` (negative red; looks cyan; probably not advised!)
  * `10.234, 10.567, 5e4`(sky blue)


### String

* Default value: `""` (empty string).
* Can convert from: `integer`, `boolean`, `float`.
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**string**](/nodes/StringValue/documentation.md) node.
* Examples of valid values:
  * `""` (empty string)
  * `"1.234"`
  * `"The quick brown fox jumps over the lazy dog."`
  * `"Chuaigh bé mhórshách le dlúthspád fíorfhinn trí hata mo dhea-phorcáin bhig."`
  * `"中国俗语"`


### Enum

The enumeration type is an input type (only) that represents a choice in a list of options, typically displayed as a dropdown menu in a UI .

* Default value: `0`.
* Can convert from: `integer`, `boolean`, `float`.
* This type is one of the possible value types for [parameters](/concepts/GeneralConcepts/parameter.md), set by a [**choice**](/nodes/EnumValue/documentation.md) node.

Its value is an integer, to denote which option is picked, with `0` meaning the first item in the list provided by the options property of the input.
