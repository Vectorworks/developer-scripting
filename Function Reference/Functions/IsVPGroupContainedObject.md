# IsVPGroupContainedObject

## Description
Determines if specified object is contained within a viewport group, and if so which type of group.

```pascal
FUNCTION IsVPGroupContainedObject(
				objectHandle : HANDLE;
				groupType    : INTEGER): BOOLEAN;
```

```python
def vs.IsVPGroupContainedObject(objectHandle, groupType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to object|
|groupType|INTEGER|Type of group containing the object: (1 = Crop, 2 = Annotation, 3 = Cache, 4 = Section)|

## Examples
```pascal
BEGIN
	htemp := h;
	{check if object is not in an annotation group of a ViewPort}
	IF ( NOT IsVPGroupContainedObject( htemp, 2 ) )
	then BEGIN
		WHILE ( (GetType(GetParent(htemp)) <> 31) ) DO htemp := GetParent(htemp);
		objH := htemp;
		layerH := GetParent(htemp);
	END

BEGIN
	IF (IsNewCustomObject (gPluginName)) OR ((GetLayer (gPluginHand) = NIL) AND (NOT IsVPGroupContainedObject (gPluginHand, 2){NOT a VP!})) THEN
	BEGIN
		datumRef := GetRField (formatH, gPluginName, 'datumRef');
		SetRField (gPluginHand, gPluginName, 'datumRef', datumRef);
	END

formatH := GetObject (gPluginName);
IF IsNewCustomObject (gPluginName) OR ((GetLayer (gPluginH) = NIL) AND (NOT IsVPGroupContainedObject( gPluginH, 2 ){NOT a VP!})) THEN
BEGIN
	{* Determine if the Part Info Record exists and, if not, create it.*}
	defaultRecName := GetLocStr (16001, 3);
	IF GetObject (defaultRecName) = NIL THEN
	BEGIN
		NewField (defaultRecName, GetLocStr (16001, 5), '0', 1, 0);
		NewField (defaultRecName, GetLocStr (16001, 6), ' ', 4, 0);
```
```python
import vs

# Determines if specified object is contained within a viewport group, and if
# so which type of group.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
groupType = 0

ok = vs.IsVPGroupContainedObject(objectHandle, groupType)
if ok:
    vs.Message('IsVPGroupContainedObject succeeded')
else:
    vs.Message('IsVPGroupContainedObject failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
