# DTM6_IsDTM6Object

## Description
Check if the passed object handle is for SiteModel object type.

```pascal
FUNCTION DTM6_IsDTM6Object(hDTMObject : HANDLE): BOOLEAN;
```

```python
def vs.DTM6_IsDTM6Object(hDTMObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|A handle of an object to be checked.|

## Examples
```pascal
IF (hSelectedDTM = NIL) or (not DTM6_IsDTM6Object(hSelectedDTM) ) THEN
	BEGIN
	{no DTM object below the selection}
	AlrtDialog(GetPlugInString(7002));
	END

{check to see if the selected is a DTM object}
IF NOT DTM6_IsDTM6Object( hDTMObject ) THEN
	hDTMObject		:= NIL;
```
```python
import vs

# Check if the passed object handle is for SiteModel object type.
hDTMObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.DTM6_IsDTM6Object(hDTMObject)
if ok:
    vs.Message('DTM6_IsDTM6Object succeeded')
else:
    vs.Message('DTM6_IsDTM6Object failed')
```

## Version
Availability: from All Versions

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
