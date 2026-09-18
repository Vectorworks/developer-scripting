# GetNumberOfComponents

## Description
Gets the number of components in an object.

```pascal
FUNCTION GetNumberOfComponents(
				obj               : HANDLE;
				VAR numComponents : INTEGER): BOOLEAN;
```

```python
def vs.GetNumberOfComponents(obj):
    return (BOOLEAN, numComponents)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|numComponents|INTEGER|Returns the number of components.|

## Examples
```pascal
BEGIN
	if GetNumberOfComponents(temp_h, numberOfCompon) THEN
	BEGIN
		selCompIndex := 0;
		ALLOCATE slabName[ 1 .. numberOfCompon ];
		FOR ctr2 := 1 TO numberOfCompon DO
		BEGIN
			slabName[ctr2] := GetComponentName( temp_h, ctr2 );

BEGIN
result := GetNumberOfComponents( extStyle_h, numberOfComponents );
coreComponentIndex := GetCoreWallComponent( extStyle_h );
IF coreComponentIndex <> 0 THEN
	BEGIN
	for cnt:= 1 to numberOfComponents DO

BEGIN
	wallStyleName := GetWallStyle(wall_h);
	wallStyleHand := GetObject(wallStyleName);
	IF wallStyleHand <> NIL THEN BEGIN
		result := GetNumberOfComponents( wallStyleHand, numberOfComponents );
		temp_r := 0;
		for cnt:= 1 to numberOfComponents DO BEGIN
			result := GetComponentWidth( wallStyleHand, cnt, currTMPOffset );
			temp_r := temp_r + currTMPOffset;
```
```python
import vs

# Gets the number of components in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, numComponents = vs.GetNumberOfComponents(obj)
vs.Message('GetNumberOfComponents returned: ' + str((ok, numComponents)))
```

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
