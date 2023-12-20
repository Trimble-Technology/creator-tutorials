# Ease

**_Performs an ease function on 0 to 1 input values._**

---


#### Inputs

* _value_

  * The value to ease.

* _function_

  * Sets the function in which the input _value_ will be eased with. The list of options can be found in the Note(s) section below.

* _repeat mode_

  * Sets the mode in which a function is repeated to ease a list of values. This can be `clamp`, `repeat`, or `swing`.


#### Outputs

* _result_

  * The eased value.

* _result list_

  * The list of eased values.


### Note(s)

* The list of possible functions as as follows:

  * `Linear`, `QuadraticIn`, `QuadraticOut`, `QuadraticInOut`, `CubicIn`, `CubicOut`, `CubicInOut`, `QuarticIn`, `QuarticOut`, `QuarticInOut`, `QuinticIn`, `QuinticOut`, `QuinticInOut`, `SinusoidalIn`, `SinusoidalOut`, `SinusoidalInOut`, `ExponentialIn`, `ExponentialOut`, `ExponentialInOut`, `CircularIn`, `CircularOut`, `CircularInOut`, `ElasticIn`, `ElasticOut`, `ElasticInOut`, `BackIn`, `BackOut`, `BackInOut`, `BounceIn`, `BounceOut`, or `BounceInOut`.
  * To see what each of these functions look like, have a look at the "Ease Visualization" example below.

* Other names for this node include: Animation, Animate, Interpolate, Ramp, and Gradient.


### Example(s)

* <a href="https://creator.trimble.com/graph?asset=whp:ccc52e9e-5b24-467d-a190-63bbcaada403&version=latest" target="_blank">Ease Visualization</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:9fcc6f91-c9eb-4b58-bd23-a77689aa20ba&version=latest" target="_blank">Using UVs to deform meshes</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:45738561-dcda-4b42-9c0b-4e645a341ca4&version=latestt" target="_blank">Using noise to distort points along a single axis</a>
