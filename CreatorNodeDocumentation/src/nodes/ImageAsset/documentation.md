# Image asset

**_Imports an image asset._**

> This node has data inputs and outputs.
>
> This node does NOT have geometry inputs and outputs.


### Inputs

* _preload asset_

  * Sets whether to load the output image asset on graph load or not.

* _asset uri_

  * The asset URI (as a string value) that defines what uploaded image asset to output. See <a href="/concepts/GeneralConcepts/assets.md" target="_blank">Assets</a> for more information.


### Outputs

* _asset uri_

  * The asset URI of the uploaded image asset as defined by the _asset uri_ input. See <a href="/concepts/GeneralConcepts/assets.md" target="_blank">Assets</a> for more information.

* _asset name_

  * The name of the uploaded image asset (as a string value). 


### Notes



* Images can be uploaded to Trimble Creator by dragging and dropping the file into the Graph Viewer.
* Trimble Creator supports following image file formats for import:
    * JPEG / JPG
    * PNG
* Other names for this node include: Picture, Texture, Bitmap, JPEG, JPG, and PNG.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:b432f0b3-3b32-4867-8b38-8647efa60924&version=latest" target="_blank">Assigning materials and textures</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:518f2715-d7e9-491c-888c-9481b272776f&version=latest" target="_blank">Flip texture UVs</a>
