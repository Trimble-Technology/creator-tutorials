## NURBS curve

A NURBS curve is a primitive representing a 3D <a href="https://en.wikipedia.org/wiki/Non-uniform_rational_B-spline" target="_blank">NURBS</a> curve. These curves are smooth mathematical spline interpolations of a set of control points. A NURBS curve is parametrised along a U coordinate, varying between `0` and `1`.

A NURBS curve has following notable properties:

* _control points_: a list of 3D vectors representing the 3D coordinates of the points that define the curves's mathematical spline function.
* _order_: a positive integer defining the number of nearby control points that influence any given point on the curve. Practically: the higher the number, the smoother the curve. Order 2 effectively turns the curve into a polyline connecting the control points with straight line segments.

<p align="center">
  <img width="400" src="images/NURBS.png"/>
</p>
