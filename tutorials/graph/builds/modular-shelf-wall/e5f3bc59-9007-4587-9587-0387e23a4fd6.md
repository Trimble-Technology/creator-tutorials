You may have noticed that whenever the “Modules wide” parameter value is odd, the graph will instead give us the next even number. This is by design so that we don’t need to recalculate for each row of hexagons. We can instead more easily remedy this by checking when the “Modules wide” parameter is odd, and remove a column of hexagons. This is where that **group** node helps us to define the columns.

There are many mathematical ways we can figure out if the “Modules wide” parameter is odd, but the easiest way is to use the **modulo** node. Create a **modulo** node and connect its _value 1_ input to the _value_ output of the “Modules wide” **integer** node. Set the **modulo** nodes _value 2_ input to `2`.

What is a modulo operation?

Shortly put, a modulo operation finds the remainder after one value has been divided by another.

In Layman's terms, if you had 12 oranges and needed to pack them in sets of 5, you would have 2 oranges left over. So, `12` _modulo_ `5` `=` `2`.

In the context of this graph (`“Modules wide”` _modulo_ `2`), the remainder will be 0 or 1 depending if the whole number is even or odd.