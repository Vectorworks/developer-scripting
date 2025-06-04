# DTM6_GetDTMObject

## Description
Try to find a Site Model instance. If there is only one Site Model in the document, return it.

If there are more than one, check the passed layer, if there is only one Site Model on that layer - return it.

If the passed layer is NIL or contains more than one Site Model, and 'bPickUpModel' is TRUE, show a dialog, asking the user to pick a Site Model from all available.

Returns NIL if there are no Site Models found or the user canceled the dialog.

```pascal
FUNCTION DTM6_GetDTMObject(
				hLayer       : HANDLE;
				bPickUpModel : BOOLEAN):HANDLE;
```

```python
def vs.DTM6_GetDTMObject(hLayer, bPickUpModel):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|A handle to a layer to be searched for site model objects.|
|bPickUpModel|BOOLEAN|Pas in TRUE if a UI is to be used to identify Site model object if there are several instances on the layer.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
