# Create material

**_Creates a material definition._**

---


#### Inputs

* _base color_

  * The color value that defines the albedo (base color) of the material.

* _set base texture_

  * Sets whether to assign a base texture to the material or not.

* _base texture_

  * The string value (image asset URI) that defines the base texture to assign when the _set base texture_ input is set to `true`.

* _set opacity_

  * Sets whether to set an opacity property on the material or not.

* _opacity_

  * The value that defines the opacity of the material (between a range of `0` and `1`) when the _set opacity_ input is set to `true`. Values below `1` make the material transparent.

* _x scale_

  * The value that defines the UV scale of textures along U.

* _y scale_

  * The value that defines the UV scale of textures along V.

* _set roughness_

  * Sets whether to set a roughness property on the material or not.

* _roughness_

  * The value that defines the roughness of the material (between a range of `0` and `1`) when the _set roughness_ input is set to `true`.

* _roughness texture_

  * The string value (image asset URI) that defines the roughness texture to assign when the _set roughness_ input is set to `true`.

* _set metallic_

  * Sets whether to set a metallic property on the material or not.

* _metallic_

  * The value that defines the metalness of the material (between a range of `0` and `1`) when the _set metallic_ input is set to `true`.

* _metallic texture_

  * The string value (image asset URI) that defines the metallic texture to assign when the _set metallic_ input is set to `true`.

* _set normal texture_

  * Sets whether to assign a normal map to the material or not.

* _normal map_

  * The value that defines the strength of the normal map (between a range of `-10` and `10`) when the _set normal texture_ input is set to `true`.

* _normal map texture_

  * The string value (image asset URI) that defines the normal map texture to assign when the _set normal texture_ input is set to `true`.

* _set ambient occlusion_

  * Sets whether to set an ambient occlusion property on the material or not.

* _ambient occlusion_

  * The value that defines the strength of the ambient occlusion (between a range of `-10` and `10`) when the _set ambient occlusion_ input is set to `true`.

* _ambient occlusion texture_

  * The string value (image asset URI) that defines the ambient occlusion texture to assign when the _set ambient occlusion_ input is set to `true`.


#### Outputs

* _material_

  * A reference to the created material definition. Connect this to the _material_ input of an [**apply material**](/nodes/ApplyMaterial/documentation.md) node.


### Note(s)

* This node does not assign a material to geometry on its own. Connect its _material_ output to an [**apply material**](/nodes/ApplyMaterial/documentation.md) node.

* Texture inputs accept an image URL, or the _asset uri_ output of an [**image asset**](/nodes/ImageAsset/documentation.md) node.

* See [Material](/concepts/GeneralConcepts/material.md) for more information.

* Other names for this node include: CreateMaterial, Definition, Shader, Shading, Roughness, Reflectance, Albedo, Opacity, Transparency, Emission, and Bump.
