# Formula

**_Calculates the results of the written expression._**

---

> #### DEPRECATED
>
> This node is a duplicate of the [**Expression**](/nodes/ExpressionParser/documentation.md) node, and is now unneeded.
>
> Superseded by [Expression](/nodes/ExpressionParser/documentation.md)


#### Inputs

* _expression_

  * The string value to define the expression to calculate.

* _formula_

  * The string value to store an unparsed version of the expression. This input is not used when the graph is computed.

* _a_

  * The value that is used to define “a” in the _expression_ input.

* _b_

  * The value that is used to define “b” in the _expression_ input.

* _c_

  * The value that is used to define “c” in the _expression_ input.

* _d_

  * The value that is used to define “d” in the _expression_ input.

* _e_

  * The value that is used to define “e” in the _expression_ input.

* _f_

  * The value that is used to define “f” in the _expression_ input.

* _g_

  * The value that is used to define “g” in the _expression_ input.

* _h_

  * The value that is used to define “h” in the _expression_ input.

* _i_

  * The value that is used to define “i” in the _expression_ input.

* _j_

  * The value that is used to define “j” in the _expression_ input.

* _k_

  * The value that is used to define “k” in the _expression_ input.

* _l_

  * The value that is used to define “l” in the _expression_ input.

* _x_

  * The value that is used to define “x” in the _expression_ input.

* _y_

  * The value that is used to define “y” in the _expression_ input.

* _z_

  * The value that is used to define “z” in the _expression_ input.

* _w_

  * The value that is used to define “w” in the _expression_ input.


#### Outputs

* _result_

  * The result of the calculation as defined by the _expression_ input.

* _result list_

  * The list of results of the calculation as defined by the _expression_ input.


### Note(s)

* The list of possible operations that can be performed by this node are as follows:

  * +, -, *, /, \\, %, >, <, =>, =<, ==, =!, &&, ||, &, |, =^, **, ?:, min, max, sin, cos, tan, asin, acos, atan, atan2, sinh, cosh, tanh, round, ceil, floor, trunc, sqrt, pow, exp, log, log10, abs, sign.

* The [**Expression**](/nodes/ExpressionParser/documentation.md) node that supersedes this one has fewer inputs, exposing only _a_, _b_, _c_, _d_, _x_, _y_, _z_, and _w_.

* Other names for this node include: Formula parser.
