# Assets

---

Assets are representations of stored data. E.g. a graph created by a user. Other types of assets may be external in origin and uploaded, e.g. an IGES or OBJ model.

### Asset types

Any file can be an asset, but in practice only the following asset types are relevant:

* The primary asset is a [graph](/concepts/GeneralConcepts/graph.md).
* A few geometry formats are recognized. Geometry files need to be stored as assets to be used.
* A few image formats are recognized for use as material textures. They too need to be stored as assets to be used.

See the [Import & Export](/concepts/GeneralConcepts/ImportExport.md) page for a list of supported formats.

### Asset policies

Key asset policies:

* Assets can be saved, but not deleted.
* All assets are versioned in version streams.
* An asset can be owned by a single user, determined by the first version of the asset, or it can be owned by an organization if the user saved the asset while acting on behalf of that organization.
* The user must own the asset to save a new version of it.
* There are limits to asset uploading. See section below.

### Storing assets

#### Save

There are multiple states in which a graph can be saved. Saving will:

* Start a new asset version stream if the current asset has not been saved previously under the current user or organization.
* Version up an existing version stream.
* If the asset name has changed, saving will either:
  * Start a new asset version stream.
  * Version up an existing version stream.
* If the asset name has changed to an existing asset with that name, saving will prompt to either:
  * Version up an existing version stream.
  * Rename the graph and



### Asset URI

All assets are associated with a unique database identifier. It is a unique hash with a prefix specifying the asset storage provider.

For example, assets stored in the Trimble Warehouse Platform database use the `whp:` prefix, as in:

`whp:e6266721-3266-4065-bd90-d263fa568966`

### Upload limits

These are the approximate limits for asset uploading:

* 20MB per asset
* 100MB per session
* 100 uploads per session