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

## Examples
```pascal
BEGIN
	if hDTMObject = nil then BEGIN
		hDTMObject := DTM6_GetDTMObject(hObjLayer, TRUE);
	END;

{work with the DTM over which the first selection is}
hSelectedDTM	:= DTM6_GetDTMObject( hDTMLayer, TRUE );

gResetErr := FALSE;
temp_s := getlname(actlayer);
ForEachObject(preflight,(SEL & (L = temp_s)));
{try to find a DTM object below the Selected}
hDTMObject := DTM6_GetDTMObject( ActLayer, TRUE );
IF hDTMObject = NIL then AlrtDialog( GetPluginString(5008) );
{check if the found DTM object is Ready for use}
IF (hDTMObject  <> NIL ) AND (not DTM6_IsObjectReady( hDTMObject )) then BEGIN
	AlrtDialog( GetPluginString(5009) );
```
```python
import vs

# Try to find a Site Model instance.
hLayer = vs.ActLayer()  # handle to the active design layer
bPickUpModel = True

objHandle = vs.DTM6_GetDTMObject(hLayer, bPickUpModel)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
