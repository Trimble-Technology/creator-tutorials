## Points to curve

**_Creates a curve using input points._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _points per curve_

  * The number of points that define a single curve. Multiple curves can be made from the same list of points by setting this input to a value lower than the number of input points.

* _order_

  * The value that defines the order of the output line. See &lt;a href="/concepts/GeneralConcepts/nurbsCurve.md" target="_blank">NURBS curve&lt;/a> for more information.

* _keepIncomingGeo_

  * Sets whether to keep the input primitives or not.

* _beziers_

  * Sets whether the output curve is a [bezier curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve) or not.


#### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


#### Note(s)



* Other names for this node include: Create curve.


#### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:fe2a797b-58c5-4a2e-941d-bcae38ae6515&version=latest" target="_blank">Points to curve</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:9be3e2e0-6dbb-4c83-a1f1-49a80e7f1cb2&version=latest" target="_blank">Spiral curve</a>
