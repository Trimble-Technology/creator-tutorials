# Locator:

**_Creates a locator._**

---


### Inputs

* _id_

  * The string value that defines the ID of the locator.

* _position_

  * The vector value that defines the position of the locator.

* _type_

  * The string value that defines the position of the locator.

  * Currently there are only two types: the default locator type (when the _type_ input is left empty) and a `snap`. The `snap` type can be set by entering this JSON string: `{"type": "snap"}`.


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



* When creating snaps, snaps are designed to snap together by their axis like so: `z^ x><x z^`. In other words, the positive x direction of one locator will face the positive x direction of the other and the two positive z directions of both locators will be aligned.
* See [Locator](/concepts/GeneralConcepts/locator.md) for more information on the locator primitive type.
* Other names for this node include: Handle, Snap, and Control point.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:9e89fa57-1628-443f-a7fa-b799df36e61f&version=latest" target="_blank">Using locators</a>
