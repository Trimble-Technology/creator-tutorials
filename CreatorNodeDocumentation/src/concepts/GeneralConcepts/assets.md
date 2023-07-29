# Assets

Assets are representations of stored data. E.g. a graph created by a user. Other types of assets may be external in origin and uploaded, e.g. an IGES or OBJ model.

### Asset URI

All assets are associated with a unique database identifier. It is a unique hash with a prefix specifying the asset storage provider.

For example, assets stored in the Trimble Warehouse Platform database use the `whp:` prefix, as in:

`whp:e6266721-3266-4065-bd90-d263fa568966`

### Upload limits

These are the approximate limits for asset uploading:

* 20MB per asset
* 100MB per session
* 100 uploads per session