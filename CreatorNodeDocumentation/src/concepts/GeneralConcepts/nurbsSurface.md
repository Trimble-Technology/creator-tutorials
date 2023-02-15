# NURBS surface

A NURBS surface is a primitive representing a 3D <a href="https://en.wikipedia.org/wiki/Non-uniform_rational_B-spline" target="_blank">NURBS</a> surface. A NURBS surface always has a rectangular topology, with coordinates in two axes: U and V values varying between `0` and `1`.

NURBS curves and surfaces lend themselves well to parametric modeling applications. For example, one can easily extract a NURBS curve from a NURBS surface's particular U or V value, or create a NURBS surface from several NURBS curves.

A NURBS surface has following notable properties:

* _control points_: a list of 3D vectors representing the 3D coordinates of the points that define the surfaces's mathematical spline function.
* _order_ (in both U and V direction): a positive integer defining the number of nearby control points that influence any given point on the surface in U or V direction. Practically: the higher the number, the smoother the surface. Order 2 effectively makes the surface faceted.

<p align="center">
  <img width="400" src="images/NURBS.png"/>
</p>
