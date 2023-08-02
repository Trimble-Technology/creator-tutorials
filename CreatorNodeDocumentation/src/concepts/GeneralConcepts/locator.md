# Locator

---

A locator is a point with orientation.

Some typical use cases of a locator:

* An indicator of an important location in a 3D scene or object.
* A placeholder for a more complex 3D object.
* As a snap or connection point between 3D objects.
* A grip or handle to move geometry in a 3D view.
* A lightweight carrier of metadata or [attributes](/concepts/GeneralConcepts/attribute.md).

### Locator primitive

The locator concept is expressed via a `LocatorPrimitive`. This [primitive](/concepts/GeneralConcepts/primitive.md) is essentially a point with orientation. It has the following properties:

* An ID: a user-settable persistent ID
* A transform matrix: this gives the locator its position and orientation.
* Semantic type: can be used to turn a locator into a more complex concept, like a snapping point.
* This primitive is a 3D object, and can be transformed like one, for example using a [**transform**](/nodes/TransformPrimitives/documentation.md) node.

As with all [primitives](/concepts/GeneralConcepts/primitive.md), it can carry [attributes](/concepts/GeneralConcepts/attribute.md).


### Locator node

To create one or more locators, use the [**locator**](/nodes/Locator/documentation.md) node.
