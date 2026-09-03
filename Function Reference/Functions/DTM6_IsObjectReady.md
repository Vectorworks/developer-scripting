# DTM6_IsObjectReady

## Description
Checks if this passed DTM object is ready for use. That means that the object has associated internal data (triangulated data and so which doesn't allow the document to be big). If this returns false, you can call [ ResetObject](ResetObject.md) to prepare the object to be used.

As of Vectorworks 2011 this function will always return true.

```pascal
FUNCTION DTM6_IsObjectReady(hDTMObject : HANDLE): BOOLEAN;
```

```python
def vs.DTM6_IsObjectReady(hDTMObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|   |

## Examples
```pascal
	BEGIN
	{no DTM object below the selection}
	AlrtDialog(GetPlugInString(7002));
	END
ELSE IF NOT DTM6_IsObjectReady(hSelectedDTM) THEN
	BEGIN
	{DTM is not updated!}
	AlrtDialog(GetPlugInString(7011));
	END

{try to find a DTM object below the Selected}
hDTMObject := DTM6_GetDTMObject( ActLayer, TRUE );
IF hDTMObject = NIL then AlrtDialog( GetPluginString(5008) );
{check if the found DTM object is Ready for use}
IF (hDTMObject  <> NIL ) AND (not DTM6_IsObjectReady( hDTMObject )) then BEGIN
	AlrtDialog( GetPluginString(5009) );
	hDTMObject := NIL;
	END;

dtmHand := DTM6_GetDTMObject(NIL, TRUE);
IF NOT DTM6_IsObjectReady(dtmHand) THEN ResetObject(dtmHand);
pathHand := GetCustomObjectPath(objHand);
```
```python
import vs

# Checks if this passed DTM object is ready for use.
hDTMObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.DTM6_IsObjectReady(hDTMObject)
if ok:
    vs.Message('DTM6_IsObjectReady succeeded')
else:
    vs.Message('DTM6_IsObjectReady failed')
```

## Version
Availability: all versions.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
