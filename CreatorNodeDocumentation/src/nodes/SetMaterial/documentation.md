# Material

**_Sets the material properties of primitives._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _primitive mask_

  * The list of boolean values that defines which input primitives to set the material properties to. If empty, all input primitives will be set to the defined material properties.

* _set base color_

  * Sets whether to set a base color material property to the input primitives or not.

* _base color_

  * The color value (vector) that defines the base color to set the input primitives when the _set base color_ input is set to `true`.

* _set base texture_

  * Sets whether to set a base texture material property to the input primitives or not.

* _base texture_

  * The string value (image asset URI) that defines the base texture to set to the input primitives when the _set base texture _input is set to `true`.

* _set opacity_

  * Sets whether to set an opacity material property to the input primitives or not.

* _opacity_

  * The value that defines the opacity to set to the input primitives (between a range of `0` and `1`) when the _set opacity _ input is set to `true`.

* _set roughness_

  * Sets whether to set a roughness material property to the input primitives or not.

* _specular roughness_

  * The value that defines the specular roughness to set to the input primitives (between a range of `0` and `1`) when the _set roughness_ input is set to `true`.

* _roughness texture_

  * The string value (image asset URI) that defines the roughness texture to set to the input primitives when the _set roughness_ input is set to `true`.

* _set metallic_

  * Sets whether to set a metallic material property to the input primitives or not.

* _metallic_

  * The value that defines the metalness to set to the input primitives (between a range of `0` and `1`) when the _set metallic _input is set to `true`.

* _metallic texture_

  * The string value (image asset URI) that defines the metallic texture to set to the input primitives when the _set metallic _input is set to `true`.

* _set reflectance_

  * Sets whether to set a reflectance material property to the input primitives or not.

* _reflectance_

  * The value that defines the reflectance to set to the input primitives (between a range of `0` and `1`) when the _set reflectance _input is set to `true`.

* _reflectance texture_

  * The string value (image asset URI) that defines the reflectance texture to set to the input primitives when the _set reflectance _input is set to `true`.

* _set bump_

  * Sets whether to set a bump material property to the input primitives or not.

* _bump_

  * The value that defines the bump to set to the input primitives (between a range of `0` and `1`) when the _set bump _input is set to `true`.

* _bump texture_

  * The string value (image asset URI) that defines the bump texture to set to the input primitives when the _set bump _input is set to `true`.

* _set incandescence_

  * Sets whether to set an incandescent material property to the input primitives or not.

* _incandescence_

  * The color value (vector) that defines the incandescence to set to the input primitives (between a range of `0` and `1`) when the _set incandescence _input is set to `true`.

* _incandescence texture_

  * The string value (image asset URI) that defines the incandescence texture to set to the input primitives when the _set incandescence _input is set to `true`.

* _set double-sided_

  * Sets whether to set the material properties on the input primitives to be double-sided or not.

* _double-sided_

  * Sets whether to make the material properties double-sided or not.

* _set texture size_

  * Sets whether to set the size of the texture inputs to set to the input primitives or not.

* _texture size_

  * The value that defines the size of the textures used in the material properties (also known as the UV scale of the textures).


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



* See [Material](/concepts/GeneralConcepts/material.md) for more information on the specfics of materials in Trimble Creator.
* Other names for this node include: Set Material and Shader.


### Example(s)



* <a href="https://creator.trimble.com/graph?assetURI=whp:b432f0b3-3b32-4867-8b38-8647efa60924&version=latest" target="_blank">Assigning materials and textures</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:db8352d7-1c4f-4f7a-aeb5-fad07cf14a5e&version=latest" target="_blank">Semi-transparent textures</a>
