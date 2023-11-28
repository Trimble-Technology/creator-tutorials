# Flip UV

**_Swaps or flips UV coordinates of NURBS surfaces. Reverses NURBS curves._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mode_

  * Sets the mode in which the UV coordinates are manipulated. This can be `no change`, `flip U`, `flip V`, `flip U & V`, or `swap U & V`.

* _mask_

  * The list of boolean values that defines which primitives to apply manipulations to as set by the _mode_.


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)

* [NURBS curves](/concepts/GeneralConcepts/nurbsCurve.md) only have a U coordinate and will therefore only be affected by the `flip U` and `flip U & V` modes, effectively reversing the direction of the curve.

* Other names for this node include: FlipUV, Swap, and Reverse curve.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:67f86262-b4ca-4351-8c0b-157693ae3711&version=latest" target="_blank">Flip texture UVs on a NURBS surface</a>
